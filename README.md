# CRUELTY SQUAD VR MOD LOADER
![teddybearvr](https://user-images.githubusercontent.com/87204721/226103085-e4b45fcd-df85-46fa-9354-1449c1da08ad.png)

**This modloader was developed as a fork of the excellent modloader developed by crustyrashky and disco0, it is now its own repo only to avoid confusion between the VR mod and normal flatscreen modloader. But all code for the modloader that makes this work was originally developed by them, and credit goes to them.**

**YOU SHOULD NOT USE THIS INSTALLER IF YOU DON'T HAVE A VR HEADSET**

Only use this mod on an official purchased version of the game.

**Back up EVERYTHING Cruelty Squad associated before trying this version of the modloader.  Especially your SAVES!**

Post any issues to the Issues tab of this Github so I can keep track of them.  Or you can contact me on the Cruelty Squad discord modifications channel or on the Flat2VR discord server.  

This VR mod is now co-maintained and updated by https://github.com/SpencerBinXia as well.

**LAST UPDATED: March 18, 2023 (v 1.0-Stable)**

## PRELIMINARY STEPS:

If you are running Cruelty Squad for the first time, run the game once first just to make sure all directories are created and then exit out.

If you have installed Cruelty Squad before and you have used any mods / modloaders before, you must return to a "clean" state of the game, otherwise this is very likely not to work.

Make sure the game is installed in the same directory as your Windows Powershell. For me, installing in my normal default Steam directory in Program Files worked fine.  Some have had success on other drives, but if it fails, this may be the issue.

If you are using WMR, set your OpenXR runtime to SteamVR NOT WMR in the SteamVR settings.  Otherwise the game will appear on the screen but not your headset.

Check out the wiki page for more FAQs and stuff: https://github.com/teddybear082/CrueltySquadVR-Modloader/wiki

**HOW TO UPDATE IF ALREADY INSTALLED VR MOD:** See the wiki link above or click on "Wiki" on this page.

**EPILEPSY / SEIZURE WARNING:** Textures move very quickly in VR, psychos cause a visual effect that may be disturbing, and there are flashing images. Therefore if you have Epilepsy you probably should not play this VR mod.

## Install the loader

1. ~~Download the v1.0-release-crueltysquad-vrmod release in this repo. Link here: https://github.com/teddybear082/CrueltySquadVR-Modloader/releases/download/v1.0-release-crueltysquad-vrmod/crus-vr-modloader.zip (folder will be called "crus-vr-modloader.zip")

This build currently uses a modification of crustyrashky and disco0's newer install script method that was developed for the flatscreen game. Unzip the release and copy the folder this README is in to your game folder, it should look something like this:
```
=> <GAME_DIR>
  => <THIS FOLDER> (Unzipped, but still a folder - crus-vr-modloader)
    - Install-Modloader.ps1
    - install_modloader.bat
    - godotpcktool.exe
    - modloader.gdc
    - addons (folder)
    - libgodot_openxr.dll
    - openxr_loader.dll
    - override.cfg
    - cs-scripts-vr-mod (folder)
    - cs-vr-mod-vr-files (folder)
    - cs-vr-mod-xr-tools (folder)
    - README.md
  - crueltysquad.pck
  - crueltysquad.exe
  - [...]
```


![Stable1-0-release-install-directory](https://user-images.githubusercontent.com/87204721/226102214-76b5d4af-c2a5-4ff8-807b-cee11b7862f1.png)




---------------------------------------------------------------------------


![Stable1-0-release-crus-vr-modloader-folder](https://user-images.githubusercontent.com/87204721/226102220-0d0f10d1-b9cc-4d8f-9781-0f3a7dc6bc05.png)


**The key thing here is that you unzip to the crus-vr-modloader folder as shown above NOT to loose files and NOT in a nested folder with more than one crus-vr-modloader folders.  Just one crus-vr-modloader folder, next to your .exe.**


2. Run `install_modloader.bat`
3. Check to see if your game directory now has an override.cfg, libgodot_openxr.dll and openxr_loader.dll next to the crueltysquad.exe and crueltysquad.pck (If so, that is a good sign, as this installer copies those files there; there will also now be a backup of your original game exe and pck as shown in the screenshots above). **If Windows Defender or Windows complains about the files or asks you for permission to run or keep the files, make sure to choose run or keep.**
4. Start the game (it may crash the first time due to lack of the godot-xr-tools asset); if you now have a `mods` folder under `%appdata%\Godot\app_userdata\Cruelty Squad\` it worked  (as an example, I find this folder in my personal install by navigating to Windows(C:)\Users\[my windows user profile name]\AppData\Roaming\Godot\app_userdata\Cruelty Squad\mods).

5. Now go to that `mods` folder and copy the "cs-vr-mod-vr-files" folder, "cs-vr-mod-xr-tools" folder, and "cs-scripts-vr-mod" folder from this folder to the 'mods' folder.
6. Run the crueltysquad.exe again with your VR headset on and active / running and the main scene should populate into your VR headset if all has gone well.
	If it crashes the first time to desktop, run it again, sometimes it takes FOUR times running the .exe for everything to take effect.  More than that, and there's a problem.
	
	There will be a terminal / command prompt window running while you run the game.  You'll see lots of supposed "ERROR:" messages but they do not impact the game, it is just very detailed logging going on.

## Known issues

-There is no teleport. If you get motion sickness you may want to try https://store.steampowered.com/app/1143750/VRocker/ to help.  I confirmed it works at least with Quest+Virtual Desktop in the "stick touch" mode. Won't work with Link/Airlink. Not sure about other platforms.

-You have to jump up stairs

-If you have a Valve Index, reduce to 90 framerate instead of 144 or 120.  144 definitely causes odd jitter and performance issues.

-If you have bad performance otherwise you can try the following:
	
	(1)	Turning down your resolution some in your headset settings / virtual desktop settings (medium instead of high or ultra)
	
	(2)	Turning on ASW always on (Oculus OpenXR Runtime), Virtual Desktop SSW always on (Steam OpenXR Runtime), SteamVR Reprojection always on
	
	(3)	Turning down the "NPCs" and "Draw Distance" values in game settings.
	
-Because of the same performance issues I have modified the game to deactivate NPCs that are a certain distance from you. This means the game does not quite play the same as the original and you can catch NPC's "sleeping on the job." But it also provides a 15-20 FPS boost in my testing.  If you want to go back to the normal way the game was made and sacrifice those performance games, just uncheck the "NPC Performance Hack" in the main menu.


-If you find other issues or think settings on certain implants should be tweaked, please let me know!  You can post issues on the "Issues" tab of this repo or contact me on the Cruelty Squad or Flat2VR discords.


## Return to flat screen mode
1. Remove the vr-related mod folds from your mod directory

## Uninstall the loader

1. Right-click game in steam
2. Go to Properties > Local Files
3. Verify integrity of game files

## Install custom levels

1. Drag/extract / unzip level folder into `%appdata%\Godot\app_userdata\Cruelty Squad\levels .`  You can find levels at: https://crus.cc/maps/newest/
2. Launch the game
3. If it didn't work post to #modifications in the discord with the contents of `%appdata%\Godot\app_userdata\Cruelty Squad\logs\mods.log`

## Uninstall mods

1. Remove mod folder from `%appdata%\Godot\app_userdata\Cruelty Squad\mods`

## Credits

Made for https://store.steampowered.com/app/1388770/Cruelty_Squad/

Uses https://github.com/hhyyrylainen/GodotPckTool to install

Builds off of https://github.com/disco0/crus-modloader and https://github.com/crustyrashky/crus-modloader

Uses Godot OpenXR Asset and Godot XR Tools assets, found here:

https://github.com/GodotVR/godot_openxr (uses Godot OpenXR 1.3.0 release, July 15, 2022)

https://github.com/GodotVR/godot-xr-tools (uses December 29, 2022 build)

Special thanks to:

Ville Kallio, dev of Cruelty Squad, for the game, supporting the modding community, and for help figuring out a performance issue and fix that was disproportionately impacting the VR mod.

Spencer for jumping into Crus VR dev after the 1.0 beta to make huge changes for the 1.4 beta and 1.0 stable release

Testers: Distant075, Brock, MrGlock, Cortik from the Crus Discord, Hoshi82 (Youtube/Twitter), Iona_dev (Twitter), Asaklair (Twitter/Discord - also makes music for modded maps!), Cortezj5 (Twitch) for testing 

DX from the Crus Discord for so much help and ideas even though DX does not have a VR headset

Trashski and Disc0 from the Crus discord for their modloader which literally made this mod happen and tons of advice along the way.

Digital Nightmare and MalcolmnNixon from Godot XR discord for so much help and pointers with VR stuff and creating the XRTools that again literally made this mod happen.

Bastiaan Olij ("mux213") for creating and maintaining Godot's XR Asset and functionality and making GodotXR so easy for a noob like me to work with.

Frenchie from the Cruelty Squad Discord for creating the awesome CS mods website and hosting this mod!

Saracen from Godot Engine and the V-Sekai Godot project for helping point me to the ultimate solution for crashes!!

---------------------------------------------------

## Controls

Left (off hand)

Trigger: Kick (targets at where you aim your weapon)/jetpack Activate (toggle)/BioThruster/Throw held items- and select items on menu with pointer

X: Not used

Y: Toggle floating menu (pause menu) and stocks menu on right hand (touch stocks menu with left index finger to select options; use pointer to select options on floating menu or get close enough to hit it with your hand)

Grip: Climb, Use items / doors in proximity to hand

Joystick: move 

Joystick press: go back screens in main menu, like when selecting implants and equipment 

-----------------

Right (weapon hand)

Trigger: Shoot / Skull gun - select items on menu with pointer 

A: throw weapon (For Vive OG wand users, throw weapon instead by pressing both triggers and both grips at the same time)

B: Grappendix

Grip: Use  / climb / Activate reload 

Joystick: turn (Joystick up to jump, joystick down for crouch)

Joystick press: hold for Radial menu to select weapon, go back screens on main menu 


---------------


Gesture controls:

Hand Radial menu: Select weapon by hovering and then releasing joystick press 

	On radial menu, bottom option is tertiary and will activate grenades or consume health items if you have those as your tertiary.
	
	On radial menu, up option is suicide. Choose it twice to activate.

Point weapon down: Reload (while holding grip)

You can swing your arms in an upward movement together to jump instead of using jump button

In main menu just select things by using the index finger of your hands

You can press the grip button of your offhand controller to use or grab items as well as using the virtual pointer on your weapon hand (grabby hand)

-----------
Vehicle controls (reversed in Left Handed mode):

Grab steering wheel and turn to turn 

Gas: right trigger

Brake: left trigger 

Reverse/Forward: Right pad press (toggle)

---------------------------------------------------

Recenter View - In main menu you can reset view with the B or Y buttons, in game you can recenter view by pressing offhand (non-weapon hand) thumbstick.

-------------

## 100 Percent Save File

If you just want to play around with CS in VR and have never played the game before or haven't gotten far, I found a 100% save file on NexusMods. Not my content and I can't vouch for it.

But you can find it here: https://www.nexusmods.com/crueltysquad/mods/2 as well as instructions for backing up your save file and installing the new save in case you want to revert back.

I have been using it for testing the mod functions for quite some time now but I can't say for sure whether using it breaks your experience at all.


