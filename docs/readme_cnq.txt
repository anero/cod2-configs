###########################
Conquest Gametype for COD2
###########################
by Tally and UncleBone
(original scripting by Innocent Bystander)

AWE compatable Version Included


Included are the gametype files (1 server; 1 client) needed to play conquest on a CNQ enabled map.

//USE

//Standalone

Place both _svr_cnq.iwd and client_cnq.iwd on your server. 
Place client_cnq.iwd on your redirect so that the client gets both.

//AWE Version

Either add the server files (_svr_cnq_awe.iwd) to the server part of AWE 3.0 beta 10, or add straight to the fs_game folder where the server AWE files are.

It is recommended to add them in, as the checksum error can always rear its ugly head.

Do the same with the client part - client_cnq.iwd - either add them to the client AWE download, or add them next to it in the fs_game folder.


//Credits

Slyk - for all the hard work thinking the concept of Conquest out in MOH:Spearhead & vCOD/UO

Innocent Bystander - for the original script in vCOD/UO, and giving me permission to continue the project into COD2 (and beyound???)

AfterHourz Gaming Network - for help and support testing Twin Ridges, the first CNQ map for COD2

//Disclaimer 

Tally is NOT associated with After Hourz Gaming Netowrk in any formal way, other than to be involved with UncleBone, who is.

ADMIN OPTIONS
-------------

There have been a number of requests for changes to the gametype 
which are already possible using existing gametype cvars. 
I'll go over a few of them here:

Q) The game should end if one team flips a bonus switch
A) Though not the default setup, this is easily accomplished. 
    In your server config, set "scr_cnq_team_bonus_points" to 
    be a the same number as scr_cnq_scorelimit (500 by default).
    This way when a team flips the bonus 500 points are awarded
    and thus the game will end immediately.
    
Q) Players should receive points for taking objectives.
A) Set "scr_cnq_player_bonus_points" and "scr_cnq_player_objective_points"
   (both 0 by default) in your server config to a value you want 
   assigned for doing so. Note that when a player recieves points it also
   counts toward the team score, so you may want to set "scr_cnq_team_bonus_points"
   and "scr_cnq_team_objective_points" to 0 so that points aren't doubled up.
   
Q) The teams should start in the middle of the maps, not at one end.
A) Set "scr_cnq_initialobjective" to be the number of the objective
   you want teams to start at. For example on Gun Assault, if you want the 
   teams to start so that the Allies have the Manor House and the Axis the 
   Plowed Field, you would set this value to "2" (the second objective in
   progression).
   
Q) The game values TDM-style killing too much, you should make it 
   objective-only based.
A) This was a design intent, but you can modify the game very easily to 
   place MUCH more emphasis on objectives than killing. Simply set 
   "scr_cnq_team_bonus_points" and "scr_cnq_team_objective_points" to
   higher values than stock (currently 25 and 10, respectively). You may
   also want to adjust "scr_cnq_scorelimit" to a higher number to compensate
   for the increases in points being awarded.