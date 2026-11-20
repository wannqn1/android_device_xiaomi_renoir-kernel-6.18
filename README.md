# Renoir 6.18.39-Tempest kernel package

This package contains the ARM64 Image, Shima DTB, renoir DTBO and 313 modules
used by the LineageOS 24.0 renoir product. The module dependency checks and DT
overlay validation passed. The complete ROM build and boot are unverified.

| Source repository | Revision |
| --- | --- |
| [Kernel](https://github.com/wannqn1/android_kernel_xiaomi_sm7350) | `dc9b4cf5fc48235be4b8b90b53ab9b0586a9ef5d` |
| [Device trees](https://github.com/wannqn1/android_kernel_xiaomi_sm7350-devicetrees) | `ab735cc44d85f053d1b63cc4e4ebdd70fe5d33f0` |
| [External modules](https://github.com/wannqn1/android_kernel_xiaomi_sm7350-modules) | `999fadfb7deff2afaf93fda97d00dbceef991fde` |

Build the kernel, DT images, and modules together when updating this package.

The package restores the legacy `/sys/mm_hardware` diagnostics and the Shima
EPSS L3 interconnect provider. The legacy L3 latency governor and CVP
accelerator still require a 6.18 port. The Qualcomm watchdog modules are
included for device testing, with the watchdog node disabled in the Renoir
device tree.
