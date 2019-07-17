# Emulated NVRAM, Issue Fix Work In Progress
 
 

Opencore Emulated NVRAM


This is a small guide for users that use opencore, that don't have working NVRAM, There is certain motherboards that will not support native NVRAM and are the non-Z370 300 series chipsets:

B360
B365
H310
H370
Q370
Z390

Creating Your NVRAM.plist

![NVRAM Tool](https://i.imgur.com/lAegCiD.png)

So to creat a nvram.plist 2 aspects are needed in your config.plist:

LegacyEnable: set to YES

LegacySchema: NVRAM variables set
(OpenCore compares these to the variables present in nvram.plist)

Once those are set, Compile the latest version of OpenCore and you want to run the LogoutHook.command found in OpenCore - EFI/OC/Utilities/LogoutHook. This will create a new folder, which dumps the basic output. And  you'll find a plist file named nvram.plist. Place this in the root of your EFI Folder and you'll have emulated NVRAM

![Newly Created NVRAM.plist](https://i.imgur.com/grwl4TX.png)
