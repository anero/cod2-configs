La Truffe presents : AWE v3.4.2


++ Object

AWE mod version 3.4.2 for COD2 multiplayer.


++ Added/changed features since 3.0 beta 10b

AWE v3.4.2 :

- as requested by ub_dragon : new option to have an extra points multiplier for making a headshot, with dvar awe_points_headshot_x ; if this dvar exists, awe_points_headshot will be ignored

- new dvar : awe_points_headshot_x


AWE v3.4.1 :

- new option for the secondary weapon slot disabling : players may pick up a new weapon

- frag and smoke grenades count can now be set to 0, thus you can remove grenades for some or all weapons

- workaround to prevent the "dobj for xmodel 'xxx' has more than 127 bones" client error when unfixing a turret

- fix : fatal script error when both awe_tripwire and awe_grenade_explode_contact are set to "0"

- fix : grenade (frag and smoke) count overriding not working for the SVT40

- fix : player dying when fixing/unfixing a turret leaves 2 resp. 0 turrets

- fix : clan password screen not displayed when awe_clan_reserveslot is set to "0"

- fix : fx removal not working after warmup or next round

- fix : fx removal not removing sound fx

- fix : admin command rename does not take the full name if it contains space characters

- fix : player invisible after changing team while in the parachute landing point selection screen

- dvars with new values : awe_disable_secondary, awe_grenade_count, awe_smokegrenade_count

- new dvars : none


AWE v3.4 :
- grenade count is now configurable per weapon as well as globally
- quieter tripwire plant/defuse sounds
Now they sound just like they did in AWE v2.
- extra points awarded for killing with a certain weapon (per weapon type, not per individual weapon)
- fx removal : you can remove any fx loaded by the map script, for example remove dust ; see "fx removal" in awe.cfg
- secondary weapon slot disabling : will prevent players from picking up another weapon
- option to fix/unfix turrets ; see "Turret options" in awe.cfg
In AWE, there are 2 kinds of turrets : fixed turrets and mobile turrets.
Fixed turrets are those initially placed by the map maker at strategic locations.
Mobile turrets are machine guns deployed by players.
Now deployed turrets can be fixed : when a player fixes a turret, he will leave the turret where it's deployed, losing it as a weapon.
And fixed turrets can be unfixed : when a player unfixes a turret, he will take the weapon with him, losing his current weapon.
A turret can be fixed then unfixed then fixed again, and so on.
Fixed turrets have unlimited ammo, whereas mobile turrets have limited ammo. This is far from optimal but it was like that in AWE v2 so I guess we can live with that...
- option to make frag grenades explode when entering in contact with any object or player
When this option is enabled (dvar awe_grenade_explode_contact), a player can choose to make the grenade explode on contact by pressing the Use key when throwing it.
The grenade will not bounce but instead explode when entering in contact with any solid object, for example another player !
Otherwise, the grenade will explode after its regular fuse time.
WARNING : this option can stress your server if a lot of players throw a lot of grenades simultaneously.
- option to make tripwires explodable with frag grenades (dvar awe_tripwire_nade_explode)
Now you can get rid of those nasty tripwires by blowing them !
WARNING : this option can stress your server if a lot of players throw a lot of grenades simultaneously.
- option to limit the number of thrown smoke grenades (see new dvars in "Weapon and grenade options")
If you set a limit, only a maximum number of smoke grenades can be thrown simultaneously.
Any additional thrown smoke grenade will be removed and given back to its launcher.
You can also control the duration to take into account, if you don't want to wait for the smoke to dissipate completely before allowing a new one.
WARNING : this option can stress your server if a lot of players throw a lot of grenades simultaneously.
- new admin command "rename" : will rename a player
- additional check to prevent deployment of a mobile turret on a too much inclined ground
- force player to leave turret when attacking a spawn protected player (awe_spawn_protection_punish set to "1")
- force player to leave turret when disarmed with admin command "disarm"
- force player to leave turret when bash mode enabled
- HM : the Group Commander can no longer go spectator, to avoid losing the Commander completely
- IHTF : new dvar to set a maximum distance the players will spawn from the flag ; now there is a minimum and a maximum distance as well
- HTF : new dvar to set a maximum distance the players will spawn from the flag ; now there is a minimum and a maximum distance as well
- fix : weapon limiting
Let's be honest, weapon limiting was not working very well for quite a while.
Hopefully, it now works as it should, and does not re-allow weapons that have been explicitly disallowed by the admin.
- fix : allies are always american if scr_allies is not set
- fix : bash mod broken
- fix : grenades not removed in bash mode
- fix : some fundmod powerups not working at all (fast, slow, lowgrav, invisibleweapon)
- fix : some funmod powerup effects causing problems if the round or map ends in the meantime (wabbit, crazyshooter, fast, slow, lowgrav)
- fix : sniper range finder only working when adjustable zoom enabled
- fix : extra points awarded for making a headshot or bashing an enemy not accounted in round based gametypes
- fix : in some gametypes, if the dvar awe_parachutes_only_attackers is set to "1", only allies are able to parachute whereas there are no defenders and no attackers
- fix : anti-camping enabled by default, now is disabled
- fix : awe_clan_team option not working if awe_allow_team_select is set to "0"
- fix : fatal script error if anti teamkilling is disabled (awe_teamkill_max set to "0")
- fix : some messages are not displayed on Linux server in CNQ, CTF, DM, HQ, LMS, LTS, RE, SD and TDM ; this is a stock COD2 bug !
- fix : in VIP, impossibility to select a MG as primary weapon


