# twrp_device_xiaomi_lake
 The TWRP device tree for Redmi 14C/POCO C75/Redmi A3 Pro(lake/pond)  
 Based on HyperOS 1.0.1.0.UGTMIXM, device tree port from negroweed/device_xiaomi_gold_recovery  
 You should flash the original venodr_boot image from official fastboot package and install 
 current TWRP ramdisk to boot partition after entering TWRP main screen. Otherwise the system won't boot normally.  
 Bugs:  
 touch screen, data decryption(stuck on TWRP logo), fastbootd mode, all buttons in the interface are very slow to click.     
 Works:  
 ADB, sideload and local zips flashing, SD card and internal storage(without encryption),   
 mounting all of the partitions, USB OTG.  
 Build Steps:  
 repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1  
 repo sync  
 git clone -b alpha_20250224 https://github.com/lpxx50117/twrp_device_xiaomi_lake.git device/xiaomi/lake  
 . build/envsetup.sh  
 lunch twrp_lake-userdebug  
 mka vendorbootimage
