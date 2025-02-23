🔙 [Windows Dual Boot Instructions](https://github.com/ahaddad91/OdinMultiBootGuides/blob/main/pages/odin_dualboot_windows_guide.md)

Update GPU Driver from POCO F1
This allows to run some games that were not running with out of the box valhalla drivers (ie Need For Speed Most Wanted 2005)
1 - Go to https://github.com/edk2-porting/WOA-Drivers/releases/tag/2210.1-fix

2 - Download the beryllium.zip file

3 - Extract the GPU folder to your desktop

4 - Go to device manager, video adapters, right click Adreno 630, update drivers

5 - Choose to select driver from your computer, in the next screen select the option to search for drivers in a folder, select "from disk"

6 - Select the qcdx850.inf file from your Desktop\GPU folder

7 - It will display a message saying that the driver is not signed, install anyway

8 - Your GPU will display as Adreno 680 in device manager, it works fine, just ignore

App Screenshot

Video of NFS MW (doesn't work out of the box in Valhalla installation) , DMC4 and NFS Hot Pursuit running with the updated driver:

https://www.youtube.com/watch?v=LeEsKOwLIXk

To get DMC4 to work you have to go to C:\Users\YOURUSERNAME\AppData\Local\CAPCOM\DEVILMAYCRY4SPECIALEDITION open config.ini with text editor and replace everything with https://pastebin.com/emS7h5Ew
You should now be able to enter graphics settings ingame, set everything to low.

To get NFS Hot Pursuit to work, go to My Documents\Criterion Games\Need for Speed(TM) Hot Pursuit open config.NFS11Save with text editor and replace everything with https://pastebin.com/37VNQZMU and:
Launch game. Decreasing resolution in this game has little to no impact on FPS, so I run it in 1080p.

Open task manager with the game open, go to NFS11.exe process, right click, set affinity and uncheck core 0 and core 1, go back to game and enjoy.
