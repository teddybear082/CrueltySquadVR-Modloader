# CRUELTY SQUAD VR MOD LOADER

**This is a fork of the excellent modloader developed by crustyrashky and disco0, which installs both disco's 0.2.2b version of the crus modloader as well as files required for a VR mod using the Godot OpenXR Asset and XR Tools asset.**

**YOU SHOULD NOT USE THIS INSTALLER IF YOU DON'T HAVE A VR HEADSET**

Only use this mod on an official purchased version of the game.

**This is also in an ALPHA (TESTING) STATE!!! Back up EVERYTHING Cruelty Squad associated before trying this version of the modloader.  Right now it is intended ONLY for VR modders not end-users.**


## PRELIMINARY STEPS:

If you are running Cruelty Squad for the first time, run the game once first just to make sure all directories are created and then exit out.

If you have installed Cruelty Squad before and you have used any mods / modloaders before, you must return to a "clean" state of the game, otherwise this is very likely not to work.

Make sure the game is installed in the same directory as your Windows Powershell. For me, installing in my normal default Steam directory in Program Files worked fine.


## Install the loader

1. ~~Download the v0.17-VR-alpha release in THIS fork (teddybear082/new-install-script). Link here: https://github.com/teddybear082/crus-modloader/releases/tag/v.017-VR-alpha

This early build currently uses a modification of crustyrashky and disco0's newer install script method. Unzip the release and copy the folder this README is in to your game folder, it should look something like this:
```
=> <GAME_DIR>
  => <THIS FOLDER> (Unzipped)
    - Install-Modloader.ps1
    - install_modloader.bat
    - godotpcktool.exe
    - modloader.gdc
    - addons
    - libgodot_openxr.dll
    - openxr_loader.dll
    - override.cfg
	- cs-scripts-vr-mod
    - cs-vr-mod-vr-files
	- cs-vr-mod-xr-tools
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

## Return to flat screen mode
1. Remove the vr-related mod folds from your mod directory

## Uninstall the loader

1. Right-click game in steam
2. Go to Properties > Local Files
3. Verify integrity of game files

## Install custom levels

1. Drag/extract / unzip level folder into `%appdata%\Godot\app_userdata\Cruelty Squad\levels .  You can find levels at: https://crus.cc/maps/newest/`
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

Testers: Brock, MrGlock, Cortik from the Crus Discord and Hoshi82 (Youtube/Twitter) for testing 

DX from the Crus Discord for so much help and ideas even though DX does not have a VR headset

Trashski and Disc0 from the Crus discord for their modloader which literally made this mod happen and tons of advice

Digital Nightmare and MalcolmnNixon from Godot XR discord for so much help and pointers with VR stuff and creating the XRTools that again literally made this mod happen.



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

In main menu just select things by using the index finger of your hands

You can press the grip button of your offhand controller to use or grab items as well as using the virtual pointer on your weapon hand (grabby hand)

-----------
Vehicle controls (reversed in Left Handed mode):

Grab steering wheel and turn to turn 

Gas: right trigger

Brake: left trigger 

Reverse/Forward: Right pad press (toggle)

---------------------------------------------------

## 100 Percent Save File

If you just want to play around with CS in VR and have never played the game before or haven't gotten far, I found a 100% save file on NexusMods. Not my content and I can't vouch for it.

But you can find it here: https://www.nexusmods.com/crueltysquad/mods/2 as well as instructions for backing up your save file and installing the new save in case you want to revert back.

I have been using it for testing the mod functions but I can't say for sure whether using it breaks your experience at all.

## Known issues

-You have to jump up stairs

-You need to set the resolution in the in game menu to 1024 x 720 to ensure you can see the full menus

-If you have bad performance you can try the following:
	
	(1)	Turning down your resolution some in your headset settings / virtual desktop settings (medium instead of high or ultra)
	
	(2)	Turning on ASW always on (Oculus OpenXR Runtime), Virtual Desktop SSW always on (Steam OpenXR Runtime), SteamVR Reprojection always on
	
-Because of the same performance issues I have modified the game to deactivate NPCs that are a certain distance from you. This means the game does not quite play the same as the original and you can catch NPC's "sleeping on the job." But it also provides a 15-20 FPS boost in my testing.

-Wall jump in death mode is experimental

-Some random crashing. I don't think this is specifically related to VR.

-If you find other issues or think settings on certain implants should be tweaked, please let me know!
