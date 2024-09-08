# Lenovo ThinkCentre M910x OpenCore

## My Configuration

|         Hardware       |                   Model                  | 
|-------------------:|:----------------------------------------|
|          Motherboard | Lenovo ThinkCentre M910x                       |
|                CPU | Intel Xeon E-2268M                     |
|           Graphics Card | UHD P630   |
|              SSD 1 | SSD 256GB SSTC Oceanic Whitetip NVMe                  |
|               RAM 1 | Hynix DDR4 3200Mhz 16G  |
|               RAM 2 | Samsung DDR4 3200Mhz 8G  |
|        Wireless + Bluetooth | Intel® Dual Band Wireless-AC 8265    |

## OpenCore
OpenCore-1.0.1-RELEASE

### Driver
- OpenCanopy.efi
- OpenHfsPlus.efi
- OpenRuntime.efi
- ResetNvramEntry.efi
### Kext
- AppleALC.kext
- BlueToolFixup.kext
- IntelBluetoothFirmware.kext
- IntelBTPatcher.kext
- IntelMausi.kext
- itlwm.kext
- Lilu.kext
- NVMeFix.kext
- RestrictEvents.kext
- SMCProcessor.kext
- SMCSuperIO.kext
- USBMap.kext
- VirtualSMC.kext
- WhateverGreen.kext
- XHCI-unsupported.kext

## Status
### Working
Possibly everything
### Not Working
You tell me

## Quick Guide
1. Use GenSMBIOS to Gen iMac19,1 SMBIOS
2. Replace USBMap.kext with your own
3. Open config.plist and adjust it to your information
4. Remember to install HeliPort.dmg for Wifi & Internet
5. Black screen? Try to remove all debug symbols, trust me, it'll work!

## TODO
1. Replace itlwm.kext and HeliPort.dmg with AirportItlwm.kext
2. Replace OpenHfsPlus.efi with HfsPlus.efi?
3. Refine ACPI for better compatibility with my machine
4. Investigate why adding -v and debug options results in a black screen or boot failure - currently booting into macOS without knowing if there are any errors
5. Consider upgrading to a dGPU like RX460 or RX560, and test if the machine can boot with it
6. Replace the temporary 8GB RAM stick with a proper 16GB DDR4
7. Upgrade to a more suitable SSD instead of the current experimental one