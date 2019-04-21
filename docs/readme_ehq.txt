Enhanced Headquarters (EHQ) : a gametype for COD2
Version : 1.3
Author : La Truffe (latruffe666@hotmail.com)

++ Credits

Ravir : cvardef function

++ History log

1.0
- initial version

1.1
- moved radio icons on HUD at the top center of screen to avoid overlapping with chat messages
- optimization : spawn just one script_model for all radios

1.2
- actions on HQ (establish, destroy) are logged
- fixed visibility of some displayed messages on Linux server
- moved back to a basic serverinfo screen, to avoid "SV_SetConfigValueForKey: overflow" error due to COD2 not being able to handle many serverinfo dvars

1.3
- optimized handling of serverinfo dvars, to completely avoid "SV_SetConfigValueForKey: overflow" error
- ... which allowed to restore the complete serverinfo screen
- new option to disable weapon during capture of a radio (dvar scr_ehq_capturenoweapon)
- fixed visibility of some displayed messages

++ Object

This gametype is an extension of the HQ gametype in COD2.
It's all started with very limited changes (adding dvars to configure things), then bigger modifications, then even bigger ones... until the whole thing eventually became an independent gametype.
Why a new gametype ? leaving HQ untouched allows you to play standard HQ along EHQ if you like.

Here is a summary of what EHQ brings to the old HQ gametype :

1/ Dvars controlling the respawn delays
Players and radio respawn delays are configurable.

2/ Respawn of defenders
In standard COD2, defenders who have established a HQ won't respawn. In EHQ, defenders may be given the ability to respawn.
If they respawn, they can have an extra delay penalty to maintain a slight advantage to attackers.
If all defenders are dead, the HQ is automatically destroyed in standard HQ ; in EHQ this is configurable.

3/ Dvar controlling the maximum hold time
The maximum time a team can hold the HQ is configurable.

4/ Dvars controlling the radio radius
The radio radius is the maximum distance a player must stand from the radio to capture it.
In EHQ this radius is configurable.
Using the provided values (which are lower than in standard HQ, those from HQ being kept as default values) is an effective way to prevent players from capturing radios through walls, something that has always been a huge flaw in HQ IMHO.
No more telekinetic powers in EHQ ! players will have to stand firm on the radio.

5/ Time out for capturing a radio
If you mess with radio radius or use player spawn points (see below) some radios may become unreachable.
Or if a radio point is placed on a funky position of the map, players may never be able to reach it... alive.
EHQ provides a time out for capturing the radio ; after this delay, another radio respawns elsewhere.

6/ Use of DM and TDM spawn points
EHQ can create radio points out of DM and TDM spawn points for maps that have not been designed for HQ ; this makes virtually every map playable with EHQ !
Of course, radio points specifically designed by the map author are generally better than spawn points ; on the other hand, you can ignore the radio points provided in the map in case they are dummies : map authors often create the map script by copying an existing one, but sometimes forget to adjust radio points or remove them in case they don't provide compatibility with HQ.
Just select the appropriate combination between provided radio points and player spawn points.
You can also set a minimum distance a player may respawn from the current radio position, thus avoid players spawning directly on the radio.

7/ Dvars controlling the speed of radio capture
The time needed for players to establish a HQ and the time needed to destroy a HQ can be controlled, separately.
This allows to simulate the fact that establishing a HQ should normally take more time than destroying one... or the opposite if you wish.

