# 0.8.5 OpenCore - Dell 8940 with macOS Monterey (Windows tutorial but can be with macOS)

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

You need to open the macrecovery folder in OpenCore-0 -> Utilities -> macrecovery 

After that open CMD in this folder and enter this command to download the macOS Monterey Version : python ./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download

Normally you will have two files in the macrecovery folder : BaseSystem.dmg and BaseSystem.chunklist

# 3) Format your USB Stick  :

You will need to format your USB exactly like that :


![format-usb-rufus 43feba9e](https://user-images.githubusercontent.com/78324112/195980444-6415c1f6-5b51-45ae-9866-f61c1dbb3390.png)

# 4) Put macOS in the key :

You wil have to create a folder at the root named "com.apple.recovery.boot" and place the two files previously downloaded (BaseSystem.dmg and BaseSystem.chunklist).

After that, copy my EFI folder at the root;

# 5) Mapping your USB Port :



# Bios Setting you will need to changes before boot in the USB installer :

To enter into the bios press F2 when the Dell logo appears.