AWE v3.3 :

- extra points awarded for making a headshot or bashing an enemy (dvars awe_points_headshot and awe_points_bashkill)
- option to disable vote kick in the standard in-game voting menu (dvar awe_ingame_vote_allow_kick)
- new option in the anti-dbbh to prevent disabling the weapon when the player steps over a little obstacle (dvar awe_anti_dbbh_jump_height)
- new admin command "crush" : will drop an object on the player
- new anti-camping punishment ("8" = crush : will drop an object on the player)
- configurable ammo for mobile turrets (dvars awe_mg42_ammo and awe_30cal_ammo)
- ammo limiter configurable per weapon as well as globally
- reduced default zoom level for scoped G43, now can zoom in and out like other sniper rifles
- range finder for sniper rifles (dvar awe_sniper_rangefinder)
- fog settings can now be changed on the fly during game without having to restart the map (dvar awe_efog_cycle)
- option to display only one random welcome message instead of all messages (dvar awe_welcome_random)
- option to slow down bots (dvar awe_bots_slow) ; only useful for testing purposes !
- more maps configuration for BT/DOM/ONS gametypes
- CTFB : in random flag positions mode, minimum distance between the flag bases is configurable (dvar scr_ctfb_random_flag_distance)
- ESD : ability to use other spawn points than SD spawn points (dvar scr_esd_spawnpoint)
Some players noticed that the standard SD spawn doesn't fit very well when respawn is activated because in this case :
1) The SD spawn points are too close to each other, which encourages spawn camping,
2) The defenders spawn points are often located very close to the objectives, which is a real pain for attackers.
So now, server admins can set another spawn type in ESD.
The values for scr_esd_spawnpoint can be :
+ "best" : then the script tries CTF, TDM, DM and then SD spawn types in this order. The first which is compatible with the current map is selected.
+ "ctf" : this forces the CTF spawn type to be selected.
+ "tdm" : this forces the TDM spawn type to be selected.
+ "dm" : this forces the DM spawn type to be selected.
+ "sd" :this forces the SD spawn type to be selected (default)
- new clan option : clan password (dvars awe_clan_password and awe_clan_password_timeout)
The server admin can set up a password for his clan. This password can be any string composed of up to 30 alphanumeric lowercase characters.
Upon connection to the server, players will have the ability to enter the clan password. If it matches the server's clan password, they will be considered as clan members.
Players will have 3 attempts max within a limited time, to prevent them from staying in the password screen with no user interaction.
The clan password can only be entered upon connection ; players who could not enter the password for some reason will have to reconnect to the server.
The clan password method overrides the clan tag identification method ; this way, any player entering the correct password will be a clan member, regardless of his player name.
However, if no clan password is defined, the clan tag identification stays active.
The clan password method is a lot more secure than the clan tag identification method, as any player can change his name easily to match the clan tag.
Bear in mind that this password is managed by AWE, it has nothing to do with server password (g_password) or private slot password (sv_privatepassword) that are managed by the game itself.
- parachuting
Players can parachute to their spawn point when they spawn or respawn.
They also have an option to select a landing target among several allowed spawn points chosen randomly.
Beware that this will override the spawn logic of the gametype ! (example : in HTF, the player may land directly on the flag if the flag has not been picked yet)
During parachute flight, you won't see objects/players and won't hear any game sound until you reach a certain height. This is because of the low sky on some maps : until you get below the sky level, you're considered as being out of the map.
See awe.cfg for dvar configuration.
- funmod
The funmod is an add-on aiming to bring more fun to the gameplay.
It's only meant for fun, without the slightest care for realism.
Admins seeking the ultimate realism for their server had better skip it completely, the funmod is definitely not designed for them !
The funmod is compatible with every gametype and every map that provides DM or TDM spawn points, that is to say the majority of maps.
It should not interfere with other AWE features ; however, please report any unexpected behavior you may find.
It's based on very classic game widgets : powerups.
Powerups randomly spawn into the map.
When picked up, they give the player the ability to trigger a special effect.
Powerups have a time out and will reappear elsewhere if not picked up.
Powerups can be made visible on the compass.
There are 5 types of powerup effects :
+ "level" type powerup : its effect is global, and the player can trigger it at any time ; only one level powerup can be activated at a time to avoid compatibility issues
+ "good" powerup : the player can activate it at any time, and its effect will be applied on himself and hopefully will be "good" for him...
+ "bad" powerup ; the effect applies on the player after 3 seconds and will do something not so good to him...
+ "target" : the player has to target a victim at any time and will trigger the effect on the targeted victim
+ "super" : the player activates it at any time and it will be applied to all enemies, whether the gametype is team based or not
+ "wicked" : activates after 3 seconds and will have an effect on all players !
Some powerups, by essence, are level wise. Other can only be of the "target" or "good" type.
But most powerups can be either "bad", "target", "super" or "wicked" ; these are called "multi typed".
You won't know the nature of a powerup and its effect type until you pick it up, so do it at your own risk !
The nature is in fact random.
However, you can configure the list of powerups you want to enable. This way you can avoid those you don't want on your server. And there's no doubt you will absolutely hate some of them ;-)
For multi typed powerups, the effective type is random too, but the server admin can configure the probability for a multi typed powerup to be each one of the 4 types.
A player can pick up only one powerup at once. If not activated, he will keep it until he dies. Basically, he cannot get rid of it.
Powerup effects are either applied once (in one shot) or continuously during a configurable time (or until the victim dies), depending on the nature of the powerup.
When under the effect of a powerup, a player cannot pick a powerup, he has to wait for the effect to stop, if not lethal...
A player is allowed to pick up a powerup only after a configurable delay after spawning, even if he spawns directly on a powerup.
The funmod tweaks dvars and commands at the client side. Experienced players could manage to abort some powerup effects by issuing commands on their client console ; to avoid this you may want to disable the client console by setting sv_disableClientConsole to "1" in your server config.
You may have to adapt your Punkbuster configuration if it checks client dvars.
By the modularity of its implementation, the funmod can be extended with new powerups pretty easily. 
This initial version comes with 25 defined powerups, but we're open to suggestions for new ones, especially the craziest !
Check awe.cfg for additional info and dvar configuration.
- fix : script error if using tripwires when allies are different than the ones defined in the map script (by setting dvar scr_allies)
- fix : wrong message displayed when using admin command "crash"
- fix : overheating sometimes triggering when firing weapon while being close to a fixed turret
- fix : fixed turrets non overheating in some custom maps ; now AWE uses a much more reliable method to detect whenever a player is using a fixed turret
- fix : placement of some HUD items on wide (non 4/3) screen resolutions : AWE version logo, server logo, sprint bar, sprint hint, health bar, spawn protection cross, number of dead players, round timer and round count in BT/DOM/ONS, team flags in ECTF, radio and number of players to capture in EHQ, icons and instructions in HM, duel HUD in LMS
- fix : better detection of the prone position in the anti-dbbh, thanks to dorian_rast
- fix : in ESD, no more free spectating during spawn delay after the end of the 1st round
- fix : non clan member can escape kicking if map or round ends just before he is supposed to be kicked


