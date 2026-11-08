# SPDX-License-Identifier: GPL-2.0
#
# 8849 Tank3 boards (mt6895) — DTB / DTBO
#

# 树内 dts 用 "mediatek/xxx.dtsi" 前缀引用同目录文件
DTC_INCLUDE += $(srctree)/arch/arm64/boot/dts/oblue

dtb-$(CONFIG_ARCH_MEDIATEK) += \
	mt6895.dtb

dtbo-$(MACH_TANK3) += tank3.dtbo
tank3.dtbo-base := mt6895.dtb

# tank3.dtbo 要在 mt6895.dtb 的 __symbols__ 上做 fixup, base 必须带 -@
DTC_FLAGS_mt6895 += -@
DTC_FLAGS_tank3 += -@ -H epapr
