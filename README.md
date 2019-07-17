# Emulated NVRAM
 
 

Opencore Emulated NVRAM for Non Supported NVRAM Motherboards


This is a small guide for users that use opencore, that don't have working NVRAM, There is certain motherboards that will not support native NVRAM including Z390.

Creating Your NVRAM.plist

So to create a nvram.plist 2 aspects are needed in your config.plist:

LegacyEnable: set to YES

LegacySchema: NVRAM variables set
(OpenCore compares these to the variables present in nvram.plist)

Once those are set, Compile the latest version of OpenCore and you want to run the LogoutHook.command found in OpenCore - EFI/OC/Utilities/LogoutHook. This will create a new folder, which dumps the basic output. And  you'll find a plist file named nvram.plist. Place this in the root of your EFI Folder and you'll have emulated NVRAM

![NVRAM Tool](https://i.imgur.com/lAegCiD.png)

![Newly Created NVRAM.plist](https://i.imgur.com/grwl4TX.png)
