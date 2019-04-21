WARNING: These modifications are given AS IS with NO WARRANTY. 

This is an Enhanced CTF for AWE.

It's based on Bullet-Worm's PowerServer CTF script.

NOTICE: Sorry but this mod is not serverside only as I made some localizations in order 
to limit the "WARNING: Non-localized..." lines on log files...

NEW FEATURES:

 + 2 Points scored for assisting the flag carrier or defending your own flag ("a la CoDUO").

 flag grace period:
 If the Flag is taken but not captured for that period, the flag icon disappears from your teams compass and appears on enemys compass.

INSTALL:

1. Make a back of your ctf.gsc (located in maps\mp\gametypes)

2. Copy ctf.gsc and _flag_status.gsc to the maps\mp\gametypes directory (click yes to overwrite)

3. Copy ctf.str to your localizedstrings directory of your client.iwd file

4. Copy ctf.cfg to your fs_game directory (or add the NEW CVARS below to your server.cfg)

5. Add the following without the Quotes to your server.cfg "exec ctf.cfg"

6. To change the messages/language open ctf.str with a text editor (make your changes and save them)

NEW CVARS:

 // Automatic Flag Return Delay after dropped
 set scr_ctf_flagreturndelay 120 // 120 stock
 //
 // Stolen Flag's Position shown on Compass?
 // 0 = no
 set scr_ctf_show_compassflag 0
 //
 // Stolen Flag GracePeriod for Compass Icons
 // Sets the number of seconds a player has to "get away"
 // before the flag's compass icon starts to show its
 // current position to the enemy via the compass.
 // note: scr_ctf_show_compassflag must be on!
 set scr_ctf_flag_graceperiod 30
 //
 // Compass Flag Position Update Time
 // Sets how often (in seconds) a stolen flag updates 
 // its current position on the compass.
 // note: scr_ctf_show_compassflag must be on!
 set scr_ctf_positiontime 10


CREDITS:

	Bullet-Worm for the main job (http://www.wormsworld.net/forums),
	Shooter for the AWE adaptation
	[GromoV]0ddball for localization, corrections and modifications + Linux testing. (http://gromov.free.fr)