AWE v3.2.2 :

- vanishing tripwires : tripwires can vanish or auto-explode after a time out
Configured by dvars awe_tripwire_vanish and awe_tripwire_vanish_time.
- invisible spawn protection : can make a player invisible to other players during spawn protection
Particularly useful in maps that provide very few or packed spawn points.
Configured by dvar awe_spawn_protection_invisible.
- adjustable zoom for sniper rifles
With this option, sniper rifles will be equipped with 4 extra zoom levels.
While aiming down the sight, pressing the Melee key will zoom in and pressing the Use key will zoom out.
Note that the scoped G43 sniper rifle will have no extra zoom in, only zoom out.
Can be configured separately for each sniper rifle (5 dvars).
- more maps configuration for BT/DOM/ONS gametypes
- fix : some functions (like sprint, mobile turret deployment) not working just after starting next round in round based gametypes
- fix : various script errors with mobile turrets, mobile turrets sometimes overheating as soon as deployed
- fix : mobile turret not always auto-used if the player is holding the Use key pressed
- fix : weapon limiting not working with panzerschreck/panzerfaust and mobile turrets
- fix : weapon disabling sometimes not working with deployed turret, same for "disarm" admin command


AWE v3.2.1 :

- overheating on mobile turrets just like fixed turrets
- awe_anticamp_turret now applies to mobile turrets like fixed turrets
- 2 new custom compass models
The compass model is selectable via dvar awe_compass_model.
- BT, DOM, ONS : can use pre-defined flag definitions in the map script
Mappers can pre-define flag definitions in their map.gsc, then BT, DOM and ONS will use them.
- fix : cannot deploy machine guns when admin commands are disabled (awe_admin_commands = 0)
- fix : weapon limiting not working in AWE 3.2
- fix : script error when using punishment method 6 for campers (explode)
- fix : red dots erroneously disabled even in b0, b1 and b2.iwd
- fix : blood mod version 2 erroneously present in a0 and b0.iwd
- fix : sound of reloading panzerfaust and panzerschreck can be heard from anywhere in the map
- fix : sound of placing and pickinp up of mobile turrets can be heard from anywhere in the map
- fix : overlapping pictures in the russian weapons menu
- workaround to prevent the "dobj for xmodel 'xxx' has more than 127 bones" client error
When mobile turrets are enabled, the russian player model "coats" is replaced by "padded" and the german player model "winterdark" is replaced by "winterlight", regardless of the map setting.
These models ("coats" and "winterdark") are known to crash the client game when a player switches to a MG.
This workaround will prevent crashes until a real solution is found, maybe one day...
- HQ, EHQ : fix bad handling of scr_forcerespawn, generating script errors
- HTF : fix crash when starting the server in Brecourt


