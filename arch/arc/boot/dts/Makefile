# SPDX-License-Identifier: GPL-2.0
# Built-in dtb
builtindtb-y		:= nsim_700

ifneq ($(CONFIG_ARC_BUILTIN_DTB_NAME),)
	builtindtb-y	:= $(CONFIG_ARC_BUILTIN_DTB_NAME)
endif

obj-y   += $(builtindtb-y).dtb.o
dtb-y := $(builtindtb-y).dtb

# for CONFIG_OF_ALL_DTBS test
dtb-	:= $(patsubst $(src)/%.dts,%.dtb, $(wildcard $(src)/*.dts))

# board-specific dtc flags
DTC_FLAGS_hsdk += --pad 20
