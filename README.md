# z6lite
Tutorial for Lenovo Z6 Lite

# IF YOU HAVE GPS LOCK PROBLEMS LENOVO RECOMENDS TO CHANGE ROM TO 11.0.049

# DOWNLOAD ROM
# INCLUDES DRIVERS / QPST / ROM
https://yadi.sk/d/9drVdFo7rQtfOw?spm=5261.im.0.0.c9833e5fV9s3si

# DOWNLOAD ADB & FASTBOOT
https://developer.android.com/studio/releases/platform-tools.html?hl=es-419

# ENABLE USB DEBUGGING
SETTINGS -> GENERAL SETTINGS -> DEVELOPER OPTIONS -> Turn on USB DEBUGGING

# INSTALL QPST
~/Tools/QPST/QPST.2.7.460.exe

# OPEN QFIL PROGRAM
# SELECT FLAT BUILD
# SELECT PROGRAMMER PATH
~/images\prog_emmc_firehose_sdm670_ddr.elf

# LOAD XMLs
rawprogram0.xml & patch0.xml

# IF THE PHONE IS NOT RECOGNISED THE DOWNLOAD BUTTON WILL BE UNAVAILABLE. DON'T PANIC WE FORCE IT RESTARTING EDL ON NEXT STEP

# OPEN CMD AS ADMIN
# GO TO ADB PATH

# REBOOT EDL
# SCREEN PHONE GONNE BLACK BUT QFIL NOW CAN CONNECT TO PHONE
abs reobot edl

# FLASH ROM USING QFIL
Press "Download"

# YOUR PHONE HAVE NOW A NEW ROOM

----------------------

# HOW TO UNLOCK YOUR PHONE BOOTLOADER

# GET UNLOCK IMAGE
# YOU NEED PHONE IMEI AND SERIAL NUMBER
https://www.zui.com/iunlock

# UPDATE UNLOCK IMAGE
fastboot flash unlock ${IMAGE_FILE}

# UNLOCK
fastboot oem unlock-go

----------------------

# HOW TO LOCK YOUR PHONE BOOTLOADER

# REBOOT
adb reboot bootloader

# LOCK
fastboot flashing lock