AWE v3.2 :

- 5 new weapons : Scoped Gewehr43, Panzerschreck, Panzerfaust, M1919A6 .30cal, MG42
The scoped G43 is available in the german weapons menu.
Allies can select the M1919A6 .30cal machine gun, while axis can select the MG42.
The panzerschreck and panzerfaust are available to allies as well as axis.
The panzerfaust behaves exactly like the panzerschreck : you have 10 rockets and it reloads automatically.
The M1919A6 .30cal and MG42 turrets (machine guns) must be planted before being fired. Planting is done by aiming down the sight (a la COD/UO).
Planting and picking times can be configured separately (see "Turret options" in awe.cfg).
Machine guns don't need reloading, they are equipped with a 250-round belt that cannot be changed. However, ammo can be picked up just like with any other weapon.
- alternative weapons menu allowing selection of all available weapons from all 4 nationalities
The standard weapons menus can be replaced by an alternative menu showing all available weapons in the game (all stock weapons including pistols and the 5 new ones).
- announcer module
Some events can be announced with a visual message and/or sound : headshot kill, headbash kill, multi-kill, killing spree, first blood, end of match victory/defeat, end of match countdown, camping, team killing.
Announcer sounds come from UT2004.
- better resistance to players running external unsupported weapons mods
This should avoid script errors or server crashes when players are running external weapons mods sitting silently in their main directory.
- server logo file (_awe_server_logo.gsc) moved out of the server IWD, for easier customization
- all dvars can now be overridden for specific maps and/or gametypes
This applies to all AWE dvars (awe_<var>), all gametype dvars (scr_<gametype>_<var>), and the following standard COD2 dvars as well :
g_allowvote
scr_allies
scr_drawfriend
scr_friendlyfire
scr_killcam
scr_spectateenemy
scr_spectatefree
scr_teambalance
and all scr_allow_<weapon> dvars
See note on dvar overriding below.
- fix : awe_sniper_limit not working well for british team
- fix : CoD2maps.arena (all gametypes except CNQ and LIB)
- fix : script error in BT, DOM and ONS when awe_hud_score is set to 0
- fix : forcing primary and secondary weapon not working in SD and ESD
- fix : in ESD, wrong round count when team swap is enabled
- fix : tripwire planting and defusing sounds not playing
- CNQ : changed dvar scr_show_obj_hud to scr_cnq_show_obj_hud
- ECTF : changed dvar scr_objectiveicon to scr_ectf_objectiveicon
- ESD : change in the team swap option
When teams swap, they swap their side and role, but players no longer change team. This allows to be an attacker or defender while staying in the same team throughout the whole match.
Plus, it's now possible to specify every round after which teams will swap, not only a single round.
You can then decide to swap only once, or after each round, or every 2 rounds... as you like.
- ESD : added the option to make defenders respawn with an extra delay penalty (similarly with EHQ)
Defenders always respawn very close to the objectives, so this gives an extra chance to attackers when defenders are able to respawn.
- RE : compatibility with all stock maps + more than 100 custom maps (kudos to =G4C=Dude4Him !)


