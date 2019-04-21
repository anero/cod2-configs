Individual Hold the Flag (IHTF) : a gametype for COD2
Version : 1.4
Author : La Truffe (latruffe666@hotmail.com)

++ Credits

Bell : HTF gametype
Ravir : cvardef function

++ History log

1.0
- initial version
- minor bug fixes and some minor tweaking by Bell before including it in AWE

1.1
- force some printed text in white color in case player names include color codes
- add a time out for stealing the flag, controlled by scr_ihtf_flagtimeout ; after this delay the flag respawns elsewhere
- force players to spawn away from the flag, at a minimum distance controlled by scr_ithf_spawndistance
- remove cvar scr_ihtf_removeflagspawns

1.2
- enable scr_ihtf_pointsforkillingplayers to be negative, to be able to penalize players killing non flag carriers
- make use of all spawn points available in the map, as well as CTF flag positions, SD bomb zones and HQ radio positions ; 2 new dvars : scr_ihtf_playerspawnpointsmode and scr_ihtf_flagspawnpointsmode
- flag time out applies also when flag has been dropped - not only when flag is at base
- all printed text is localized
- more informative serverinfo screen
- fixed flag base visibility
- compatibility with eXtreme+ mod

1.3
- fixed bug in the serverinfo screen (AWE and standalone versions only)
- fixed bug where HUD score was not updating
- optimized handling of serverinfo dvars, to completely avoid "SV_SetConfigValueForKey: overflow" error (AWE and standalone versions only)
- fixed visibility of some displayed messages
- when scr_ihtf_pointsforkillingplayers is negative, the flag carrier will not be penalized when killing other players
- scr_spectatefree and scr_spectateenemy now supported

1.4
- fixed typo in dvar scr_ihtf_spawndistance (was scr_ithf_spawndistance before)

++ Object

IHTF is based on the famous HTF gametype.
For those familiar with HTF, IHTF is a mix between HTF and DM.
Basically, it is like HTF without teams, or DM with an objective (the flag).

The object is to get the flag, which spawns randomly, and hold it as long as possible.

The flag holder scores 3 points every 30 seconds by default.
The flag is always marked on the compass.

The first player that reaches the score limit wins.
The player with the best score at time limit wins.

Any player can kill any other player, being the flag holder or not.
However, killing the flag carrier, stealing the flag and holding it earns more points.

If the flag has not been stolen within a time limit, it will respawn elsewhere. This in case it may become unreachable to players.

++ Compatibility with COD2

COD2 1.3
Do NOT try it on older versions, it will probably not work well, if working at all.

++ Compatibility with mods

This is a standalone mod.
It is already integrated in AWE mod (Community Edition version) and eXtreme+ mod.
For other mods an adaptation may be needed.

++ Compatibility with maps

IHTF 1.3 is able to create player spawn points and flag spawn points from the following entities defined in maps :
- DM, TDM, CTF, SD spawn points
- CTF flag positions
- SD bomb zones
- HQ radio positions
This is configurable by 2 dvars.

This makes IHTF COMPATIBLE WITH EVERY COD2 MAP CREATED ON EARTH !!

However, compatibility does NOT guarantee it will be enjoyable in all maps.
For example, sniper maps usually have 2 areas separated by a non crossable frontier. IHTF will work on those maps but the gameplay will be pretty dumb.

++ Installation / uninstallation

The mod has a client and a server part. It cannot be made server-side only because it contains client files. However, the client part is ridiculously small.
It's available with separate client and server IWDs, as well as a combined client + server IWD.

To install, put the client and server IWDs in your fs_game folder.
On your redirect space, put only the client IWD that will be downloaded by players.

You may also want to combine the client part with another client mod, the same for the server part. It should not be a problem, as there are only new files, no existing file has been modified.
This is the preferred method to avoid the painful "Info string length exceeded" error.

To uninstall, just remove the client and server IWDs ; now that's an uninstallation procedure !

++ Configuration

Please see the sample ihtf.cfg for a description of the new dvars, and a note about dvar overriding.
Copy/paste the desired dvars in your config file or make it execute ihtf.cfg, and set g_gametype to ihtf in your config file.

++ Limitations / problems

The mod does not include configuration options from a listen server ; please use a dedicated server instead, listen servers are known to be mods unfriendly anyway.

IHTF being an additional gametype, it may not be possible to vote for this gametype with the standard voting option. This is a known COD2 limitation, and there's little we can do for that. Also, custom maps won't be showing on the menu if you select IHTF, even if they actually work fine with IHTF.

The client and server part of the mod both include a file with the same name (ihtf.gsc) : this is intended ! on your server, you have to make sure that the server part will be read before the client part. A way to achieve this is to keep the file names intact. Remember that COD2 loads files in the inverse alphabetical order ; zzz_ihtf_svr_1.3.iwd will be read BEFORE zzz_ihtf_cli_1.3.iwd, so in the server the correct ihtf.gsc will be loaded (from the server IWD) and the blank one (from the client IWD) will be ignored.

You may find in your server log lines such as "WARNING: Spawn point entity 683 is in solid at (2495, -1793, 172)" but you can ignore them ; the game complains about some new spawn points but it should not be a problem.

++ Copyright

Copywhat ?? no, seriously... as long as you don't forget the credit you're free to do anything you want with this mod.

++ Feedback

Please give your feedback (comments, bug reports, suggestions, cheers, insults or whatever) preferably in this thread, or by a PM in this forum, or by email at latruffe666@hotmail.com.
Remember that this is still beta, and may (read : "surely") contain bugs, as it's difficult to test in conjunction with every standard option or many features provided by AWE or eXtreme+ mods.
I'm particularly interested in script error reports from the console log, because it's sometimes difficult to reproduce bugs.
Another sweet tool for helping the debugging is to make a small demo (with the console command /record) showing the problem.

Have fun with this gametype !