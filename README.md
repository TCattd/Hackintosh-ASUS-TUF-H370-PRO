# Hackintosh ASUS TUF H370-Pro Gaming (WI-FI) + Intel Core i7-8700 + Gigabyte AMD Radeon RX 580 4GB
EFI folder used on my _ASUS TUF H370-Pro Gaming (WI-FI)_ Vanilla Hackintosh build, running macOS Catalina 10.15.x

--------------------------------------------------------------------------------------------

## Hardware Specs

- [x] <b>Board</b>: [ASUS TUF H370-Pro Gaming (WI-FI)](https://www.asus.com/Motherboards/TUF-H370-PRO-GAMING-WI-FI/)
- [x] <b>CPU</b>: [Intel Core i7-8700 Coffe Lake @ 3.2 GHz / 4.6 GHz](https://ark.intel.com/content/www/us/en/ark/products/126686/intel-core-i7-8700-processor-12m-cache-up-to-4-60-ghz.html)
- [x] <b>GPU</b>: [Gigabyte AMD Radeon RX 580 4GB](https://www.gigabyte.com/Graphics-Card/GV-RX580GAMING-4GD-rev-10-11)
- [x] <b>RAM</b>: [32GB DDR4 @ 3000MHz (16GB x2) Corsair](https://www.corsair.com/us/en/Categories/Products/Memory/VENGEANCE%C2%AE-LPX-16GB-%281-x-16GB%29-DDR4-DRAM-3000MHz-C16-Memory-Kit---Black/p/CMK16GX4M1D3000C16)
- [x] <b>SSD</b>: [NVMe PCIe M.2 Crucial 1TB](https://www.crucial.com/usa/en/CT1000P1SSD8)
- [x] <b>SSD</b>: [SATA SSD Crucial 1TB](https://www.crucial.com/usa/en/ct1000bx500ssd1)
- [x] <b>Wifi/Bluetooth</b>: [Fenvi FV-T919 Broadcom BCM94360CD](http://en.fenvi.com/en/brand_view.php?id=366)

--------------------------------------------------------------------------------------------

## How to
Use the [Hackintosh Vanilla Desktop Guide (Building the USB Installer)](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/building-the-usb-installer) to prepare your USB Flashdrive to install macOS.

Then mount the USB Flashdrive's EFI partition (with Clover Configurator or EFI Mounter) and use the EFI folder in this repo instead of following the rest of the guide.

--------------------------------------------------------------------------------------------

## config.plist
You will need to generate your own values in the config.plist for the following vars:
- RtVariables -> MLB
- SMBIOS -> BoardSerialNumber
- SMBIOS -> SerialNumber
- SMBIOS -> SmUUID

--------------------------------------------------------------------------------------------

## Extras
The folder Extras contains:

#### Motherboard settings
A copy of the motherboard settings exported from the same UEFI/BIOS configuration utility.
You can use that file (CMO) to import the settings from an USB drive while in the UEFI/BIOS configuration, inside Tools (in Advanced Mode).

Current UEFI/BIOS version: 1801

#### USB SSDT
It also contains a copy of the SSDT-UIAC-ALL.dsl used to compile the ACPI patch for Clover to enable all USB ports in without the need of patching everytime Apple releases an update. Many thanks to [RehabMan](https://www.tonymacx86.com/threads/guide-creating-a-custom-ssdt-for-usbinjectall-kext.211311/) and [UtterDisbelief](https://www.tonymacx86.com/threads/a-beginners-guide-to-creating-a-custom-usb-ssdt.272505/) for the guides they put together.

Open Extras/SSDT-UIAC-ALL.dsl and see the comments to know what ports are enabled.

#### EFI USB Install
A zip file, EFI-20190522-USB-Install-Minimal.zip, with a minimal EFI folder, meant to be used in the USB flash drive to install macOS. Just the bare minimum for it to run the installer in this Hackintosh configuration. Mainly tested with Mojave. Should work with Catalina (updated to use Clover 5093).

If the main EFI folder in the repo doesn't let you finish the installation, you can try to use this one in the USB Flashdrive Installer. Not for use in the final installation disk.

First try the main EFI folder (repo's root) to install Calatina, as i did when transitioning to a Vanilla Hackintosh.

--------------------------------------------------------------------------------------------

## More info
At my blog: [It's about Attitude](https://itsaboutactitud.wordpress.com/2019/09/03/hackintosh-2019/) (Spanish only).

--------------------------------------------------------------------------------------------

## Questions?
Reach me at [Twitter](https://twitter.com/TCattd/) or by e-mail: esteban (at) attitude.cl

--------------------------------------------------------------------------------------------

## Changelog
### 2020-03-25
* Updated to macOS Catalina 10.15.4 (19E266)

### 2020-01-29
* Updated to macOS Catalina 10.15.3 (19D76)

### 2019-12-27
* Updated UEFI BIOS firmware to 1801.

### 2019-12-13
* Updated to macOS Catalina 10.15.2 (19C57)

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
