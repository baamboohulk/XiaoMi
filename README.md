# How to flash MIUI Fastboot ROM from Linux 

- Download the fastboot ROM suitable for your device from the [MIUI](https://xiaomifirmwareupdater.com/) and extract the downloaded archive

- Download and extract the [Android SDK Platform Tools](https://developer.android.com/studio/releases/platform-tools.html)

- Make sure ``adb`` and ``fastboot`` (components of platform-tools) are in your
  path

    `$ export PATH=path/to/android/sdk/platform-tools:$PATH`

- Connect your device to your computer using a USB cable and enable *USB
  Debugging* in your device's settings. Check if your device is detected.

    `$ adb devices`

- If device is listed, reboot to bootloader

    `$ adb reboot bootloader`

- Check if your device is detected by fastboot

    `$ fastboot devices`

- You may need to use ``sudo`` before ``fastboot`` if you get a permission denied
  error

- There are two scripts for flashing the ROM:

  1. ``flash_all.sh`` - Flash ROM and erase user data
    
  2. ``flash_all_except_data_storage.sh`` - Flash ROM without erasing user data
  
- Whichever script you decide to use, make sure that the interpreter is
  mentioned at the top of the script like

    `#!/bin/sh`

- If the above line is missing, add it to the top of the script

- Make the script executable (I've chosen ``flash_all.sh``)

    `$ cd path/to/extracted/ROM/archive`
    `$ chmod a+x ./flash_all.sh`

- Run the script

    `$ ./flash_all.sh`

- You may need to run ``sudo ./flash_all.sh`` if you had to use ``sudo`` with ``fastboot``

- Sit back and relax. The script needs no user interaction. After flashing the
  ROM, the script will reboot your device.

- Reboot will take quite a bit of time. Don't panic.


