# Hackintosh ASUS TUF H370-Pro Gaming + Intel Core i7-8700 + Gigabyte AMD Radeon RX 580 4GB
EFI folder used on my _ASUS TUF H370-Pro Gaming_ Hackintosh build (Vanilla), running macOS Catalina 10.15.x

--------------------------------------------------------------------------------------------

## Hardware Specs

- [x] <b>Board</b>: [ASUS TUF H370-Pro Gaming](https://www.asus.com/Motherboards/TUF-H370-PRO-GAMING-WI-FI/)
- [x] <b>CPU</b>: Intel Core i7-8700 @ 3.2GHz
- [x] <b>GPU</b>: [Gigabyte AMD Radeon RX 580 4GB](https://www.gigabyte.com/Graphics-Card/GV-RX580GAMING-4GD-rev-10-11)
- [x] <b>RAM</b>: 32GB DDR4 @ 3000MHz Corsair
- [x] <b>SSD</b>: NVMe PCIe M.2 Crucial 1TB
- [x] <b>SSD</b>: SATA SSD Crucial 1TB
- [x] <b>Wifi/Bluetooth</b>: [Fenvi FV-T919 Broadcom BCM94360CD](https://www.aliexpress.com/item/32778371977.html)

--------------------------------------------------------------------------------------------

## config.plist
You will need to generate your own values in the config.plist for the following vars:
- RtVariables -> MLB
- SMBIOS -> BoardSerialNumber
- SMBIOS -> SerialNumber
- SMBIOS -> SmUUID

--------------------------------------------------------------------------------------------

## Extras
The folder Extras contains a copy of the motherboard settings exported from the same UEFI/BIOS configuration utility.
You can use that file (CMO) to import the settings from an USB drive while in the UEFI/BIOS configuration, inside Tools (in Advanced Mode).

UEFI/BIOS version: 1502

It also contains a copy of the SSDT-UIAC-ALL.dsl used to compile the ACPI patch for Clover to enable all USB ports in without the need of patching everytime Apple releases an update. Many thanks to [RehabMan](https://www.tonymacx86.com/threads/guide-creating-a-custom-ssdt-for-usbinjectall-kext.211311/) and [UtterDisbelief](https://www.tonymacx86.com/threads/a-beginners-guide-to-creating-a-custom-usb-ssdt.272505/) for the guides they put together.

Open Extras/SSDT-UIAC-ALL.dsl and see the comments to know what ports are enabled.

--------------------------------------------------------------------------------------------

## More info
At my blog: [It's about Attitude](https://itsaboutactitud.wordpress.com/2019/09/03/hackintosh-2019/) (Spanish only).

--------------------------------------------------------------------------------------------

## Questions?.
Reach me at [Twitter](https://twitter.com/TCattd/) or by e-mail: esteban (at) attitude.cl

--------------------------------------------------------------------------------------------

## Changelog
### 2019-10-30
* Updated to macOS Catalina 10.15.1 (19B88)

### 2019-10-18
* Added a custom SSDT-UIAC-ALL.aml ACPI patch to enable all USB ports.

### 2019-10-13
* macOS Mojave Vanilla Installation. [Use this guide](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/) to prepare your USB Installer.

### 2019-09-04
* Added UEFI/BIOS settings.

### 2019-09-03
* Initial release for macOS Mojave 10.14.x
