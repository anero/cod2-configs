V.I.P. : a gametype for COD2
Version : 1.4
Author : La Truffe (latruffe666@hotmail.com)

++ Credits

Ravir : cvardef function

++ History log

1.0
- initial version

1.0b
- fixed bug : ugly script error when VIP smoke grenades are disabled
    
1.1
- fixed bug : auto-balancing or change of team when VIP was waiting to respawn lead to unexpected results
- use of cvardef allows to create overriding dvars
- reward VIP for staying alive : the VIP will score scr_vip_vippoints points every scr_vip_vippoints_cycle minutes, when enemy team is populated
- reorganized serverinfo screen to include the 2 new dvars scr_vip_vippoints and scr_vip_vippoints_cycle
- display alive time when VIP dies, keep track of record time
- select a new VIP only when enemy team is populated

1.2 RC1
- use of unmodified cvardef (gametype dependent)
- the VIP has a status icon on the scoreboard
- the VIP head icon will no longer interfere with AWE spawn protection
- the VIP cannot change team or go spectator
- the selected VIP's body is removed before respawning
- version displayed on serverinfo screen
- lots of changes to ensure compatibility with eXtreme+ mod

1.2 RC2
- fixed visibility of some displayed messages on Linux server

1.2
- fixed an error that could occur just before the selected VIP spawns
- moved back to a basic serverinfo screen, to avoid "SV_SetConfigValueForKey: overflow" error due to COD2 not being able to handle many serverinfo dvars

1.3
- optimized handling of serverinfo dvars, to completely avoid "SV_SetConfigValueForKey: overflow" error (AWE and standalone versions only)
- ... which allowed to restore the complete serverinfo screen (AWE and standalone versions only)
- fixed visibility of some displayed messages

1.4
- fixed a bug allowing the VIP to change team or go spectator, that would lead to 0 or 2 VIPs in the team

++ Object

This is a new gametype for COD2.
It's more or less similar to VIP gametypes that can be found in other multiplayer games, but here is a version for COD2 with its own features.

This gametype is team based. Each team has 1 special player (the VIP), which is the target for the other team. Each team must try to kill the enemy VIP while protecting its own.
Why only 1 VIP per team ? because it probably wouldn't be too much fun to run after several enemy VIPs and have to protect several friendly VIPs at the same time ; 2 objectives at once seem enough for most players.

A team scores one point when the enemy VIP has been killed.
Players get individual scores for killing regular players and the VIP.
Players also get score by protecting their VIP, that is killing enemies in the vicinity of the VIP or enemies that recently caused damage to the VIP.
These extra scores are a strong incentive for players to keep the objective in mind (kill the enemy VIP and protect his own) instead of blindly killing anybody in sight like in plain old TDM.
The VIP gets score by staying alive as long as possible.

When friend icons are enabled, the VIP has a specific head icon visible by his own team mates.
VIPs may also be targeted on the compass for team mates and/or enemies (configurable by dvars).

When a VIP has been killed, the player respawns as a regular player, and another player in the team is selected as the new VIP.
The selection system integrates a random factor that usually prevents being the VIP twice in a row, although it's not impossible - and certainly necessary if you are alone in your team !
When a player is picked as the new VIP, he dies (without accounting this death) and is forced to respawn at a spawn point. This is to prevent "instant VIP killing" if the player was in the middle of a firefight and about to die just before being selected.

The VIP is a very special player, not a simple soldier ; otherwise we wouldn't call him "VIP", would we ?
As such, he cannot handle weapons and is only able to use a pistol, smoke and frag nades.
Hopefully, his pistol is heavily modified : it makes 2x damage and has 5x ammo !
Also, he uses special smoke nades that make a very dark smoke spreading over 2x the space of a normal smoke cloud. And when the VIP stands into the smoke, he becomes invisible on the compass ! (if compass visibility is activated of course).
The smoke provides a good visual protection for the VIP, its drawback being that the smoke is also a good indication of the area where the VIP is hiding.
VIP visibility on compass is not altered by the enemy VIP's smoke, or even by a previous VIP now dead ; let's say their respective smoke nades are not compatible...
VIP smoke nades cannot be thrown, just dropped.
VIP pistol and smoke nades can be disabled with a dvar, if you want to give the VIP the opportunity to use standard weapons or smoke nades.
The VIP uses normal frag nades. Why ? err... why not ? but the number of frag nades given to the VIP is configurable.
Last, the VIP has an initial health of 150% compared to standard health ; configurable of course.

Binoculars of all players have the ability to tell you when you have spotted the enemy VIP ! this can be useful to track down a hiding VIP even if he's marked on the compass. The VIP smoke neutralizes this feature.
These special binoculars can be disabled as well.

++ Compatibility with COD2

COD2 1.3
Do NOT try it on older versions, it will probably not work well, if working at all.

++ Compatibility with mods

This is a standalone mod.
It is already integrated in AWE mod (Community Edition version) and eXtreme+ mod.
For other mods an adaptation may be needed.

++ Compatibility with maps

V.I.P. uses existing TDM spawn points so it should be compatible with any map that supports TDM.

++ Installation / uninstallation

The mod has a client and a server part. It cannot be made server-side only because it contains client files. However, the client part is ridiculously small.
It's available with separate client and server IWDs, as well as a combined client + server IWD.

To install, put the client and server IWDs in your fs_game folder.
On your redirect space, put only the client IWD that will be downloaded by players.

You may also want to combine the client part with another client mod, the same for the server part. It should not be a problem, as there are only new files, no existing file has been modified.
This is the preferred method to avoid the painful "Info string length exceeded" error.

To uninstall, just remove the client and server IWDs ; now that's an uninstallation procedure !

++ Configuration

Please see the sample vip.cfg for a description of the new dvars, and a note about dvar overriding.
Copy/paste the desired dvars in your config file or make it execute vip.cfg, and set g_gametype to vip in your config file.

++ Limitations / problems

The mod does not include configuration options from a listen server ; please use a dedicated server instead, listen servers are known to be mods unfriendly anyway.

VIP being an additional gametype, it may not be possible to vote for this gametype with the standard voting option. This is a known COD2 limitation, and there's little we can do for that. Also, maps won't be showing on the menu if you select VIP, even if they actually work fine with VIP.

The VIP smoke nades may cause graphics lag on older machines, a bit more than standard nades because the smoke is thicker. The only way to bypass this is to disable them completely.

The client and server part of the mod both include a file with the same name (vip.gsc) : this is intended ! on your server, you have to make sure that the server part will be read before the client part. A way to achieve this is to keep the file names intact. Remember that COD2 loads files in the inverse alphabetical order ; zzz_vip_svr_1.3.iwd will be read BEFORE zzz_vip_cli_1.3.iwd, so in the server the correct vip.gsc will be loaded (from the server IWD) and the blank one (from the client IWD) will be ignored.

In the eXtreme+ version, if the VIP tries to swap his VIP pistol with another weapon, he will actually drop it and have to pick it up again ; this is because eXtreme+ handles weapons in a very special way

++ Copyright

Copywhat ?? no, seriously... as long as you don't forget the credit you're free to do anything you want with this mod.

++ Feedback

Please give your feedback (comments, bug reports, suggestions, cheers, insults or whatever) preferably in this thread, or by a PM in this forum, or by email at latruffe666@hotmail.com.
Remember that this is still beta, and may (read : "surely") contain bugs, as I did not extensively test it in conjunction with every standard option or AWE option.
I'm especially interested in script errors reports from the console log, as it's sometimes difficult to reproduce bugs. Another sweet tool for helping the debugging is to make a small demo (with the console command /record) showing the problem.

Have fun with this gametype !