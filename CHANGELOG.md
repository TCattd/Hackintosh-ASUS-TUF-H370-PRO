# Changelog
## 2021-02-04
* Updated OpenCore to 0.6.6

## 2021-02-02
* Updated to macOS 11.2 Big Sur (20D64)

## 2021-01-07
* Updated OpenCore to 0.6.5

## 2020-12-16
* Updated to macOS 11.1 Big Sur (20C69)
* Updated OpenCore to 0.6.4

## 2020-11-22
* Updated to macOS 11.0.1 Big Sur (120B29)

## 2020-10-06
* Updated OpenCore to 0.6.3

## 2020-10-06
* Updated OpenCore to 0.6.2
* Updated UEFI BIOS firmware to 2301

## 2020-09-14
* Updated OpenCore to 0.6.1

## 2020-08-11
* Updated UEFI BIOS firmware to 2002

## 2020-08-10
* Updated OpenCore to 0.6.0

## 2020-07-15
* Updated to macOS Catalina 10.15.6 (19G73).
* Removed unnecessary kexts, as this build is using a Fenvi Wifi-Bluetooth combo card and, [according dortania](https://dortania.github.io/Wireless-Buyers-Guide/Kext.html), those removed kexts aren't needed when using a Fenvi card.

## 2020-06-08
* Configured and added a proper [USB Mapping](https://dortania.github.io/USB-Map-Guide/) kext.

## 2020-06-01
* Updated OpenCore to 0.5.9
* Added FileVault support.
* Updated Kexts.
* Updated to macOS Catalina 10.15.5 (19F101).

## 2020-05-25
* Updated UEFI BIOS firmware to 1901.

## 2020-05-22
* Removed XhciPortLimit patch. Not needed, because we already have a working ACPI patch for our USB ports (SSDT-UIAC-ALL.aml).
* Cleaned up the EFI/OC/Resources/Audio folder for freeing some space. Just one wav needed for the boot-chime, [as described here](https://dortania.github.io/OpenCore-Desktop-Guide/extras/gui.html#setting-up-a-boot-chime).

## 2020-05-17
* Migrated from Clover to OpenCore 0.5.8. New EFI folder should be a quickly and fully replaceable, if you performed a Vanilla macOS installation before and always maintained SIP enabled (did no system modifications at all). Just mind the PlatformInfo part at the README.md. You can re-use your old Clover generated values there too.

## 2020-04-11
* Added EmuVariableUefi.efi for [issue 2](https://github.com/TCattd/Hackintosh-ASUS-TUF-H370-PRO/issues/2) (Thanks @bricco1981).
* Updated to macOS Catalina 10.15.4 (19E287).

## 2020-03-25
* Updated to macOS Catalina 10.15.4 (19E266).

## 2020-01-29
* Updated to macOS Catalina 10.15.3 (19D76).

## 2019-12-27
* Updated UEFI BIOS firmware to 1801.

## 2019-12-13
* Updated to macOS Catalina 10.15.2 (19C57).

## 2019-10-30
* Updated to macOS Catalina 10.15.1 (19B88).

## 2019-10-18
* Added a custom SSDT-UIAC-ALL.aml ACPI patch to enable all USB ports.

## 2019-10-13
* macOS Mojave Vanilla Installation. [Use this guide](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/) to prepare your USB Installer.

## 2019-09-04
* Added UEFI/BIOS settings.

## 2019-09-03
* Initial release for macOS Mojave 10.14.x.
