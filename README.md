# Renoir 6.18.39-Tempest kernel package

This package contains the ARM64 Image, Shima DTB, renoir DTBO and 313 modules
used by the LineageOS 24.0 renoir product. The module dependency checks and DT
overlay validation passed. The complete ROM build and boot are unverified.

| Source repository | Revision |
| --- | --- |
| [Kernel](https://github.com/wannqn1/android_kernel_xiaomi_sm7350) | `2db0cd1d5ce4a5376dd23cd810dafca52453ceaa` |
| [Device trees](https://github.com/wannqn1/android_kernel_xiaomi_sm7350-devicetrees) | `1c1c2aff30ebbaa24aa08ddd687a20c566ec4635` |
| [External modules](https://github.com/wannqn1/android_kernel_xiaomi_sm7350-modules) | `a9b97cbf93b0663bab2b4fa6b638506520ae7d12` |

The header archive contains the ARM64 Linux UAPI and the Qualcomm module
UAPI from those same source revisions. Soong extracts each header as a declared build
output and exports the include directory to the Qualcomm HALs.

Build the kernel, DT images, and modules together when updating this package.
The kernel staging script regenerates the header archive.

The package includes multimedia hardware diagnostics and Qualcomm DCVS
scaling for the L3 cache, DDR, and LLCC. The Qualcomm watchdog modules are
included with the watchdog node disabled pending reset and suspend tests.

The kernel source provides a `cvp` target that stages a separate 315-module
test package with the CVP-enabled DTB and the CVP and SYNX modules. Its
firmware files, reserved memory, module dependencies, and DT overlay pass
static checks. EVASS startup and CVP sessions still need testing on a Renoir
handset.
