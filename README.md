# 0.8.5 OpenCore - Dell 8940 with macOS Monterey (Windows tutorial but can be used in macOS)

# Dell 8940 Configuration :

CPU : i9-10900K 

GPU : Dell RTX 3060 Ti

iGPU : Intel UHD Graphics 630

WiFi/Bluetooth Card : Killer..

RAM : 2x8Go 

Monitor (Speaker Integrated) : LG 32UL950-W 4K 32"

# What is not Working (I'm working on) ?

- Bluetooth
- 4K (I can only run 2K)
- Speaker of the Monitor
- ShutDown/Reboot/Sleep
- Uses of external disk than apfs 

OtherWise all works perflectly (iServices, WiFi, Fluidity...)

# 1) What you need :

GenSMBIOS to create your own SMBIOS deets (SN/MLB/UUID/ROM) : https://github.com/corpnewt/GenSMBIOS

ProperTree to modify the config,plist for your own computer : https://github.com/corpnewt/ProperTree

macrecovery tool to download the macOS partition : https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.5

USBTool Mapper : https://github.com/USBToolBox/tool/releases/tag/0.1.1

Rufus to format your USB : https://rufus.ie/

My EFI Folder in the top 

Python3 if you don't have installing this : https://www.python.org/downloads/release/python-3108/

# 2) Download the macOS partition with Macrecovery tool :

Open the macrecovery folder in OpenCore-0 -> Utilities -> macrecovery 

After that open CMD in this folder and enter this command to download the latest macOS Version : python ./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download

Normally you will have two files in the macrecovery folder : BaseSystem.dmg and BaseSystem.chunklist

# 3) Format your USB Stick  :

Format your USB exactly like that :


![format-usb-rufus 43feba9e](https://user-images.githubusercontent.com/78324112/195980444-6415c1f6-5b51-45ae-9866-f61c1dbb3390.png)

# 4) Put macOS in the key :

Create a folder at the root named "com.apple.recovery.boot" and place the two files previously downloaded (BaseSystem.dmg and BaseSystem.chunklist).

After that, copy my EFI folder at the root.

# 5) Mapping your USB Port :

Open the USBTool software and enter D to Discover Ports (Every 5 seconds it refresh the usb ports detected)

![Capture d’écran 2022-10-15 à 12 18 05](https://user-images.githubusercontent.com/78324112/195981177-e2d4e307-fd50-43c3-b1a1-549a23e98185.png)

After clicking, enter usb devices in all your ports to have them detected by the USBPort Mapper Program. You don't need to do it at the same time, it refresh every 5 seconds the usb ports detected.

And Finally enter S and after K to Build the Kext.

Recover the kext and drop it into the kext folder of the EFI.

# Generate SMBIOS deets :





# Bios Setting you will need to changes before boot in the USB installer :

To enter into the bios press F2 when the Dell logo appears.


