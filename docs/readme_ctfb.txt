Capture the Flag Back (CTFB) : a gametype for COD2
Version : 1.3
Author : La Truffe (latruffe666@hotmail.com)

++ Credits

Matthias : original CTFB gametype in Admiral mod
Ravir : cvardef function

++ History log

1.0
- initial version

1.1
- fixed bug when flag carrier disconnects
- players get points for defending their flag (dvar scr_ctfb_points_defend) or assisting the carrier of their flag (dvar scr_ctfb_points_assist)
- dvar for flag protection (defend or assist) distance : scr_ctfb_flagprotectiondistance
- auto-return of dropped flag after a configurable delay (dvar scr_ctfb_flagautoreturndelay)
- flag auto-returns in minefields, like in CTF

1.2
- 2 UI dvars renamed (AWE and standalone versions only)
- fixed visibility of some displayed messages

1.3
- fixed bug making players sometimes spawn under the map in random flags mode

++ Object

CTFB is a great gametype Matthias introduced in his Admiral mod.

It works exactly as CTF, except that a flag won't automatically return to its base when a player of the same team touches it.
In this case, the flag will have to be returned to its base by a player of the team.
As a consequence, a player may carry both flags at the same time.

This adaptation of CTFB differs from the Admiral mod version by a few functionalities.

++ Compatibility with COD2

COD2 1.3
Do NOT try it on older versions, it will probably not work well, if working at all.

++ Compatibility with mods

This is a standalone mod.
It is already integrated in AWE mod (Community Edition version) and eXtreme+ mod.
For other mods an adaptation may be needed.

++ Compatibility with maps

CTFB is obviously compatible with maps supporting CTF.
In random flag position mode, it makes use of DM spawn points to place flags and spawn players. Using this option requires maps supporting DM.

++ Installation / uninstallation

The mod has a client and a server part. It cannot be made server-side only because it contains client files. However, the client part is ridiculously small.
It's available with separate client and server IWDs, as well as a combined client + server IWD.

To install, put the client and server IWDs in your fs_game folder.
On your redirect space, put only the client IWD that will be downloaded by players.

You may also want to combine the client part with another client mod, the same for the server part. It should not be a problem, as there are only new files, no existing file has been modified.
This is the preferred method to avoid the painful "Info string length exceeded" error.

To uninstall, just remove the client and server files ; now that's an uninstallation procedure !

++ Configuration

Please see the sample ctfb.cfg for a description of the new dvars, and a note about dvar overriding.
Copy/paste the desired dvars in your config file or make it execute ctfb.cfg, and set g_gametype to ctfb in your config file.

++ Limitations / problems

The mod does not include configuration options from a listen server ; please use a dedicated server instead, listen servers are known to be mods unfriendly anyway.

CTFB being an additional gametype, it may not be possible to vote for this gametype with the standard voting option. This is a known COD2 limitation, and there's little we can do for that. Also, maps won't be showing on the menu if you select CTFB, even if they actually work fine with CTFB.

The client and server part of the mod both include a file with the same name (ctfb.gsc) : this is intended ! on your server, you have to make sure that the server part will be read before the client part. A way to achieve this is to keep the file names intact. Remember that COD2 loads files in the inverse alphabetical order ; zzz_ctfb_svr_1.2.iwd will be read BEFORE zzz_ctfb_cli_1.2.iwd, so in the server the correct ctfb.gsc will be loaded (from the server IWD) and the blank one (from the client IWD) will be ignored.

++ Copyright

Copywhat ?? no, seriously... as long as you don't forget the credit you're free to do anything you want with this mod.

++ Feedback

Please give your feedback (comments, bug reports, suggestions, cheers, insults or whatever) preferably in this thread, or by a PM in this forum, or by email at latruffe666@hotmail.com.
Remember that this is still beta, and may (read : "surely") contain bugs, as it's difficult to test in conjunction with every standard option or many features provided by AWE.
I'm particularly interested in script error reports from the console log, because it's sometimes difficult to reproduce bugs.
Another sweet tool for helping the debugging is to make a small demo (with the console command /record) showing the problem.

Have fun with this gametype !