# android_kernel_samsung_j7poplte_usa_spr
Kernel Source for Sprint Samsung Galaxy J7 Perx / SMJ727P
=================================

I've listed both the Snapdragon 625 and 626 in the specs. The 625 is supposed to be capped at 2.0Ghz, and the 626 (MSM8953Pro) was released specifically with an increase of frequency to 2.2Ghz, so it seems like this is actually using the 626/MSM8953Pro chip. But other than the slight clock increase, it seems exactly the same spec wise, and in the source it is definitely listed as the 625.


Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-Core 2.2Ghz GHz Cortex-A53
CHIPSET | Qualcomm Technologies Inc MSM8953/MSM8953Pro? Snapdragon 625/626?
GPU     | Adreno (TM) 506
Memory  | 2GB RAM
Android | 7.0
Storage | 8/16 GB
MicroSD | Up to 128GB
Battery | 3300 mAh
Display | 5.5", 720 x 1280 pixels, 267 ppi, Technology: TFT
Screen Mirroring | Wireless screen share
Selfie Camera  | 5 MP, 2576 x 1932 pixels, autofocus, LED flash
Rear Camera  | 8 MP,  4128 x 3096 pixels, autofocus, LED flash
Wireless | Pronto driver
NFC | No

Boot.img info                                                                                                            
Taken from J727PVPU1AQF5 (latest firmware)
-----------------------------------------------------------
Page size: 2048 (0x00000800)                                                                                     
Kernel size: 10987026 (0x00a7a612)                                            
Ramdisk size: 3745179 (0x0039259b)                                      
Second size: 0 (0x00000000)                                                         
Board name: SRPPI22A000KU                                                                           
Command line: 'console=null androidboot.hardware=qcom msm_rtb.filter=0x237 ehci-hcd.park=3 androidboot.bootdevice=7824900.sdhci     lpm_levels.sleep_disabled=1 androidboot.selinux=permissive'                                                                                 
Base address: (0x81dfff00)                                                                                              
