# 0.8.5 OpenCore - Dell 8940 with macOS Monterey (Windows tutorial but can be with macOS)

# Dell 8940 Configuration :

CPU : i9-10900K 

GPU : Dell RTX 3060 Ti

iGPU : Intel UHD Graphics 630

WiFi/Bluetooth Card : Killer..

RAM : 2x8Go 

Monitor (Speaker Integrated) : LG 32UL950-W 4K 32"

# 1) What you need :

GenSMBIOS to create your own SMBIOS deets (SN/MLB/UUID/ROM) : https://github.com/corpnewt/GenSMBIOS

ProperTree to modify the config,plist for your own computer : https://github.com/corpnewt/ProperTree

macrecovery tool to download the macOS partition : https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.5

USBTool Mapper : https://github.com/USBToolBox/tool/releases/tag/0.1.1

My EFI Folder in the top 

Python3 if you don't have installing this : https://www.python.org/downloads/release/python-3108/

# 2) Download the macOS partition with Macrecovery tool :

You need to open the macrecovery folder in OpenCore-0 -> Utilities -> macrecovery 

After that open CMD in this folder and enter this command to download the macOS Monterey Version : python ./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download

Normally you will have two files : BaseSystem.dmg and BaseSystem.chunklist

# 3) Create the USB Bootable macOS installer :





