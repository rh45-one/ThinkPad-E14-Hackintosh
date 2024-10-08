# ThinkPad Hackintosh - Ventura
ThinkPad E14 Gen5 Hackintosh EFI - Created with Dortania's OpenCore Install Guide

Laptop Specs: Ryzen 7 7730U, 40GB DDR4 3200Mhz (8GB + 32GB), 512GB NVME SSD, 1024GB NVME SSD.

### Note
I included a censored `config.plist` file named `censored-config.plist`. You will have to rename it and add your own MLB, ROM, SystemSerialNumber and SystemUUID.

### Troubleshooting
#### Post-Install Kernel Panic 
If you are using this EFI folder on a different laptop model, but similarly specced and get a kernel panic after installing MacOS, make sure to customize the USB port configuration to match your device.<br/> 
Also, you can avoid rebooting after a kernel panic by adding the following boot args: `debug=0x100` and `keepsyms=1` .

#### Non-functional brightness keys (Last Update: June 2024)
Commit [eff598f](https://github.com/ChefKissInc/NootedRed/commit/eff598f9d3f1dfcbe9ee5d220e63226fab0ef6f2) of **NootedRed** is referenced in an [issue](https://github.com/ChefKissInc/NootedRed/issues/236) regarding the backlight controls. Apparently, that was the last versión to ever work properly.<br/>
However, the action has since expired and it need to be compiled again.<br/>
I included the appropriate version inside my *kexts* folder, but it can also be recompiled using Xcode.

#### Additional features (Lenovo laptops)
Consider installing [YogaSMC](https://github.com/zhen-zen/YogaSMC) and installing the app on MacOS to enable additional features such as FN keys, charge threshold, fan control, keyboad backlight control, etc.