AWE v3.1 :

- better handling of incompatible gametype and map, with a fallback gametype/map
When an incompatible gametype/map is detected, the server no longer switches to DM with players stuck into spectators.
Instead, the current rotation item is skipped and the rotation continues on the next item.
When not using a rotation, the server switches to the gametype and map specified by the dvar awe_fallback_gametype_map.
- new option for spawn protection, allowing to punish a player attacking a protected player
A player attacking a spawn protected player can be punished : drop weapon, reflect damage or suicide.
This is controlled by dvar awe_spawn_protection_punish.
- new custom gametype : LIB (Liberation)
AWE now has 21 gametypes ! (5 standard, 16 custom)
- CTFB upgraded to 1.3 (bug fix)
- HTF upgraded to 1.1 (new options !)
- IHTF upgraded to 1.4 (bug fix)
- VIP upgraded to 1.4 (bug fix)
- more localized text
- more maps configuration for BT/DOM/ONS gametypes
- clan options : move clan members to the same team and non clan members to the other team, reserve a server slot to ensure priority of clan members over non clan members
- new option allowing players to safely jump over tripwires (dvar awe_tripwire_jump)
- anti camping
- fix : CNQ reference removed from CoD2maps.arena


AWE v3 CE :
- new client mods with red dot on compass disabled when enemy fires
- new custom gametypes : BT, CTFB, CNQ, DOM, ECTF, EHQ, ESD, HM, ONS, VIP, totalling 20 gametypes !
- upgraded gametype : IHTF (1.3)
- Lee Enfield selectable from American weapons menu
- warmup delay
- anti dive bomber & bunny hopper
- next map voting extension
- new option in the ingame vote menu allowing to choose from all available gametypes
- new option in the ingame vote menu allowing to choose from all available maps
- new option in the ingame menu allowing to display the serverinfo screen
- admin commands
- bash mode
- fix : can no longer place tripwire when standing at spawn
- fix : turret temperature bar moved a little higher to avoid overlapping with server logo, localized string for overheating message
- fix : AWE bots now working when secondary weapons enabled, some runtime errors corrected
- optimized handling of serverinfo dvars, to completely avoid "SV_SetConfigValueForKey: overflow" error
- new options for team killing punishment : kick player, freeze controls during 1 minute


