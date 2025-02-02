# Hackintosh - Asus Tuf Gaming B560M-Plus Wifi

# Current macOS 
macOS Big Sur 
Version 11.7.7

## Hardware components:

* ASUS TUF GAMING B560M-PLUS WIFI

  - Intel B560 Express Chipset: This chipset is responsible for communication between the processor and all the other components on the motherboard. The B560 chipset enables PCIe 4.0 and USB 3.2 Gen 2×2 (20 Gbps) support on the motherboard.

  - Realtek ALC897 8-Channel High Definition Audio CODEC: This chipset is responsible for the operation of the motherboard's built-in sound card. The ALC897 CODEC supports 192 kHz / 24-bit playback and features the Audio Boost function, which enhances audio quality for a better listening experience.
  
  - Realtek RTL8125B 2.5Gb Ethernet Controller: This chipset is responsible for the operation of the motherboard's built-in Ethernet port. The 2.5 Gb/s Ethernet controller enables faster internet connectivity and higher-speed data transfer over the local network.
  
  - Intel Wi-Fi 6 AX201 (802.11ax) Chipset: This chipset powers the motherboard's built-in Wi-Fi module, which supports the latest Wi-Fi standards like 802.11ax, MU-MIMO, and OFDMA.
  - Bluetooth 5.2 inside the wifi card.
  
* i5-11400
  - Intel® UHD Graphics 730
  
* Corsair Vengeance RGB PRO 32GB (2x16GB KIT)

* 2x WD Red SN700 NVMe 1 TB

## OpenCore EFI

Added version 0.9.0

## ACPI files

The uploaded files has been generated with [SSDTTime](https://github.com/corpnewt/SSDTTime) under Linux Live.

Howto(s):

  * https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-easy.html

  * https://christitus.com/opencore-mac/

## Kexts files

  * Lilu - This is a kext management framework that is necessary for the system to function properly and is a prerequisite for many other kexts.
  
  * VirtualSMC - This kext serves as an SMBIOS emulator for the system's motherboard and components, emulating Apple's original SMBIOS system.
  
  * WhateverGreen - This kext is responsible for supporting graphics cards and may be required to support the Intel integrated graphics controller on the motherboard.
  
  * AppleALC, AppleALCU - This kext is responsible for audio support on the motherboard. AppleALC supports motherboard audio cards and provides audio input and output functions.
  
  * FakePCIID - This is a kernel extension that provides fake identification information for various PCI devices. 
  
  * FakePCIID_Intel_HDMI_Audio - This is a companion extension specifically for Intel integrated HDMI audio. They allow certain unsupported hardware to be recognized and used by macOS.
  
  * LucyRTL8125Ethernet - This kext is responsible for network card support and may be required to support Ethernet controllers on the motherboard.

  * USBInjectAll - This kext is responsible for supporting USB ports and may be required to support USB ports on the motherboard.
  
  * NVMeFix.kext - This kext is an add-on file for macOS that improves the performance and stability of NVMe drives.
  
  * SMCProcessor - SMC ensures the reading and setting of data from hardware sensors and sensors (e.g. temperature, fan speed, battery status, etc.) through systems designed by Apple.
  
  * SMCSuperIO - This is an add-on kext for macOS that supports motherboard hardware such as motherboard circuit controllers (Super I/O). These controllers are responsible for controlling fans, temperature sensors, and LEDs on the front of the computer case.

### WIFI and Bluetooth kexts:

  * AirportItlwm and IntelBluetoothFirmware, IntelBluetoothInjector - These kexts are responsible for supporting the Wi-Fi and Bluetooth controllers and may be required to support the Intel Wi-Fi and Bluetooth controllers on the motherboard.

  * BlueToolFixup - this fixes firmware errors related to Apple Broadcom WiFi and Bluetooth cards that may occur with unsupported Wi-Fi and Bluetooth cards. kext improves AirDrop, Handoff and other features.

  * IntelBTPatcher - A Lilu base patcher that fix Intel Bluetooth on Bigsur, Catalina, Mojave, High sierra etc, tested with Bigsur and Catalina all working good.


## BIOS setup

  * X.M.P.: Enabled
  * Intel Rapid Storage Technology: Off
  * AI Overclock Tuner: XMP II
  * Intel VMX Virtualization Technology: Enabled
  * Hyper-Threading: Enabled
  * VT-d: Enabled
  * Primary Display: Auto
  * iGPU: Enabled
  * DVMT Pre-Allocated: 1024
  * SATA Mode Selection: AHCI
  * Re-Size BAR Support: Enabled
  * SR-IOV Support: Enabled
  * XHCI Hand-off: Enabled
  * Serial port: Disabled
  * Secure Boot: Other OS
  * Secure Boot Mode: Custom
  * Clear Secure Boot Keys: YES
  * Fast Boot: Disabled
  * Boot Sector Recovery Policy: Auto Recovery (Follow UEFI Rules)


## Good and Bad

  :thumbsup: Audio: OK
  :thumbsup: WIFI: OK (stable with the original Intel wifi)
  :thumbsup: BT: OK
  :thumbsup: Handoff: Not tested
  :thumbsup: Airdrop: NOK

## WARNING!

Do not forget to edit the PlatformInfo section of config.plist!

## Screenshots

![Screenshot1](screenshots/Screenshot1.png)
![Screenshot2](screenshots/Screenshot2.png)
