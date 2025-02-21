<p align="center">
  <a href="https://github.com/acidanthera/OpenCorePkg">
    <img src="https://raw.githubusercontent.com/acidanthera/OpenCorePkg/master/Docs/Logos/OpenCore_with_text_Small.png" alt="logo" height="80">
  </a>
</p>

<p align="center">
  <strong>Opencore 1.0.0</strong>  
</p>
<br>


> ⚠️ **Warning:** This EFI only supports **OpenCore** and will **not support Clover bootloader**.



### **📝 MacOS BigSur Hackintosh**
![](/Docs/Image.jpg)
I assume you already have a copy of the OS image. If not, click [here](/Docs/DiskImage.md) for instructions on flashing a copy of macOS Big Sur onto a USB drive. Kindly note this does not reflect the original performance of a Mac, and all rights are owned by Apple Inc.

### **🖥 Hardware**
- **CPU:** QuadCore Intel Core i5-8265U, 3900 MHz (39 x 100)  
- **Chipset:** Intel Cannon Point-LP, Intel Whiskey Lake-U  
- **GPU:** Intel UHD Graphics 620 (1 GB)  
- **Audio Chipset:** Intel Cannon Point-LP PCH - cAVS (Audio, Voice, Speech) [D0]  
- **Wi-Fi:** Intel Wireless-AC 9560 802.11 ac Dual Band 2x2  
- ~~**GPU**: NVIDIA GeForce GTX MX250 (Not Supported)~~  
- **Storage 1:** HGST HTS541010A7E830 HDD  
- **Storage 2:** Micron 1100 SATA M.2 SSD  
- **Display:** Touchscreen Generic PnP Monitor  
- **Battery:** Original HP Battery (**Removed**)  
<br>

> ⚠️ **Warning:** Carefully review the **underlined** specifications above and compare them with your hardware.  
> If even a single spec does not match, **avoid using this EFI**, as it will simply not work.



### **📋 Compatibility**
| Feature           | Status     | Notes |
|------------------|-----------|--------------------------------|
| **Mac**          | ✅ Works  | MacOS BigSur |
| **CPU**          | ✅ Works  | Fully functional with power management |
| **NVIDEA**          | ❌ Not Working | Only handfull of cards work with Hackintosh |
| **Wi-Fi**        | ✅ Works | RealtekRTL8111.kext Works |
| **Bluetooth**    | ✅ Works  | IntelBluetoothFirmware.kext works |
| **Audio**        | ✅ Works  | Requires AppleALC |
| **Sleep/Wake**   |  🟡 Not Tested | -- |
| **USB Ports**    | ⚠️ Partial | Needs USB mapping for full functionality |
| **iServices/AirDrop** | 🟡 Not Tested | Requires proper SMBIOS configuration |
| **SD CARD** | ❌ Not Working | SD Cards are not yet supported |
| **Internal Microphone** | ✅ Works | Works with AppleALC |
| **Storage** | ✅ Works | Works with an SATA drive |
| **Touchpad/Keyboard** | ✅ Works | Works with VoodooPS2 and PS/2 |
| **Touchscreen** | ✅ Works | Works with Voodoo2C |
| **3.5mm Jack** | 🟡 Not Tested | -- |
| **HDMI** | 🟡 Not Tested | -- |
| **Ethernet/RJ45** | ✅ Works | -- |
| **Brightness Hotkeys** | ✅ Works | BrightnessKeys kexts |
| **Webcam** | ✅ Works | BrightnessKeys kexts |
| **Keyboard Backlight** | ✅ Works | SSDT-PNLF ACPI |

### **🖥️ BIOS Setup**
- Change the storage controller from SATA -> AHCI. Since there is no option to change them, its assumed the default controller uses AHCI
- Turn off Secure Boot
- Turn off TPM
- Turn on Virtualization/VT-x 
- Turn on Fan Always On
- Legacy boot or BIOS boot is **strictly** not supported
- Use UEFI boot

### **🗐 Credits & Documentation**
#### **🗂️ Resources**
- [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) - A Well Documented Guide
- [Olarila Hackintosh](https://olarila.com/) - Prebuilt OS image files
- [OpenCore](https://github.com/acidanthera/OpenCorePkg) - Bootloader for dynamic kernel module injections
#### **🧰 Tools**
- [ProperTree](https://github.com/corpnewt/ProperTree) - GUI editor for editing `plist` based files
- [GetSMBIOS](https://github.com/corpnewt/GenSMBIOS) - Generates serial numbers for macOS
- [Hackintool](https://github.com/benbaker76/Hackintool) - Swiss army knife of vanilla hackintoshing
- [OCAuxilary](https://github.com/ic005k/OCAuxiliaryTools) - Complete GUI client for `config.plist` modification
- [ESP Mounter Pro](https://www.insanelymac.com/forum/files/file/566-esp-mounter-pro/) - Tool to mount ESP onto MacOS
#### **📂 Kexts**
- [Lilu](https://github.com/ic005k/OCAuxiliaryTools) - MacOS Essencial patch
- [WhateverGreen](https://github.com/acidanthera/WhateverGreen/) - Graphics Fixes
- [AppleALC](https://github.com/acidanthera/AppleALC) - MacOS audio support
- [VirtualSMC](https://github.com/acidanthera/VirtualSMC) - SMC Firmware for Apple
- [IntelMausi](https://github.com/acidanthera/IntelMausi) - Support for Intel WiFi chipset
- [Airportltlwm](https://github.com/OpenIntelWireless/itlwm) - Enables WiFi and Bluetooth Support

