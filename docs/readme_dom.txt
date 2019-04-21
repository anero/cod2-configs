*****************************************
*    DOMination release 4 (Mar 2007)    *
*             N.0.P.                    *
* (Nedgerblansky & 0ddball Productions) *
*****************************************

++ Credits

Matthias Lorenz : for the original Admiral mod version
Tally : who made the release 2 with us
Pointy : for some of his code (http://www.planetpointy.co.uk)

++ History log

1.0
- initial version

2.0

- Player number 'think' - dynamic flags spawn according to the number of players on a server. The more players, the more flags. if no players are on the server, no flags spawn.
- Choice of Static or dynamic flags - all the stock maps have 5 static flags placed in the best areas. But Admins can choose to have dynamic flags if they want
- Spawn radius think - dvar to set the min and max radius for players to spawn in relation to where the flags are.
- Configurable flag timeout - if a flag isnt capped in the timeout period, it is destroyed and respawns somewhere else. This stops campers holding down a flag area so that no one can cap it.
- Dvar to show/hide flag hints - this can stop the flagpoint hints showing through buildings and across maps. It makes the players more dependent on the compass if enabled.
- Configurable Player points to cap a flag - just allows Admins to decide how many points individual players get for capping a flag.
- Round Warmup Period - Gives time for players to join a server. In this Warmup Period, killing is allowed but no capping of flags. When timeout is over, the map automatically restarts and round 1 starts.

3.0

- DOMination TooL (DTL) is a mini-mod made to help mappers or even admins to set Static Flags positions directly ingame.
- Enhanced _mapsetup.gsc with Static Flags Positions + Spawn type set for Stock maps + the Custom Maps:
 - Bigred,
 - LouretBeta,
 - Anzio,
 - Castle Assault,
 - Bridge,
 - Chelm,
 - Border,
 - Destroyed Village,
 - Draguignan,
 - Edelweiss,
 - Eindhoven Beta,
 - Panodra,
 - Simmerath,
 - Townville,
 - Sevastopol.
 Made with DTL.
- A spawn type for players can now be defined if you don't want the default "dm" one, in _mapsetup.gsc, inside the map function. This make the DOM gametype compliant with nearly all maps.

4.0

- Switch spawns and flags: by setting scr_dom_switchspawns to "1", each team will switch spawns at each round,
- Capture clock added.
- Positions of flags are no longer located in _mapsetup.gsc but in mapsconfig.ini, a file located
  in the scriptdata sub directory (DTL has also been modified to follow this). 
- TOP HUD icons will no longer fade but blink. No more "neutral" state for a flag during capture.
- Conditions of victory can be changed: if scr_dom_mostflagswins dvar is set to 1, the team which 
  has captured the most flags at the end of the round wins. Otherwise (default) only capturing EVERY
  flag can drive to victory.
- Added Custom maps Static Flags & Spawns:
  - Salerno Beachhead Beta,
  - Tigertown Final
  - Foucarville
  - Farm Assault
  - Eindhoven
  - Night_of_days
  - Farm Assault beta 2
  - Winter Assault
  - Tuscany
	- Manche

++ Object

DOM is a great gametype Matthias introduced in his Admiral mod.

Each team has to capture every flag present in the map. To capture a flag,
a player has to stay near the flag during a fixed amount of time. The capture
may be interrupted if:
 - an enemy get close to the flag
 - the player is killed.

++ Compatibility with COD2

COD2 1.3
Do NOT try it on older versions, it will probably not work well, if working at all.

++ Compatibility with mods

It is already integrated in AWE mod (Community Edition version) and eXtreme+ mod (DOM version 2).
For other mods an adaptation may be needed.

++ Compatibility with maps

In random flag position mode, DOM is compatible with maps supporting at least TDM.
In static flags position mode, the flag positions of a map MUST be present in /scriptdata/mapsconfig.ini in order for that map to be playable in DOM.
You can create flag positions and define the spawn type for any map with the separate DTL tool.

++ Installation / uninstallation

The mod has a client and a server part. It cannot be made server-side only because it contains client files. However, the client part is ridiculously small.
It's available with separate client and server IWDs, as well as a combined client + server IWD.

To install, put the client and server IWDs in your fs_game folder.
On your redirect space, put only the client IWD that will be downloaded by players.

You may also want to combine the client part with another client mod, the same for the server part. It should not be a problem, as there are only new files, no existing file has been modified.
This is the preferred method to avoid the painful "Info string length exceeded" error.

To uninstall, just remove the client and server files ; now that's an uninstallation procedure !

++ Configuration

Please see the sample dom.cfg for a description of the new dvars.
Copy/paste the desired dvars in your config file or make it execute dom.cfg, and set g_gametype to dom in your config file.

++ Limitations / problems

DOM being an additional gametype, it may not be possible to vote for this gametype with the standard voting option. This is a known COD2 limitation, and there's little we can do for that. Also, maps won't be showing on the menu if you select DOM, even if they actually work fine with DOM.

The client and server part of the mod both include a file with the same name (dom.gsc) : this is intended ! on your server, you have to make sure that the server part will be read before the client part. A way to achieve this is to keep the file names intact. Remember that COD2 loads files in the inverse alphabetical order ; zzz_dom_svr_4.0.iwd will be read BEFORE zzz_dom_cli_4.0.iwd, so in the server the correct dom.gsc will be loaded (from the server IWD) and the blank one (from the client IWD) will be ignored.

++ Copyright

Copywhat ?? no, seriously... as long as you don't forget the credit you're free to do anything you want with this mod.

++ Feedback

Please give your feedback (comments, bug reports, suggestions, cheers, insults or whatever) preferably in this thread, or by a PM in this forum, or by email at 0ddball.gromov@gmail.com or latruffe666@hotmail.com.
Remember that this is still beta, and may (read : "surely") contain bugs, as it's difficult to test in conjunction with every standard option or many features provided by AWE.
I'm particularly interested in script error reports from the console log, because it's sometimes difficult to reproduce bugs.
Another sweet tool for helping the debugging is to make a small demo (with the console command /record) showing the problem.

Have fun with this gametype !