++ Note on the new custom gametypes

ECTF, EHQ and ESD are extensions of the stock CTF, HQ and SD gametypes respectively, with lots of customization and new features.
ESD brings features similar to the famous RSD gametype for COD1.

CTFB is CTF with a twist, which leads to interesting gameplay.

CNQ is the famous Conquest TDM gametype ported to COD2.

HM and VIP are role based gametypes, where certain players are the targets to reach. VIP is team oriented, whereas HM has no team.

DOM is a re-creation of the DOM gametype in COD/UO, with new features.
BT and ONS are variants of DOM, with important changes in the number and order of objectives.
For those familiar with COD3 on consoles, BT is the equivalent of the WAR gametype in COD3, but much better of course ;-)

CNQ and LIB need maps specially designed to support these gametypes.
BT and ONS need maps configuration data from a configuration file. AWE provides a default file with a selection of custom maps. DOM can also benefit from this file. 


++ Compatibility

COD2 1.3 only.
It's recommended to start a modded server as dedicated, although AWE should work fine on listen servers too.


++ Installation : from scratch

The installation of AWE v3.4.2 is the same as for AWE 3 beta 10b, and only differs by the following :

1. The package is available in a zipped form only.
There is no longer an installer for the Windows platform.
The install method is thus the same for all platforms (Windows, Linux, Mac OSX).

2. The client part is now available in 6 different versions instead of 3.
The original b0.iwd, b1.iwd and b2.iwd are still there unchanged.
Three new ones (a0.iwd, a1.iwd and a2.iwd respectively) are identical to their b counterpart with the only difference that they have the red dots on compass disabled when enemy fires.

Here is a summary of their features :
a0 = no blood mod + red dots on compass disabled
a1 = Blood mod version 1.0 (unrealistic) + red dots on compass disabled
a2 = Blood mod version 2.0 (realistic) + red dots on compass disabled
b0 = no blood mod + red dots on compass enabled
b1 = Blood mod version 1.0 (unrealistic) + red dots on compass enabled
b2 = Blood mod version 2.0 (realistic) + red dots on compass enabled

Use only 1 of these client parts !

3. The server part of the mod is no longer presented as flat files but in a single IWD, except for the server logo.
Server admins seeking further control can still uncompress it into files and folders.
When uncompressing, be careful to remove the blank gametype scripts (maps\mp\gametypes\*.gsc) in the client part IWD, otherwise the game will load them first and AWE won't start. Doing this will cause the loading screens to show the gametypes with a short name (eg "htf" instead of "Hold the Flag").
The server part (z_awe_svr_3.4.2.iwd) has to be placed in your fs_game folder, just like one of the client parts (a*.iwd or b*.iwd).
The server logo directory and file (server_logo\_awe_server_logo.gsc) have to be placed in your fs_game folder. You may edit this file to customize your logo (see instructions in awe.cfg).

Quick setup procedure :
- create a new folder (will be "your fs_game folder")
- select 1 of the 6 client IWDs (a0, a1, a2, b0, b1, b2) and put it into your fs_game folder ; put only 1 file !
- put the server part IWD into your fs_game folder
- put the server_logo folder and its content (1 sample file) into your fs_game folder
- put all sample config files (.cfg) into your fs_game folder
- put the scriptdata folder and its content (2 sample files) into your fs_game folder
- create a general config file for your server ; make sure it will call all the config files you need (awe.cfg + the specific config files for all gametypes you wish to run)
- edit the config files according to your needs ; be careful that all dvars definitions are initially commented out in awe.cfg, so you have to remove the comments in front of options you want to change
- create a server startup command-line (batch file, shortcut...) with at least arguments +set fs_game <your fs_game folder> and +exec <your general server config file>


++ Installation : upgrade from AWE version 3.4 or 3.4.1

