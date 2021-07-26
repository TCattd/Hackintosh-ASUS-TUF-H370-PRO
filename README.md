# Project no longer updated.
Check the [changelog](https://github.com/TCattd/Hackintosh-ASUS-TUF-H370-PRO/blob/master/CHANGELOG.md) to know the last update date.

Why?

Wrote about the change here: [Dev Enviroment: Fury Road](https://itsaboutactitud.wordpress.com/2021/07/03/dev-enviroment-fury-road/) (spanish only).


# Hackintosh ASUS TUF H370-Pro Gaming (WI-FI) + Intel Core i7-8700 + Gigabyte AMD Radeon RX 580 4GB
EFI folder used on my _ASUS TUF H370-Pro Gaming (WI-FI)_ Vanilla Hackintosh build, running macOS 11.x Big Sur

--------------------------------------------------------------------------------------------

## Hardware Specs

- [x] **Board**: [ASUS TUF H370-Pro Gaming (WI-FI)](https://www.asus.com/Motherboards/TUF-H370-PRO-GAMING-WI-FI/)
- [x] **CPU**: [Intel Core i7-8700 Coffe Lake @ 3.2 GHz / 4.6 GHz](https://ark.intel.com/content/www/us/en/ark/products/126686/intel-core-i7-8700-processor-12m-cache-up-to-4-60-ghz.html)
- [x] **GPU**: [Gigabyte AMD Radeon RX 580 4GB](https://www.gigabyte.com/Graphics-Card/GV-RX580GAMING-4GD-rev-10-11)
- [x] **RAM**: [32GB DDR4 @ 3000MHz (16GB x2) Corsair](https://www.corsair.com/us/en/Categories/Products/Memory/VENGEANCE%C2%AE-LPX-16GB-%281-x-16GB%29-DDR4-DRAM-3000MHz-C16-Memory-Kit---Black/p/CMK16GX4M1D3000C16)
- [x] **SSD**: [NVMe PCIe M.2 WD Blue SN550 1TB](https://shop.westerndigital.com/es-la/products/internal-drives/wd-blue-sn550-nvme-ssd#WDS100T2B0C)
- [x] **SSD**: [NVMe PCIe M.2 WD_Black SN750 1TB](https://shop.westerndigital.com/products/internal-drives/wd-black-sn750-nvme-ssd#WDS100T3X0C)
- [x] **Wifi/Bluetooth**: [Fenvi FV-T919 Broadcom BCM94360CD](http://en.fenvi.com/en/brand_view.php?id=366)

--------------------------------------------------------------------------------------------

## How to
Use the [OpenCore Install Guide (Creating the USB)](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) to prepare your USB flashdrive to install macOS.

Then mount the USB flashdrive's EFI partition (with [EFI Mounter](https://www.tonymacx86.com/resources/efi-mounter-v3-1.447/) or another way) and use the EFI folder in this repo instead of following the rest of the guide.

Don't forget to update and import the UEFI/BIOS settings provided in this repo **before** beginning the installation.

Keep in mind that for this EFI folder to properly boot and work, you need to have at least the same Motherboard, CPU and GPU that i have in my build. If you don't have those same three main specs as i do, you will have to do some edits to your OpenCore's config file. To know more, please, follow [Dortania's guide](https://dortania.github.io/OpenCore-Install-Guide/).

--------------------------------------------------------------------------------------------

## config.plist PlatformInfo
You will need to generate your own values in the config.plist for the following vars:

- Type: PlatformInfo -> Generic -> SystemProductName
- Serial: PlatformInfo -> Generic -> SystemSerialNumber
- Board Serial: PlatformInfo -> Generic -> MLB
- SmUUID: PlatformInfo -> Generic -> SystemUUID
- ROM or NIC MAC address: PlatformInfo -> Generic -> ROM

Follow the instructions at the [OpenCore Install Guide (Configs -> Coffe Lake -> PlatformInfo)](https://dortania.github.io/OpenCore-Install-Guide/config.plist/coffee-lake.html#platforminfo) on how to proceed with that. Although it is not mandatory, it's highly recommended to use [ProperTree](https://github.com/corpnewt/ProperTree) to edit your config.plist

--------------------------------------------------------------------------------------------

## Extras
The folder Extras contains:

#### Motherboard settings
A copy of the motherboard settings exported from the same UEFI/BIOS configuration utility.
You can use that file (CMO) to import the settings from an USB drive while in the UEFI/BIOS configuration, inside Tools (in Advanced Mode).

Current UEFI/BIOS version: 2301

#### Legacy Clover EFI
The latest working EFI based on Clover, used before migrating to OpenCore.
You can still use it if you want. Just follow the [Hackintosh Vanilla Desktop Guide (Building the USB Installer)](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/building-the-usb-installer) to prepare your USB Flashdrive to install macOS, and use this EFI folder instead.

You will need to generate your own values in the config.plist for the following vars:
- RtVariables -> MLB
- SMBIOS -> BoardSerialNumber
- SMBIOS -> SerialNumber
- SMBIOS -> SmUUID

Be warned: this Clover based EFI folder will not be updated anymore by me.

#### Legacy Clover SSDT
Folder contains a copy of the SSDT-UIAC-ALL.dsl used to compile the ACPI patch for Clover to enable all USB ports in without the need of patching everytime Apple releases an update. Many thanks to [RehabMan](https://www.tonymacx86.com/threads/guide-creating-a-custom-ssdt-for-usbinjectall-kext.211311/) and [UtterDisbelief](https://www.tonymacx86.com/threads/a-beginners-guide-to-creating-a-custom-usb-ssdt.272505/) for the guides they put together.

Open Extras/SSDT-UIAC-ALL.dsl and see the comments to know what ports are enabled.

It also contains all other .dsl files used for generating the .aml ACPI patches included in the EFI folder.

SSDT not used on OpenCore. Not needed. OpenCore uses a kext to map the USB ports.

--------------------------------------------------------------------------------------------

## More info
At my blog: [It's about attitude](https://itsaboutactitud.wordpress.com/2019/09/03/hackintosh-2019/) (Spanish only).

--------------------------------------------------------------------------------------------

## Questions?
Reach me at [Twitter](https://twitter.com/TCattd/) or by e-mail: esteban (at) attitude.cl

--------------------------------------------------------------------------------------------

## Changelog
[Changelog available here](https://github.com/TCattd/Hackintosh-ASUS-TUF-H370-PRO/blob/master/CHANGELOG.md).
