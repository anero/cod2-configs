*****************************************
*    BreakThrough release 1 (Mar 2007)  *
*             N.0.P.                    *
* (Nedgerblansky & 0ddball Productions) *
*****************************************

++ Credits

Onslaught Gametype by 0ddball,
Conquest gametype by After Hourz (http://www.after-hourz.com/)
DOMination gametype from  Nedgerblansky, Tally, Oddball based on the
original work of Matthias Lorenz on his mod ADMIRALMod, http://www.admiralmod.com.

++ History log

1.0

- initial version (this one !).
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

++ Object

BreakThrough is some sort of mix between ONSlaught and Conquest (by After Hourz) and based on the Static Flags of DOM.
Teams have to capture all objectives. At the beginnig of the round, the objective for both teams is the middle flag (or a randomly chosen one between the two center flags if the number of flags is even). All the other flags are considered to be already captured by each team (from first to objective -not included-, by allies from last to objective -not included-, by axis) The objective is shown on compass, waypoint and Top HUD by the objective star of SD.
When an objective is being captured, the icons blink on compass and Top HUD, showing the nationality of the player who captures.
As for CNQ (From After Hourz), only the objective flag is visible inside the map and on compass. When the objective is taken, the flag is removed (BTW, "hidden") and the next objective flags appears.
The round ends when the winning team has captured all the objectives or, in case of time limit, the team with the most objectives taken wins.
BreakThrough is also very similar to the WAR gametype of COD3, with more features.

Options:

- The player who captures the flags may have his weapons disabled, forcing his teammates to cover him (config var: scr_bt_capturenoweapon),
- The spawns can be switched each round (config var: scr_bt_switchspawns)
- "BreakThrough" can also be played in Booze-up mode (config var: scr_bt_drunkards)...A gift from France ! ;-)

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

Please see the sample bt.cfg for a description of the new dvars.
Copy/paste the desired dvars in your config file or make it execute bt.cfg, and set g_gametype to bt in your config file.

++ Limitations / problems

BT being an additional gametype, it may not be possible to vote for this gametype with the standard voting option. This is a known COD2 limitation, and there's little we can do for that. Also, maps won't be showing on the menu if you select BT, even if they actually work fine with BT.

The client and server part of the mod both include a file with the same name (bt.gsc) : this is intended ! on your server, you have to make sure that the server part will be read before the client part. A way to achieve this is to keep the file names intact. Remember that COD2 loads files in the inverse alphabetical order ; zzz_bt_svr_1.0.iwd will be read BEFORE zzz_bt_cli_1.0.iwd, so in the server the correct bt.gsc will be loaded (from the server IWD) and the blank one (from the client IWD) will be ignored.

++ Copyright

Copywhat ?? no, seriously... as long as you don't forget the credit you're free to do anything you want with this mod.

++ Feedback

Please give your feedback (comments, bug reports, suggestions, cheers, insults or whatever) preferably in this thread, or by a PM in this forum, or by email at 0ddball.gromov@gmail.com or latruffe666@hotmail.com.
Remember that this is still beta, and may (read : "surely") contain bugs, as it's difficult to test in conjunction with every standard option or many features provided by AWE.
I'm particularly interested in script error reports from the console log, because it's sometimes difficult to reproduce bugs.
Another sweet tool for helping the debugging is to make a small demo (with the console command /record) showing the problem.

Have fun with this gametype !