The client part is the same as AWE 3.4 or 3.4.1.
You only have to replace your server part IWD or uncompressed server files.


++ Installation : upgrade from an older AWE version (3.3 and earlier)

You need to remove the previous version IWDs before copying the new ones.
The same for uncompressed server part files.
Several versions of the mod cannot coexist in the same fs_game folder.
If you want to be able to run different versions, use different fs_game folders.


++ Configuration

The dvars from AWE 3.0 beta 10b have been kept intact.
New dvars have been introduced to configure the new options.
Please refer to the bottom part of the sample awe.cfg, as well as all the separate gametype specific configuration files.
Bear in mind that in the sample awe.cfg all dvars definitions are commented out initially, so if you make a change be sure to have the dvar definition uncommented !

Several weapons configurations are provided as examples if you want to restrict the choice to a certain type of weapons (weapons_xxx_only.cfg).


++ Note on dvar overriding

dvars can be made specific to gametypes and/or maps by adding the gametype and/or mapname to the dvar name.

Example :

set awe_mortar_hq_mp_carentan "1"		// will override
set awe_mortar_hq "2"								// which will override
set awe_mortar_mp_carentan "3"			// Which will override
set awe_mortar "4"

In the above example all maps, except mp_carentan, will have 4 mortars except in the hq gametype.
All maps, except mp_carentan, will have 2 mortars in the hq gametype.
The map mp_carentan will have 3 mortars for all gametypes except for gametype hq where there will be only 1 mortar.


++ Credits

All inherited functions from AWE 3.0 beta 10b : Bell - see specific readme
Compass red dots remover : Bullet-Worm
Lee Enfield for American : La Truffe - based on a mod by Bully & Shooter
Anti dive bomber & bunny hopper : La Truffe - based on the implementation in Astoroth's eXtreme+ mod + enhancement suggested by dorian_rast
ECTF gametype : 0ddball and Shooter - based on CTF additions in Bullet-Worm's Powerserver mod
DOM gametype : Matthias, Tally "the Forger", 0ddball and La Truffe - see specific readme
BT and ONS gametypes : 0ddball (mostly) and La Truffe (a tiny bit) - see specific readme
CNQ gametype : Tally "the Forger" and UncleBone - see specific readme
HM gametype : Tally "the Forger" - see specific readme
ESD gametype : La Truffe - includes modifications from #7's COD2Svr mod - see specific readme
CTFB gametype : La Truffe - based on the gametype from Matthias' Admiral mod - see specific readme
Admin commands : #7, from COD2Svr mod, with additions by La Truffe
Bash mode : #7, from COD2Svr mod
LIB gametype : [HI]DW, with minor changes by La Truffe
Panzerfaust, M1919A6 .30cal, MG42 weapons : inspired by Merciless2 mod
Pistol images : |IÐ|TopGun|Co, from his All Weapons Mod
M1919A6 .30cal and MG42 images : Matthias, from Admiral mod
RE gametype enhanced map compatibily : =G4C=Dude4Him
Announcer sounds : from UT2004 (C) Epic Games, Digital Extremes, Atari
Compass models : COD1 compass models by flakrider (custom 1) and BNPK (custom 2)
Invisible spawn protection : idea from {ASP}SniperOne
Method to check usage of a fixed turret : uses a suggestion by Wanna Ganoush
Parachute model : Matthias, from Admiral mod
Ideas for some new features : various RGN members
Idea for headshot extra points multiplier : ub_dragon
All the rest : 0ddball and La Truffe


++ Donations

If you want to support the mod, you may contribute with a Paypal donation : https://www.paypal.com/cgi-bin/webscr?cmd=_xclick&business=latruffe666%40gmail%2ecom&item_name=Donation%20for%20AWE%20mod&no_shipping=0&no_note=1&tax=0&currency_code=EUR&bn=PP%2dDonationsBF&charset=UTF%2d8
However, AWE v3 will always remain free, of course !


++ Contact

My AWE support forum : http://awemod.free.fr
Nedgerblansky a.k.a. La Truffe : latruffe666@hotmail.com or latruffe666@gmail.com