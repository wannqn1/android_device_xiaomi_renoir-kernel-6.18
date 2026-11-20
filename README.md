# Renoir 6.18.39-Tempest kernel package

This package contains the ARM64 Image, Shima DTB, renoir DTBO and 313 modules
used by the LineageOS 24.0 renoir product. The module dependency checks and DT
overlay validation passed. The complete ROM build and boot are unverified.

| Source repository | Revision |
| --- | --- |
| [Kernel](https://github.com/wannqn1/android_kernel_xiaomi_sm7350) | `e0b22baeab6794d5f9f44428359c32a5c2989c4c` |
| [Device trees](https://github.com/wannqn1/android_kernel_xiaomi_sm7350-devicetrees) | `3752a09df9858c7c9a047a0010287017e08dae94` |
| [External modules](https://github.com/wannqn1/android_kernel_xiaomi_sm7350-modules) | `999fadfb7deff2afaf93fda97d00dbceef991fde` |

Build the kernel, DT images, and modules together when updating this package.

The package includes the legacy multimedia hardware diagnostics, Shima EPSS
L3 provider, per-core L3 memory latency voting, and DDR and LLCC scaling through
Qualcomm DCVS. The CVP accelerator still needs hardware validation before
inclusion. The Qualcomm watchdog modules are included for device testing, with
the watchdog node disabled in the Renoir device tree.
