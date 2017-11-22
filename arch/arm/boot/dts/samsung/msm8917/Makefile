ifeq ($(CONFIG_OF),y)

ifeq ($(CONFIG_SEC_ON5QLTE_PROJECT),y)
        ifeq ($(CONFIG_MACH_ON5QLTE_CHN_OPEN),y)
                dtb-y += msm8917-sec-on5qlte-chn-r00.dtb
		dtb-y += msm8917-sec-on5qlte-chn-r01.dtb
        endif
endif

ifeq ($(CONFIG_SEC_ELITELTE_PROJECT),y)
        ifeq ($(CONFIG_MACH_ELITELTE_CHN_OPEN),y)
                dtb-y += msm8917-sec-elitelte-chn-r00.dtb
		dtb-y += msm8917-sec-elitelte-chn-r01.dtb
		dtb-y += msm8917-sec-elitelte-chn-r02.dtb
		dtb-y += msm8917-sec-elitelte-chn-r03.dtb
        endif
endif

ifeq ($(CONFIG_SEC_J3LLTE_PROJECT),y)
        ifeq ($(CONFIG_MACH_J3LLTE_USA_SPR),y)
                dtb-y += msm8917-sec-j3llte-usa-spr-r00.dtb
        endif
endif

ifeq ($(CONFIG_SEC_J3POPLTE_PROJECT),y)
        ifeq ($(CONFIG_MACH_J3POPLTE_USA_SPR),y)
                dtb-y += msm8917-sec-j3poplte-usa-spr-r00.dtb
                dtb-y += msm8917-sec-j3poplte-usa-spr-r01.dtb
                dtb-y += msm8917-sec-j3poplte-usa-spr-r03.dtb
        endif

        ifeq ($(CONFIG_MACH_J3POPLTE_USA_USC),y)
                dtb-y += msm8917-sec-j3poplte-usa-usc-r05.dtb
                dtb-y += msm8917-sec-j3poplte-usa-usc-r06.dtb
        endif

        ifeq ($(CONFIG_MACH_J3POPLTE_USA_VZW),y)
                dtb-y += msm8917-sec-j3poplte-usa-vzw-r06.dtb
        endif
endif

ifeq ($(CONFIG_SEC_ON5XLLTE_PROJECT),y)
        ifeq ($(CONFIG_MACH_ON5XLLTE_CHN_OPEN),y)
                dtb-y += msm8917-sec-on5xllte-chn-r00.dtb
                dtb-y += msm8917-sec-on5xllte-chn-r01.dtb
                dtb-y += msm8917-sec-on5xllte-chn-r02.dtb
        endif
endif


echo '*** Warning: Samsung $@ Device Tree MSM8917.'
DTB_NAMES := $(subst $\",,$(CONFIG_BUILD_ARM_APPENDED_DTB_IMAGE_NAMES))
ifneq ($(DTB_NAMES),)
DTB_LIST := $(addsuffix .dtb,$(DTB_NAMES))
else
DTB_LIST := $(dtb-y)
endif

targets += dtbs
targets += $(addprefix ../, $(DTB_LIST))
endif

$(obj)/../../%.dtb: $(src)/%.dts FORCE
	$(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/../../,$(DTB_LIST))

clean-files := *.dtb *.reverse.dts


