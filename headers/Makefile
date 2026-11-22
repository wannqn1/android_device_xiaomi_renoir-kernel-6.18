# SPDX-License-Identifier: GPL-2.0-only
# Expose the prebuilt UAPI through LineageOS's generated kernel headers rule.

.PHONY: headers_install
headers_install: include/kernel-uapi-headers.tar.gz
	@test -n "$(O)" || { echo "Set O to the kernel header output directory" >&2; exit 1; }
	@mkdir -p "$(O)"
	@tar -xzf "$<" -C "$(O)"
