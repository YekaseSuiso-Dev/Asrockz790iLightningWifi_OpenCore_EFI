<h1 align="center">
  <br>
  <img src="https://dortania.github.io/OpenCore-Install-Guide/dortania-logo-clear.png" alt="Hackintosh" width="200">
  <br>
  OpenCore EFI for Asrock z790i Lightning Wifi Hackintosh
  <br>
</h1>

<p align="center">
  <strong>A complete OpenCore EFI configuration for Asrock z790i Lightning Wifi systems</strong>
</p>
  
- OpenCore 1.0.6
- MacOS 14.7.7 23H723
- CPU	8C+16c Intel Core i9-14900K, 5686 MHz (57 x 100)
- GPU AMD Radeon RX 5700 XT 8GB GDDR6
- Asrock z790i Lightning Wifi

## Notes
- Add `-v` to boot args for verbose boot.
- During the installation process, please do not add Wi-Fi and Bluetooth drivers, as this will cause problems.
- Before installation, use “OCAT” to modify the spoof parameters to “MacPro7,1” and generate a serial number; otherwise, it will fail to boot!

## Kexts

- itlwm.kext
- AppleALC.kext
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
* Sleep: Pass
* Ethernet card: Pass
* Bluetooth: Pass

## Tips on Wi-Fi and Bluetooth:

1. Open https://dortania.github.io/OpenCore-Install-Guide/ktext.html#wifi-and-bluetooth
2. Download [AirportItlwm](https://github.com/OpenIntelWireless/itlwm/releases), [Itlwm](https://github.com/OpenIntelWireless/itlwm/releases), [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases).
3. Place into: /OC/Kexts
4. Check the [documentation](https://openintelwireless.github.io/itlwm/) and enjoy.

## BIOS Settings

### Enabled
| Setting                        | Where?                           |
| ------------------------------ | -------------------------------- |
| Above 4G Decoding              | Advanced \ Chipset Configuration |
| C.A.M. Clever Access Memory*   | Advanced \ Chipset Configuration |
| VT-d                           | Advanced \ Chipset Configuration |
| Intel Virtualization Techology | Advanced \ CPU Configuration     |
| SATA Mode Selection: AHCI      | Advanced \ Storage Configuration | 
| XHCI Hand-off                  | Advanced \ USB Configuration     |

\* Clever Access Memory refers to Resizable BAR

### Disabled
| Setting              | Where?                       |
| -------------------- | ---------------------------- |
| CFG Lock**           | Advanced \ CPU Configuration |
| CSM                  | Boot                         |
| Fast Boot            | Boot                         |
| Intel Platform Trust | Security                     |
| Secure Boot          | Security                     |

\** Can be found after enabling **CPU C States Support**.
