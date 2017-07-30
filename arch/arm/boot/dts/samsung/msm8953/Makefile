# For J7POPLTE_USA_SPR
dtb-$(CONFIG_SEC_J7POPLTE_USA_SPR) += msm8953-sec-j7poplte_usa_spr-r00.dtb \
					msm8953-sec-j7poplte_usa_spr-r01.dtb \
					msm8953-sec-j7poplte_usa_spr-r02.dtb \
					msm8953-sec-j7poplte_usa_spr-r03.dtb \
					msm8953-sec-j7poplte_usa_spr-r04.dtb \
					msm8953-sec-j7poplte_usa_spr-r05.dtb

ifeq ($(CONFIG_ARM64),y)
always          := $(dtb-y)
subdir-y        := $(dts-dirs)
else
targets += dtbs
targets += $(addprefix ../, $(dtb-y))

$(obj)/../../%.dtb: $(src)/%.dts FORCE
        $(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/../../,$(dtb-y))
endif
clean-files := *.dtb *.reserve.dts