8/ Several players needed to capture the radio
In EHQ you have the opportunity to set a minimum number of players that are needed simultaneously on the radio to capture it !
A fixed number may be specified (e.g. : 3 players) ; in random mode a value between 1 and the maximum will be chosen (e.g. : 1 or 2 or 3 players).
The number of players needed can be different for establishing and for destroying a HQ ; the current number is always indicated on the HUD inside a little radio, and may depend on the actual number of players in the team (e.g. if you're alone on your team you will have the ability to capture regardless of the number of players needed).
This option has a dramatic effect on strategy : team coordination is absolutely mandatory !

9/ Engineer mode
In that mode, some players are "engineers", who are the only ones able to capture the radio ! the other non engineer players won't be able to capture it at all.
Players are randomly selected as engineers at each new radio event (spawn or capture) and will stay engineers during the round, should they die or not.
Engineers are recognizable by their team mates with a special head icon.
You can combine this mode with a number of players needed to capture the radio ; in this case several engineers will be required on the radio at the same time.
* Advert * : playing EHQ in Engineer mode has some similarities with the V.I.P. gametype, as engineers have to be protected by their team mates in order to reach the radio and achieve the objective.

10/ Individual points
Players will score individual points for such things as establishing a HQ, destroying a HQ or killing an enemy engineer. These extra scores are a strong incentive for players to keep the objective in mind instead of blindly killing anybody in sight like in plain old TDM.

11/ A and B points on compass
For those nostalgic of COD2 1.0 (are there any ??) EHQ has an option to display the A and B objective points on compass before the radio appears.

12/ Weapon disabling during capture
Like in SD when planting or defusing a bomb, the player will have his weapon disabled during the capture of a radio.
But unlike in SD, this is configurable (not activated by default).

13/ Code optimization
The EHQ script does not use 1 thread per radio point like HQ, but a single thread for all.
Only one script_model is spawned for all radios.
This should save resources and improve stability, although I have no direct way to prove it...

++ Compatibility with COD2

EHQ is an extension of HQ in COD2 1.3 ; do NOT try it on older versions, it will probably not work well, if working at all.

++ Compatibility with mods

This is a standalone mod.
It is already integrated in AWE mod (Community Edition version).
For other mods an adaptation may be needed.

++ Compatibility with maps

EHQ is compatible with all maps that support standard HQ and uses the radio points designed for HQ.
It's also compatible with maps that support TDM but not HQ ; in this case radio points will be created out of DM and TDM spawn points. DM only compatible maps will not work because EHQ needs TDM spawn points for players, just like HQ.
In other words, EHQ is compatible with maps that support HQ and maps that support TDM.

++ Installation / uninstallation

The mod has a client and a server part. It cannot be made server-side only because it contains client files. However, the client part is ridiculously small.
It's available with separate client and server IWDs, as well as a combined client + server IWD.

To install, put the client and server IWDs in your fs_game folder.
On your redirect space, put only the client IWD that will be downloaded by players.

You may also want to combine the client part with another client mod, the same for the server part. It should not be a problem, as there are only new files, no existing file has been modified.
This is the preferred method to avoid the painful "Info string length exceeded" error.

To uninstall, just remove the client and server IWDs ; now that's an uninstallation procedure !

++ Configuration

Please see the sample ehq.cfg for a description of the new dvars, and a note about dvar overriding.
Copy/paste the desired dvars in your config file or make it execute ehq.cfg, and set g_gametype to ehq in your config file.

++ Limitations / problems

The mod does not include configuration options from a listen server ; please use a dedicated server instead, listen servers are known to be mods unfriendly anyway.

EHQ being an additional gametype, it may not be possible to vote for this gametype with the standard voting option. This is a known COD2 limitation, and there's little we can do for that. Also, custom maps won't be showing on the menu if you select EHQ, even if they actually work fine with EHQ.

The client and server part of the mod both include a file with the same name (ehq.gsc) : this is intended ! on your server, you have to make sure that the server part will be read before the client part. A way to achieve this is to keep the file names intact. Remember that COD2 loads files in the inverse alphabetical order ; for example zzz_ehq_svr_1.3.iwd will be read BEFORE zzz_ehq_cli_1.3.iwd, so in the server the correct ehq.gsc will be loaded (from the server iwd) and the blank one (from the client iwd) will be ignored.

++ Copyright

Copywhat ?? no, seriously... as long as you don't forget the credit you're free to do anything you want with this mod.

++ Feedback

Please give your feedback (comments, bug reports, suggestions, cheers, insults or whatever) preferably in this thread, or by a PM in this forum, or by email at latruffe666@hotmail.com.
Remember that this is still beta, and may (read : "surely") contain bugs, as it's difficult to test in conjunction with every standard option or AWE option.
I'm especially interested in script errors reports from the console log, as it's sometimes difficult to reproduce bugs. Another sweet tool for helping the debugging is to make a small demo (with the console command /record) showing the problem.

Have fun with this gametype !