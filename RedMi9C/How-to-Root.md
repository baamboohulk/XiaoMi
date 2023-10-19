# How to Root Redmi9C 

### I am not responsible for your actions, but I will try to help.
### I'm going to assume you have unlocked bootloader and ADB/Fastboot tools installed.

- [Download](https://github.com/topjohnwu/Magisk/releases) latest Magisk and make 2 copies of it. Install one of them on your phone. Change the extension of 2nd from `.apk` to `.zip`, then move it to your phone`s storage

- [Download](https://sourceforge.net/projects/wulan17/files/Angelica/PBRP/) Pitch Black recovery for Redmi 9C

- Move recovery.img to both your ADB folder (can be found at C:\adb) and phone`s storage

- [Download](https://zackptg5.com/android.php#disverfe) DM-VERITY, FORCED ENCRYPTION

- ~~Rename it to `enfec.zip` and place in phone`s storage~~

- Download attached [vbmeta.img](https://forum.xda-developers.com/attachments/vbmeta-img.5257631/) and place it in your ADB folder

- Go into fastboot mode

- On your PC, open cmd-here.exe in adb folder

- `fastboot flash recovery recovery.img`

- `fastboot flash vbmeta vbmeta.img`

- `fastboot reboot recovery`

- Sometimes recoveries don't work with touchscreen. In this case, flash other region's ROM. To do this, find and download fastboot version of ROM. Unzip it, run `flash_all.bat` while being in a fastboot mode (this will erase all data). WARNING: DO NOT RUN `flash_all_and_lock.bat`. THIS WILL LOCK THE BOOTLOADER AND YOU WILL HAVE TO WAIT ANOTHER WEEK!
Next retry again the whole tutorial. You can also use USB-OTG mouse.

- Navigate to 'Install' section. Check every option except 'Reboot after installation is complete', 'Zip signature verification' and 'Advanced remove of Forced Encryption'. Select recovery image that you previously moved to your storage and install it 'as Recovery'.

- In recovery, move to 'backup' and make a backup to your SD card (optional, but highly recommended). Usually, it doesn`t work out of the box. Try searching for guides.

- In the same section install ~~enfec.zip and then~~ Magisk.zip. If you get errors like 'Failed to mount /nv_data', ignore them.

- Reboot to system, copy external_sd/PBRB/tools -> storage/0/emulated/PBRB/

Done!

