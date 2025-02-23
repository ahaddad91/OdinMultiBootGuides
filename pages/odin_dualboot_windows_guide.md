# Windows Dual Boot Installation

## ⚠️ Warning ⚠️
This is **NOT** an official Windows port made by AYN. AYN will **NOT** provide support for this operating system and installing this may in fact VOID your warranty.

This is a community effort project, and thus we cannot guarantee no issues when attempting to install this port on your Odin.

Furthermore, this installation may brick your device. Do so at your own risk! We take no responsibility for hardbricked devices!

This will reset your device! Make sure to backup all files and configurations that you want to save!

It will also divide your available storage in half between the two operating systems. If you have a 128GB storage it will be 64GB/64GB and if you have a 256GB storage it will be 128GB/128GB.

## What you’ll need :

### Hardware :

- A Windows or Linux based computer (vm will work)
 
- An **Odin-Base** (4GB RAM with 64GB Storage) or an **Odin-Pro** (8GB RAM with 128GB or 256GB Storage) -> Odin 2 requires making a low level driver for Odin 2 to boot Windows in efi bootloader, and Windows driver for specific Odin 2 hardware.
- An 8GB or larger USB flash drive formatted to FAT32

- A USB-A to USB-C adapter to plug the flash drive into the C port of the Odin (if your drive doesn't have a USB-C connector)

### Prerequisite Software:

- [Google USB Driver](https://developer.android.com/studio/run/win-usb)

- [odin_custom_boot_1.0.3.7z](https://download.project-valhalla.com/custom_boot/odin_custom_boot_1.0.3.7z)

- [odin_windows_installer.7z](https://download.project-valhalla.com/custom_boot/odin_windows_installer.7z)

- Sensor Config Driver if you have **Model: Odin_M2** [qcSensorsConfig850-M2.zip](https://download.project-valhalla.com/custom_boot/qcSensorsConfig850-M2.zip)

- An [install.wim](https://www.microsoft.com/en-us/software-download/windows11arm64) click the link and download Windows 11 Arm64 in your preferred language.
  
- Mount the downloaded Windows 11 Arm64 ISO (right click the downloaded ISO file and click mount)

- Create a folder named "sources" at C:\, (or whatever letter drive your OS is installed on) If you don't know how, then open file explorer and double click This PC, then double click on the drive with the OS on it (Windows icon). Now make the folder named "sources".

- Press the windows key and type cmd then press enter. With the mounted ISO execute the following command (change the ISO drive letter (F:) if necessary):

Dism /Split-Image /ImageFile:F:\sources\install.wim /SWMFile:C:\sources\install.swm /FileSize:4000

- You now have two .swm files in C:\sources
install.swm install2.swm

- Copy the install.swm and install2.swm from C:\sources to USB\images\ (or delete the install.wim if you already did this with Project Valhalla instructions, and then copy over the two .swm files)

- In your USB stick, go to installer folder, open the install.cmd file with a text editor. In line 57 change /Index:1 to /Index:2, this is because Windows 11 Pro is Index 2 in the retail ISOs. If you skip this step you will install Windows Enterprise and will be able to login only with a corporate account.

Line 57:

From: dism /Apply-Image /ImageFile:%WinPESource%images\install.swm /SwmFile:%WinPESource%images\install*.swm /Index:1 /ApplyDir:w: /ScratchDir:w:\temp

To: dism /Apply-Image /ImageFile:%WinPESource%images\install.swm /SwmFile:%WinPESource%images\install*.swm /Index:2 /ApplyDir:w: /ScratchDir:w:\temp
ATTENTION: There are 2 lines that contain /Index:1 very close to eachother, its the second one, number 57

- Eject your USB and proceed to the installation

## Installation Steps:

1. [Preparing Windows Odin and Files](https://github.com/ahaddad91/OdinMultiBootGuides/blob/main/pages/preparing_windows_files.md)

2. [Installing Windows](https://github.com/ahaddad91/OdinMultiBootGuides/blob/main/pages/installing_windows.md)

*In case of error during windows installation (after plugging USB stick step) you don't need to start from scratch from QFIL, or repartition android/windows, just follow the steps carefully to prepare the USB stick again, insert it into your Odin and reboot. Installation will proceed as normal.

## GPU driver update:
[GPU driver update](https://github.com/ahaddad91/OdinMultiBootGuides/blob/main/pages/GPU%20driver%20update.md)

## Windowed mode fix:
[Windowed mode fix](https://github.com/ahaddad91/OdinMultiBootGuides/blob/main/pages/Windowed%20mode%20fix.md)

## Mandatory Tuning:
[Tuning](https://github.com/ahaddad91/OdinMultiBootGuides/blob/main/pages/Tuning.md)
