# amlogic-s9xxx kernel related files

Some files needed for compilation related to amlogic-s9xxx kernel are stored in the directory.

## amlogic-armbian

General file storage directory, such as [boot and firmware](https://github.com/ophub/amlogic-s9xxx-openwrt/tree/main/amlogic-s9xxx/amlogic-armbian) related.

## amlogic-dtb

For more OpenWrt firmware .dtb files are in the [amlogic-dtb](https://github.com/ophub/amlogic-s9xxx-openwrt/tree/main/amlogic-s9xxx/amlogic-dtb) directory.  When writing into EMMC through [openwrt-install](https://github.com/ophub/amlogic-s9xxx-openwrt/blob/main/amlogic-s9xxx/install-program/files/openwrt-install), select 0: Enter the dtb file name of your box.

## amlogic-kernel

The amlogic-s9xxx [kernel](https://github.com/ophub/amlogic-s9xxx-openwrt/tree/main/amlogic-s9xxx/amlogic-kernel/kernel) storage directory, more kernels can be made through [build_kernel](https://github.com/ophub/amlogic-s9xxx-openwrt/tree/main/amlogic-s9xxx/amlogic-kernel/build_kernel). 

## amlogic-u-boot

The amlogic-s9xxx 5.10 kernel version currently does not support writing to EMMC and only supports starting and using in `TF/SD card`. When using the 5.10 kernel version, you need to copy the corresponding `u-boot-*.bin` file to `u-boot.ext` (TF/SD card boot file) and `u-boot.emmc` (EMMC boot file).

## common-files

- files: The files in the `files` directory are custom files, which must be completely consistent with the structure and file naming and storage under the ***`root`*** directory in openwrt. If there are files in this directory, they will be automatically copied to the openwrt directory during `sudo ./make`. E.g:
```yaml
etc/config/network
lib/u-boot
```
- patches: The files in the `patches` directory are patch files, which are integrated when build kernel files.

## install-program

Install openwrt to emmc for Amlogic S9xxx STB. Insert the `USB hard disk` with the written `OpenWrt` firmware. Log in to the default IP: 192.168.1.1 → `Login in to openwrt` → `system menu` → `TTYD terminal` → input command: 

- Install command: `openwrt-install`

[For more instructions please see: install-program](https://github.com/ophub/amlogic-s9xxx-openwrt/tree/main/amlogic-s9xxx/install-program)


## u-boot

The [u-boot](https://github.com/ophub/amlogic-s9xxx-openwrt/tree/main/amlogic-s9xxx/u-boot) storage directory contains the mainline boot files and non-mainline boot files. 
