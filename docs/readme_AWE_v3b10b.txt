Modification for Call of Duty 2 multiplayer 1.2/1.3
---------------------------------------------------
Name   : AWE (Additional War Effects)
Version: 3.0 beta 10b
Author : Bell
Site   : http://awe.milliways.st/
Forum  : http://forum.milliways.st/


Donations
---------
If you think this mod has brought new life into your CoD server and got
a few dollars(or euros) to spend, go here: http://awe.milliways.st/donations/


Compatibility
-------------
Full compatibility on Call of Duty 2 stock gametypes and gametypes prepared for AWE
Custom gametypes not prepared for AWE will lack some features (noted in awe.cfg)


Credits (Not all those things have been ported to AWE3/CoD2 yet and perhaps some won't ever be)
-----------------------------------------------------------------------------------------------
Mortars, hitblip, cvardef, firstaid,	- Ravir (http://demolition.codcity.org/)
spawnmodel and admin tool functions.

Bomber planes 					- Pharao_FS (http://www.pharao-fs.de.vu/)

Parachutes, tracers, skyflashes code	- Parts (http://www.vs-uk.net/)
laserdot and welcome message are based
on Total War 2.3a

Painscreen, bloodyscreen, bleeding,		- Chris P (http://www.mercilessmod.com)
taunts, and the bleeding effect are based
on Merciless Blood Mod.

Mobile MG42 and mobile PTRS41 is based on	- RedMercury, Hellspawn
RedMercury and Hellspawns mobileMG42 mod

Drop Weapon on arm/hand hit is based on	- Poolmaster (http://ediv.codfiles.com)
Merciless but propably origins from
Poolmasters Realism Mod (PRM)

Alternate position for team status		- Pethron

Reflection formula in bounceObject()	- Hellspawn
	
Code to disable secondary weapon		- Zeus[BTY]

British taunts					- DirtyRat

Enhanced parachuting and stuka sounds	- DetPak

Cold breath is based on forums posts by	- French Daddy and [MW]gitman

Map voting based on code by			- NC-17(codam, powerserver) (REWORKED BY wizard220, MODIFIED BY FrAnCkY55)

Health regeneration modifications		- Wanna Ganoush -- www.anarchic-x.com

Killcam time overriding				- soco11

Duplicate name check				- trydis

Colored smoke grenades				- Dale

Alternative colored smoke grenades		- DaveW

Retrieval						- etromania

Indvidual Hold The Flag				- La Truffe

Disabling of grenade icons,			- bullet-worm
forcing exploitable dvars,
quick compass ping fading,
ideas taken from Powerserver

Helmet bounce sound				- FK

Putting back Mods to the Main Menu		- Filbert

Falldamage modifiers				- Dorian / Jazz

The rest						- Bell (http://awe.milliways.st/)

Suggestions, ideas, feedback and inspiration	- All the people in the various CoD forums
								  http://www.iwnation.com/Forums/
								  http://www.mercilessmod.com/
								  http://www.codboards.com/
								  http://www.callofduty.se/forum/
								  http://forums.vs-uk.net/
								  http://www.gamingforums.com/
								  http://www.callofdutyx.com/forums/
								  http://forums.milliways.st/

Previous webhosting of AWE website and forums	- TyphoonServers (http://www.typhoonservers.com/)

Current webhosting of AWE website and forums	- Asylym Game Servers (http://www.asylum-gameservers.com/)


Features
--------
- Teamkill detection with different punishments.
- Server messages
- Welcome messages
- Disable minefields
- Server/Clan logo under compass
- Sprinting
- Map voting
- Customizable health regeneration
- Customizable killcam time
- Healthbar
- Random maprotation
- Maprotation error correction
- Painsounds
- Deathsounds
- Checking and renaming of duplicate player names
- Disable deathicons
- Disable nadeicons
- Disable weapon drops
- Disable grenade drops
- Disable pistols
- Disable binoculars
- Disable shellshock
- Disable hud score
- Disable objective points
- Disable damage feedback
- Disable/Force crosshair
- Disable/Force crosshair enemy color
- Disable health regeneration
- Colored smoke grenades
- Headpopping
- Helmetpopping
- Damage modifiers
- Unknown Soldier handling
- Blood splatter on screen
- Cold breath
- Change gravity
- Change speed
- Healthpacks
- Mortars
- Tripwires
- Fog overriding (fading)
- Remove bodies and sink bodies
- Ammo limiting
- Unlimited ammo
- Weapon limiting
- Dvar to stop clientside exploits
- Dvar to select non-cookable or cookable nades
- 3 variants of the cookable nades with different throw distances
- Dvar to select variant of smoke nades
- Spawn protection
- Selectable secondary weapon
- Turret overheating
- Turret disabling

New gametypes
-------------
- Last Team Standing
- Hold the Flag
- Retrieval
- Last Man Standing
- Individual Hold the Flag


Installation (Windows)
----------------------
Run the installer.


Manual installation for those who choosed the .zip file
-------------------------------------------------------

***Required***
Copy the the a3b10 folder to the same place where you have your COD2MP_s.exe (or cod2_lnxded) file.
For example: C:\Program Files\Activision\Call of Duty 2\

Clientside mods (IMPORTANT! Your server should only contain 1 out of these 3)
-----------------------------------------------------------------------------
There are 3 different .iwd files which all are a combination of these:

b0 = no blood mod
b1 = Blood mod version 1.0 (unrealistic)
b2 = Blood mod version 2.0 (realistic)

Make sure you add +set fs_game a3b10 to the command line that start your server.

Windows example:

C:\Program Files\Activision\Call of Duty 2\CoD2MP_s.exe +set fs_game a3b10 +set dedicated 2 +exec myserver.cfg +map_rotate

Linux example:

./cod2_lnxded +set fs_game a3b10 +set dedicated 2 +exec myserver.cfg +map_rotate


Random maprotation
------------------
Enable this by setting awe_random_maprotation to 1.

This will read all entries in sv_maprotation at the start of each game and set sv_maprotationcurrent
one of them by random.

If you want to use the same map with different gametypes you have to specifiy the map in the map rotation
for each gametype. For example:

set sv_maprotation "gametype tdm map mp_breakout gametype sd map mp_breakout gametype hq map mp_breakout"
... this maprotation will only play mp_breakout but will randomize between tdm, sd and hq.

When you start up the server it will always play the first map in the rotation but as soon as that map
ends it will rotate to a random map.


Dvars (dvars and descriptions have moved to awe.cfg)
----------------------------------------------------
See the included awe.cfg for more info.

- awe.cfg is an example config file with quite sane value and it's a good start.

For a quickstart, copy awe.cfg to your a3b10 folder and edit it to enable/disable the stuff you want/don't want.
Then make sure your server executes awe.cfg by either calling it from your egular config file like this:

exec awe.cfg

or by adding this to the commandline that starts your server:

+exec awe.cfg

There are also example files included for fog settings, htf and lts.


Overriding dvars for gametypes and/or maps
------------------------------------------
Since I also use an improved version of Ravir's dvar handling code you can override the settings
for specific gametypes and/or maps by adding the gametype and/or mapname the dvar.

Example:

set awe_mortar_hq_mp_carentan "1"	// will override
set awe_mortar_hq "2"		// which will override
set awe_mortar_mp_carentan "3"	// Which will override
set awe_mortar "4"

In the above example all maps, except mp_carentan, will have 4 mortars unless they have gametype hq.
All maps, except mp_carentan, will have 2 mortars when gametype is hq.
The map_carentan will have 3 mortars for all gametypes except for gametype hq where there will be
only 1 mortar.


Know Issues
-----------


Changes
-------
3.0 beta 10b
	Added features
	- Added falldamage cvars
	- Added turret overheating

	Changed stuff
	- Changed turret disabling to use different cvars for MG42 and 30Cal

	Fixed issues
	- Minor bugfix with tripwire and non-team based gametypes
	- Hopefully fixed rare script error while sprinting

3.0 beta 10
	Added features
	- Added option to not show scorelimit on hud (like before 1.2 patch)
	- Added option to force number of grenades or even make them random
	- Same thing for smoke grenades
	- Added dvars to force specific primary and/or secondary weapons
	- Added dvar to disable turrets

	Changed stuff
	- Made separate tripwire defuse times for same team and other team tripwires.

	Fixed issues
	- Minor bugfix with spawn protection headicon and non teambased gametypes

3.0 beta 9
	Added features
	- Added dvar to force auto-assign

	Fixed issues
	- Fixed headicon for spawnprotection to no longer be seen through buildings and stuff

3.0 beta 8
	Redesigned stuff
	- Made sprint speed configurable with dvar
	- Made grenade cooking configurable with dvar (as suggested by shooter, original idea by Filbert)
	- Made colored smoke nades configurable with a dvar
	- Localized more strings
	- Shortened the fs_game folder name to minimize the risk of iwd name/sum errors.

	Added features
	- Spawnprotection (NOTE! Headicon will be seen through anything, use with caution, next version will fix this)
	- Added cookable grenades with shorter throw distance (75 and 50 percent of the original distance)
	- Added selectable secondary weapon

3.0 beta 7
	Fixed issues
	- Fixed a check in _teams.gsc that didn't recognize lms and ihtf as non-teambased gametypes
	- Fixed score hud notifies in custom gametypes

	Redesigning
	- Reverted to using unpacked files on server again since it offer more flexibility.
	- Localizing some strings
	- Created 18 different clientside mods to minimize the number of .iwd's to one.

	Added features
	- Added serverinfo pages for custom gametypes
	- Added option to disallow sprinting while carrying flag, as suggested by La Truffe

	Updated gametypes
	- Individual Hold the Flag updated with new version

3.0 beta 6
	- Updated to support Call of Duty 2 version 1.2

3.0 beta 5c <never released>
	Fixed issues
	- Minor bug fixes

	Added more features
	- Included a modded version of the main menu the re-enabled the "Mods" menu.

3.0 beta 5b
	Fixed issues
	- Fixed issue with tripwires not giving score in DM.
	- Fixed a minor sprinting bug.
	- Fixed minor bug with crush punishment.

	Added more features
	- Added dvar to disable/force crosshair names.
	- Added dvar to control respawn delay in HQ and CTF
	- Added CTF sounds to HTF. Credits go to Ruud.
	- Added updated anti exploit code from Innocent Bystander
	- Added new non-team-based gametype Last Man Standing(lms)
	- Added dvars to give score for planting/defusing in SD.
	- Added another non-team-based gametype Individual Hold the Flag (ihtf)

3.0 beta 5
	Fixed issues
	- Added a level check for the tripwire warning as suggested by satyr.
	- Changed tripwires to use the USE/Activate button to avoid conflicts when steadying sniper rifle
	- Minor tweaks to sprinting code
	- Tweaked map voting (thanks #7 for the idea)
	- Fixed stock bug where weapon swap was allowed after using grenades during the graceperiod
	- Changed LTS so that the team with most alive players when the round time runs out wins the round

	Added more features
	- Updated clientside .iwd with soundaliases for helmet bounce sound.
	- Added dvars to give unlimited ammo, grenades and smoke grenades.
	- Added the possiblity to specify several crushmodels from which a random one will be picked.
	- Made the crush object go back to where it came from after a timeout.
	- Added weapon limiting
	- Added dvar to force certain "exploitable" clientside dvars to their default valies.
	- Added respawn delay dvar for HTF.
	- Added dvar to force speeding up the fading of the red compass dots.
	- Added laserdot.

3.0 beta 4b
	Fixed issues
	- Fixed issue with updating healthbar when there is no attacker
	- Fixed issue with tripwires, dupecheck and healthpacks not working unless showteam status was enabled

	Added more features
	- Added another punishment for teamkilling

3.0 beta 4
	Redesigning
	- Lots of internal rearranging of the code
	- Tweaked the getstance function a little

	Fixed issues
	- Removed potato from sprint weapon
	- Fixed issues with healthbar not always updating
	- awe_objective_icons now affects ctf and htf aswell

	Added more features
	- Added dvar to disable health regeneration
	- Added healthpacks
	- Added mortars
	- Added tripwires
	- Added random flag spawns for htf
	- Added dvar to remove CoD2 teamscore hud for HTF.
	- Added efog overriding
	- Added a dvar for removing bodies quicker than normal
	- Added a dvar to sink the bodies into the ground before removing them

3.0 beta 3
	Redesigning
	- Changed the clientside mods so that only 1 or 2 .iwd files are needed.

	Fixed issues
	- Includes the updated sprint code from 3.0beta2c.
	- Removed an the anchor entity from bounced objects once they stopped bouncing to reduce gamestate size.
	- Made sure random maprotation and fix maprotation do not exceed the maximum string size (which did crash the server)
	- Fixed issue with the dupecheck which did not work unless the team status was enabled.

	Added more features
	- Added dvar to disable weapon drop on death
	- Added dvar to disable grenade drop on death
	- Added dvar to disable pistols
	- Added dvar to disable binoculars
	- Added dvar to disable shellshock
	- Added dvar to disable HUD scores
	- Added dvar to disable objective points
	- Added dvar to disable damage feedback
	- Added dvar to disable/force crosshair
	- Added dvar to disable/force the crosshair enemy color switch
	- Added dvar to override gravity
	- Added dvar to override speed
	- Added Unknown Soldier handling
	- Added blood splatter on screen
	- Added cold breath on winter maps

	Included external mods
	- Added DaveWs colored smoke grenades as an option.
	- Added Anti Exploit mod 1.0

3.0 beta 2
	Redesigning
	- Unpacked awe.iwd to avoid problems and to prevent unnecessary downloads
	- Removed _customlogo.iwd since it isn't needed after unpacking awe.iwd
	- Kept client mod names to minimum to avoid crossing a limit built into CoD2

	Fixed issues
	- Fixes errors in readme and awe.cfg.
	- Removed the first show team status alternative.
	- Tweaked the sprinting to avoid picking up weapons and fixed some bugs.

	Added more features
	- Random maprotation
	- Maprotation error correction
	- Painsounds
	- Deathsounds
	- Checking and renaming of duplicate player names
	- Disable deathicons
	- Disable nadeicons
	- Headpopping
	- Helmetpopping
	- Gametype Retrieval
	- Damage modifiers
	- Sprint speed tweakable

	Included external mods
	- Included bloodmod
	- Included color smoke grenade mod


3.0 beta 1
	Initial release for Call of Duty 2 with a limited set of AWE features
	- Teamkill detection with different punishments.
	- Server messages
	- Welcome messages
	- Disable minefields
	- Server/Clan logo under compass
	- Sprinting
	- Map voting
	- Customizable health regeneration
	- Customizable killcam time
	- Healthbar
