# CRUELTY SQUAD VR MOD LOADER

**This modloader was developed as a fork of the excellent modloader developed by crustyrashky and disco0, it is now its own repo only to avoid confusion between the VR mod and normal flatscreen modloader. But all code for the modloader that makes this work was originally developed by them, and credit goes to them.**

**YOU SHOULD NOT USE THIS INSTALLER IF YOU DON'T HAVE A VR HEADSET**

Only use this mod on an official purchased version of the game.

**This is also in an BETA (TESTING) STATE!!! Back up EVERYTHING Cruelty Squad associated before trying this version of the modloader.  Especially your SAVES! Crashes that happen with the VR mod right now (which I am looking into) could corrupt your save game so make sure you back it up.**

Post any issues to the Issues tab of this Github so I can keep track of them.  Or you can contact me on the Cruelty Squad discord modifications channel or on the Flat2VR discord server.

## PRELIMINARY STEPS:

If you are running Cruelty Squad for the first time, run the game once first just to make sure all directories are created and then exit out.

If you have installed Cruelty Squad before and you have used any mods / modloaders before, you must return to a "clean" state of the game, otherwise this is very likely not to work.

Make sure the game is installed in the same directory as your Windows Powershell. For me, installing in my normal default Steam directory in Program Files worked fine.  Some have had success on other drives, but if it fails, this may be the issue.


## Install the loader

1. ~~Download the v0.1-VR-beta release in this repo. Link here: https://github.com/teddybear082/CrueltySquadVR-Modloader/releases/tag/v.1.0-beta-CrueltySquadVR-mod

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


![cs-vr-mod-install-directory1](https://user-images.githubusercontent.com/87204721/215295165-ea75968d-4ed2-42f7-be58-ad4119a17db9.png)



---------------------------------------------------------------------------

![cs-vr-mod-install-directory2](https://user-images.githubusercontent.com/87204721/215295184-94778c91-a6e2-4376-b979-a5a4bf64b859.png)


2. Run `install_modloader.bat`
3. Check to see if your game directory now has an override.cfg, libgodot_openxr.dll and openxr_loader.dll next to the crueltysquad.exe and crueltysquad.pck (If so, that is a good sign, as this installer copies those files there).
4. Start the game (it may crash the first time due to lack of the godot-xr-tools asset); if you now have a `mods` folder under `%appdata%\Godot\app_userdata\Cruelty Squad\` it worked  (as an example, I find this folder in my personal install by navigating to Windows(C:)\Users\[my windows user profile name]\AppData\Roaming\Godot\app_userdata\Cruelty Squad\mods).

5. Now go to that `mods` folder and copy the "cs-vr-mod-vr-files" folder, "cs-vr-mod-xr-tools" folder, and "cs-scripts-vr-mod" folder from this folder to the 'mods' folder.
6. Run the crueltysquad.exe again with your VR headset on and active / running and the main scene should populate into your VR headset if all has gone well.
	If it crashes the first time to desktop, run it again, sometimes it takes THREE times running the .exe for everything to take effect.  More than that, and there's a problem.

## Known issues

-There is no teleport. If you get motion sickness you may want to try https://store.steampowered.com/app/1143750/VRocker/ to help.  I confirmed it works at least with Quest+Virtual Desktop in the "stick touch" mode. Won't work with Link/Airlink. Not sure about other platforms.

-You have to jump up stairs

-If you have a Valve Index, reduce to 90 framerate instead of 144 or 120.  144 definitely causes odd jitter and performance issues.

-If you have bad performance otherwise you can try the following:
	
	(1)	Turning down your resolution some in your headset settings / virtual desktop settings (medium instead of high or ultra)
	
	(2)	Turning on ASW always on (Oculus OpenXR Runtime), Virtual Desktop SSW always on (Steam OpenXR Runtime), SteamVR Reprojection always on
	
	(3)	Turning down the "NPCs" and "Draw Distance" values in game settings.
	
-Because of the same performance issues I have modified the game to deactivate NPCs that are a certain distance from you. This means the game does not quite play the same as the original and you can catch NPC's "sleeping on the job." But it also provides a 15-20 FPS boost in my testing.  If you want to go back to the normal way the game was made and sacrifice those performance games, just uncheck the "NPC Performance Hack" in the main menu.

-Some random crashing. I don't think this is specifically related to VR, but it might be.

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

Testers: Brock, MrGlock, Cortik from the Crus Discord, Hoshi82 (Youtube/Twitter), Iona_dev (Twitter), Asaklair (Twitter/Discord - also makes music for modded maps!) for testing 

DX from the Crus Discord for so much help and ideas even though DX does not have a VR headset

Trashski and Disc0 from the Crus discord for their modloader which literally made this mod happen and tons of advice along the way.

Digital Nightmare and MalcolmnNixon from Godot XR discord for so much help and pointers with VR stuff and creating the XRTools that again literally made this mod happen.

Bastiaan Olij ("mux213") for creating and maintaining Godot's XR Asset and functionality and making GodotXR so easy for a noob like me to work with.

Frenchie from the Cruelty Squad Discord for creating the awesome CS mods website and hosting this mod!

---------------------------------------------------

## Controls

Left (off hand)

Trigger: Kick/jetpack Activate (toggle)/BioThruster/Throw held items- and select items on menu with pointer

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


