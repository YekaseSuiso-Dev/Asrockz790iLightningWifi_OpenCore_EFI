# Asrock z790i Lightning Wifi_OpenCore_EFI
- OpenCore 1.0.6
- MacOS 14.7.7 23H723
- CPU	8C+16c Intel Core i9-14900K, 5686 MHz (57 x 100)
- GPU AMD Radeon RX 5700 XT 8GB GDDR6
- Asrock z790i Lightning Wifi

## Kexts

- itlwm.kext
- AppleALC.kext
- BlueToolFixup.kext
- IntelBluetoothFirmware.kext
- Lilu.kext
- LucyRTL8125Ethernet.kext
- RestrictEvents.kext
- SMCProcessor.kext
- SMCSuperIO.kext
- USBToolBox.kext
- UTBMap.kext
- VirtualSMC.kext
- WhateverGreen.kext

## Quirks

Please do not attempt to upgrade to macOS 15. This configuration is suitable for "retirement" on macOS 14.7.7. Below are my test results on 14.7.7.

* Wireless network: Pass
* Sleep: Not tested
* Ethernet card: Pass
* Bluetooth: Pass
