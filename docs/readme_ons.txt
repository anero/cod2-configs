*****************************************
*    ONSlaught release 2 (Mar 2007)     *
*             N.0.P.                    *
* (Nedgerblansky & 0ddball Productions) *
*****************************************

++ Credits

For DOM, on which this type is based:

Matthias Lorenz : for the original DOM Admiral mod version
Tally : who made the DOM release 2 with us
Pointy : for some of his code (http://www.planetpointy.co.uk)

++ History log

1.0

- initial version created by 0ddball.

2.0

- Switch spawns and flags: by setting scr_ons_switchspawns to "1", each team will switch spawns at each round,
- Capture clock added.
- Positions of flags are no longer located in _mapsetup.gsc but in mapsconfig.ini, a file located
  in the scriptdata sub directory (DTL has also been modified to follow this). 
- TOP HUD icons will no longer fade but blink. No more "neutral" state for a flag during capture.
- Conditions of victory can be changed: if scr_ons_mostflagswins dvar is set to 1, the team which 
  has captured the most flags at the end of the round wins. Otherwise (default) only capturing EVERY
  flag can drive to victory.
- Random Flags mode no more supported.
- All retail maps compatible + Custom maps:
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
  - Sevastopol,
  - Salerno Beachhead Beta,
  - Tigertown Final
  - Foucarville
  - Farm Assault
  - Eindhoven
  - Night_of_days
  - Farm Assault beta 2
  - Winter Assault
  - Tuscany
	- Manche.
	All flags positions made with DTL.

++ Object

Onslaught is a variant of DOMination (Static Flags).
With Onslaught, players have to capture the flags in a fixed order, one after the previous.
In this game, Allies have to capture flags from the most left flag icon of the TOP HUD to the most right and Axis, in reverse order.
The next "capturable" flag allways appears on compass.
Capturing a flag which is "over your team range" is forbidden (by the way, you can't do that) and a message is displayed if you try.

++ Compatibility with COD2

COD2 1.3
Do NOT try it on older versions, it will probably not work well, if working at all.

++ Compatibility with mods

It is already integrated in AWE mod (Community Edition version).
For other mods an adaptation may be needed.

++ Compatibility with maps

The flag positions of a map MUST be present in /scriptdata/mapsconfig.ini in order for that map to be playable in BT.
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

Please see the sample ons.cfg for a description of the new dvars.
Copy/paste the desired dvars in your config file or make it execute ons.cfg, and set g_gametype to ons in your config file.

++ Limitations / problems

ONS being an additional gametype, it may not be possible to vote for this gametype with the standard voting option. This is a known COD2 limitation, and there's little we can do for that. Also, maps won't be showing on the menu if you select ONS, even if they actually work fine with ONS.

The client and server part of the mod both include a file with the same name (ons.gsc) : this is intended ! on your server, you have to make sure that the server part will be read before the client part. A way to achieve this is to keep the file names intact. Remember that COD2 loads files in the inverse alphabetical order ; zzz_ons_svr_2.0.iwd will be read BEFORE zzz_ons_cli_2.0.iwd, so in the server the correct ons.gsc will be loaded (from the server IWD) and the blank one (from the client IWD) will be ignored.

++ Copyright

Copywhat ?? no, seriously... as long as you don't forget the credit you're free to do anything you want with this mod.

++ Feedback

Please give your feedback (comments, bug reports, suggestions, cheers, insults or whatever) preferably in this thread, or by a PM in this forum, or by email at 0ddball.gromov@gmail.com or latruffe666@hotmail.com.
Remember that this is still beta, and may (read : "surely") contain bugs, as it's difficult to test in conjunction with every standard option or many features provided by AWE.
I'm particularly interested in script error reports from the console log, because it's sometimes difficult to reproduce bugs.
Another sweet tool for helping the debugging is to make a small demo (with the console command /record) showing the problem.

Have fun with this gametype !