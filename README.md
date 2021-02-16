# YU-ACE-YU5014-twrp-3.3.1-0
Team Win Recovery Project (TWRP) is an open-source software custom recovery image for Android-based devices. It provides a touchscreen-enabled interface that allows users to install third-party firmware and back up the current system which are functions often unsupported by stock recovery images. It is, therefore, often installed when flashing, installing, or rooting Android devices, although it isn't dependent on a device being rooted prior to installation.

In my view you have already enabled Developer Options and unlocked bootloader. Also you have ADB drivers installed.

Note: This is not a port and the recovery is built from Omni Source. So you will not faces any issues (atmost). Everything you do to your smartphone is your responsibility and we (and I) are here to help you. Follow instructions properly to customize your device.

OEM Unlock

1. First enable OEM Unlock available in the developer settings.
2. Install ADB drivers and use this command to enter into fastboot mode.
Code:
adb reboot bootloader
or
use Power + Volume Down buttons after shutdown/power off. Then choose fastboot mode with volume keys as navigation.​

3. Use the below command to unlock OEM.
Code:
fastboot oem unlock
4. For flashing TWRP go on reading.

Before flashing twrp you have to flash patched boot.img from fastboot

Download patched boot.img:

http://www.mediafire.com/file/i6p2h9le6ugrsaf/yu5014_patched_boot.img/file

1. Download the patched boot.img. Open Command Prompt (CMD) or Terminal and connect your mobile to PC using USB cable.
2. Enable USB Debugging, then type the below command and hit enter.
Code:
adb reboot bootloader
3. Use the below command if your device is recognized in the fastboot mode by issuing below command:
Code:
fastboot devices
If your device is not recognized then disconnect and reconnect the cable properly.
4. Now flash the img file you have downloaded from the link above and it is named as boot.img, use below command.
Code:
fastboot flash boot boot.img
5. It takes few seconds to flash and after that you can reboot device by using below command.
Code: fastboot reboot

Download twrp:

http://www.mediafire.com/file/084soinjq8t72n2/yu5014_TWRP_recovery.img/file

Instructions:

1. Download the Unofficial TWRP. Open Command Prompt (CMD) or Terminal and connect your mobile to PC using USB cable.
2. Enable USB Debugging, then type the below command and hit enter.
Code:
adb reboot bootloader
3. Use the below command if your device is recognized in the fastboot mode by issuing below command:
Code:
fastboot devices
If your device is not recognized then disconnect and reconnect the cable properly.
4. Now flash the img file you have downloaded from the link above and it is named as TWRP_recovery.img, use below command.
Code:
fastboot flash recovery TWRP_recovery.img
5. It takes few seconds to flash and after that you can enter Recovery mode by using below command.
Code:
fastboot oem reboot-recovery
6. It takes 5 - 10 sec at TWRP main screen and you need not worry about that.
7. TWRP will ask for Decryption password. Tap on cancel.

If TWRP ask for a decryption password then you have to open wipe option in twrp and click on format and type YES and enter
After that your device will be formatted and your encryption will be removed and after that you have to flash 2 zip files. 1 zip file will work other file may not so you have to try both file.
*After downloading zip files save them into sd card so you can flash from twrp.
Zip files link:-
http://www.mediafire.com/file/ftc74dpvbtdtdsh/Disable-Force-Encryption-Treble.zip/file
http://www.mediafire.com/file/gktg25ay2ksvycc/no-verity-opt-encrypt-6.1.zip/file
