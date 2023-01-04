# [OpenCore](https://github.com/acidanthera/OpenCorePkg) EFI Build

A manually assembled build for installing Hackintosh on my laptop. Saved for future experiments.
[Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

Special thanks to [Rin](https://github.com/honeymiko) for her support with Hackintosh install.

**OpenCore Version:** 0.8.0

# Completed to working

- QE/CI of Intel HD 4400
- Audio
- Power Management
- Ethernet
- All USB Ports
- HDMI Video
- Touchpad
- Battery Indicator
- Brightness
- WiFi (Some troubles/sometimes bad speed)

# Not working

- Bluetooth (i'm don't need this work)
- Airdrop

# TODO

- Make an OTA update to Big Sur
- Fix Bluetooth

# Computer specifications

Component | Model
--- | ---
Laptop | Asus Vivobook Q301LA
CPU | Intel Core i5-4200U
iGPU | Intel HD Graphics 4400
Audio Chipset | ALC3236 (ALC233)
Ethernet | Realtek RTL8111 Gigabit Ethernet Controller

# Successfully checked versions MacOS

- [x] MacOS Catalina 10.15.7
- [ ] MacOS Big Sur 
- [ ] MacOS Monterey 

# Installed Drivers 

Drivers | Short description
--- | ---
[HfsPlus](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi) | Needed for seeing HFS volumes
[OpenRuntime](https://github.com/acidanthera/OpenCorePkg/releases) | Extension for OpenCore to help with patching boot.efi for NVRAM fixes and better memory management

# Installed Kexts

Kexts | Short description
--- | ---
[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) | Emulates the SMC chip found on real macs, without this macOS will not boot
[Lilu](https://github.com/acidanthera/Lilu/releases) | A kext to patch many processes, required for AppleALC, WhateverGreen, VirtualSMC and many other kexts. Without Lilu, they will not work.
[WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases) | Used for graphics patching, DRM fixes, board ID checks, framebuffer fixes, etc; all GPUs benefit from this kext.
[AppleALC](https://github.com/acidanthera/AppleALC/releases) | Used for AppleHDA patching, allowing support for the majority of on-board sound controllers
[RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X/release) | Used for work ethernet card
[VoodooPS2](https://github.com/acidanthera/VoodooPS2/releases) | Works with various PS2 keyboards, mice, and trackpads
[USBInjectAll](https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/) | Used for injecting Intel USB controllers on systems without defined USB ports in ACPI
