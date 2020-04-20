# S540-15IWL
Lenovo Ideapad S540-15IWL GTX Laptop on MacOS Catalina

Lenovo Ideapad S540-15IWL GTX (81SW)

![Lenovo Ideapad S540-15IWL GTX](https://brain-images-ssl.cdn.dixons.com/4/4/10193744/u_10193744.jpg)
 
Processor: Intel Core i7-8565U (4C / 8T, 1.8 / 4.6GHz, 8MB)
Memory: 4GB Soldered + 16GB DIMM DDR4-2400
Graphics: Integrated Intel UHD Graphics 620 + GeForce GTX 1650
Display: 15.6" FHD (1920x1080) TN 220nits Anti-glare
Hard Drive: CRUCIAL SSD 500 GB + Samsung 256GB PCIe NVMe
Wireless Network: Intel AC-9462 (Card replaced with BCM94360CS2 on an adapter.)
Audio: ALC 257
Camera: Inbuilt
Battery: Integrated 52.5Wh
Operating System: Windows 10 Pro + MacOS Catalina with Clover.
BIOS: LATEST
Ethernet + Bluetooth: RTL 8188EU
Card Reader: Realtek RTS522A
 
 
What's working:
Keyboard
Trackpad, gestures.
Audio
Headphones
Brightness control
Sleep
Inbuilt Camera
Card Reader: Fix also Sleep Problem! 

What's Not Working:
Dedicated Graphic Cards with Acceleration 
FingerPrint Sensor
HDMI PORT

BIOS:
Ensure your disk is in AHCI mode. Here are the settings that I used.

USB installer:
Create a normal installation media.
Use my complete EFI Folder below.

Ensure your clover/drivers/uefi folder has following files:
ApfsDriverLoader.efi
AppleImageCodec.efi
AppleKeyAggregator.efi
AppleKeyFeeder.efi
AppleUITheme.efi
AptioMemoryFix.efi
AudioDxe.efi
DataHubDxe.efi
NvmExpressDxe.efi
FSInject.efi
VirtualSmc.efi
HFSPlus.efi

Ensure your clover/kexts folder has following files:
Lilu.kext
AppleALC.kext
EFICheckDisabler.kext
NoTouchID.kext
NVMeFix.kext
Sinetek-rtsx.kext
SMCBatteryManager.kext
SMCLightSensor.kext
SMCProcessor.kext
SystemProfiler
Voodoo2C.kext
VoodooInput.kext
Voodoo2CHID.kext
VoodooPS2Controller.kext
VirtualSMC.kext
WhateverGreen.kext
 
Quickly Installation
Install Clover on your usb drive EFI Partition and replace with my complete EFI Below.
 
Keyboard:
Keyboard already be working but the Keys Will be FN+K and FN+P for fix Brightness and Volume shortcuts:
Volume already works. For brightness fix, use the SSDT-Q1112 patch.
Also apply the _Q11->XQ11 and _Q12->XQ12 rename patch via clover config.

Follow this guide if you need details.
Inbuilt Camera
Works. No extra files needed.
CPU power management
Works. No extra files needed.

Sleep
Disable Hibernation:
sudo pmset -a hibernatemode 0
sudo pmset -a standby 0
sudo pmset -a autopoweroff 0
sudo rm /var/vm/sleepimage
sudo mkdir /var/vm/sleepimage

Configuration for MacBook Pro 15,2 (13-inch Mid 2019)
