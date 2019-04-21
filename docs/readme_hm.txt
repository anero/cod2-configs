#########################
Hitman Gametype for COD2
#########################

Based on Artful_Dodger's ESP gametype for COD1 and UO

Ported over with changes by Tally

Compatable with AWE 3.0 beta 10 ; the spawn protection icon of AWE gets disabled in this gametype


THE PREMISE
============

One player is The Group Commander

At least one player is the Hitman

The majority of the players are Guards.

The Commander gets 2 points for killing a Hitman, but his position is indicated on the hud by a time-delayed blip and must keep moving to avoid precise detection by the Hitmen.

The hud blip can be turned off by cvar

Hitmen receive 2 points for killing The Commander. Hitmen are usually outnumbered 2 to 1 by Guards, who should be trying to guard The Commander in an attempt to gain their chance to be a Hitman. This promotes team work rather than merely looking to obtain points, as the object is to defend the Commander.

The more players on a server means more than one Hitman. Then, a further objective of the game is for each Hitman to evade the others, and get to and kill the Commander first.

When The Commander is killed, another Guard becomes The Commander.

The Commander cannot kill himself or be killed by friendly fire.

Guards can gain 1 point for killing a Hitman, and Hitmen gain 1 point for killing a Guard.

Damaged cause by friendly fire between the Guards and the Commander is split 50/50 between the shooter and damaged player.

If a Guard finds and kills an Hitman, that Agent becomes a Guard, and the Guard becomes a new Agent.

===================================

Features:
=========

Custom headicons:

Commander = Officers Cap

Guard = a Shield

Hitman = a Machine Gun

Fading hud elements after game start (15 seconds - to clean up the screen)

Cvar to turn off objectives on the compass altogether

Cvar to alter the time-delay for the objective blip on compass

======================================

USE:
=====

You must add both the server files and the client files to the respective AWE parts of the mod. Add the server part to the server part of AWE; add the client part to whichever client part of AWE you use (e.g b0.iwd)

There is an update for the AWE _teamkilling.gsc, as there was a bug with it. Therefore, you must replace the existing one in AWE with the one provided.

Server cvars:

//HM
set scr_hm_timelimit "20" \\Default is 30
set scr_hm_showcommander "0" \\Default is On
set scr_hm_tposuptime "5" \\Default is 1
set scr_hm_scorelimit "50" \\Default is 50
set scr_hm_showguard "0"

======================================

CONTACT/SUPPORT
===============

http://www.tallys-world.com