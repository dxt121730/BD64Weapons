INSTALL:
==NOTE: this expects you to have already set up Fishbiter's Gz3Doom-OpenVR app, I used this guide to do so: https://www.reddit.com/r/Vive/comments/aakfow/how_to_play_doom_12_brutal_doom_heretic_hexen_in/==

1.copy BD64Weapons.pk3 into the directory that contains your GZDoom.exe and all brutal doom 64 pk3s
2.In this directory, create a new batch file or use the provided one to run brutal doom 64 with the model pack
3.If you wish, you can add the "BD64Weapons_pistol_replace.pk3" file to the batch file to use the modern styled pistol instead of the traditional doom 64 style one

ADDITIONAL NOTES:
1.Two things I've left out from having 3d models are the fists and the kicking animation. I don't have anywhere near the talent to make that look passable, so I just left it as is.

2.Tactical mode weapon reloads don't have animations right now. You'll just have to use the audio cues and the HUD to figure out when the reload is complete.

3.Personally, I've been using the replacement pk3 for brutal doom 64 found here: https://www.moddb.com/mods/brutal-doom-64/addons/brutal-doom-64-v2-patched
	3a.As mentioned in this package's documentation, you will still need the maps and music, etc. from the full brutal doom 64 package in order to make this work.
	3b.If you wish to use this as well, simply modify your batch file to look for the "bd64gamev2_patched.pk3" file instead of "bd64gamev2.pk3"

4.I've provided all the files I used along the way to create this pack in the archive, mostly for educational purposes for anyone else who tries to do something like this. Feel free to use these assets however you like, just don't charge anybody for them.


SSG ISSUE:
1.There is an issue with the super shotgun where it will disappear for a couple seconds between shots due to the game wanting to display no sprite.
2.I've fixed this locally in the "bd64gamev2_patched.pk3" file for my own personal build and have provided the modified "pk3" file for your use. All credit goes to moddb user "swc132994" for this patched pk3 file (and obviously Sergeant_Mark_IV for brutal doom 64 proper) and if I do hear from either of them to remove this file from the package, I'll  gladly do so.
3.Note that, as with the original patched version, you'll need to alter the provided .bat file to make it work

(If you wish to make this change yourself for some reason, go into the DECORATE.SSg.txt file in your bd64gamev2 (or bd64gamev2_patched) .pk3 and change the "Fire" state lines:

	SSGG NOPQ 1
	TNT1 A 8
	SSGG RS 1
to

	SSGG NOPQ 2
	SSGG RS 3
	

and the "Reload" state lines:

	SSGG NOPQ 1
	TNT1 A 8
	SSGG RS 1
to

	SSGG NOPQ 2
	SSGG RS 3
	
[[EDITED BECAUSE I WAS DUMB BEFORE AND MISREAD THE ORIGINAL, THESE DEFS WILL WORK BETTER THAN THE OLD ONES]]

DISCLAIMER:
I originally just made this package to use locally because I disliked having to use the sprite options provided by default. I can't guarantee this will work on all setups or that I'll be able to provide support for any specific parts of it. I just wanted to put it out there for anyone in the same boat.

THANKS:
Thanks to /u/-Chell for the excellent "WeaponsForVR.pk3" from which I figured out most of this stuff.
Thanks to github user "Fishbiter" for their implementation of 6DoF aimable weapons and the gz3doom-OpenVR that this model pack is designed for.
Thanks to Sergeant_Mark_IV for Brutal Doom 64
Thanks to moddb user "swc132994" for their patch to the brutal doom 64 pk3 that fixed some of the bigger issues I ran into along the way
