Enhanced Search and Destroy (ESD)

This gametype is an extension of the standard SD gametype.
Many changes come from the COD2Svr mod by #7, with additions by La Truffe.

The major features that ESD brings over SD are :
- ability to make players respawn,
- ability to bomb or defuse the 2 objectives simultaneously,
- ability to restore an objective after a bomb has been defused.


Here are the configuration dvars :

// Score limit (default = 10)
set scr_esd_scorelimit "10"

// Time limit, in minutes (0 = no time limit, default = 0)
set scr_esd_timelimit "0"

// Maximum number of rounds (0 = no limit, default = 0)
set scr_esd_roundlimit "0"

// Round length, in minutes (default = 4)
set scr_esd_roundlength "10"

// Time at round start where spawning and weapon choosing is still allowed, in seconds (default = 15)
set scr_esd_graceperiod "15"

// Time it takes to plant a bomb, in seconds (default = 5)
set scr_esd_planttime "5"

// Time it takes to defuse a bomb, in seconds (default = 10)
set scr_esd_defusetime "10"

// Time it takes for a planted bomb to explode, in seconds (default = 60)
set scr_esd_bombtimer "60"

// Swap teams after a number of rounds (0 = disabled)
set scr_esd_swap_teams "0"

// Reset scores when swapping teams (0 = disabled, 1 = player score, 2 = team score, 3 = both)
set scr_esd_swap_teams_reset "0"

// Points for player that plants bomb (default = 0)
set scr_esd_plantscore "5"

// Points for player that defuses bomb (default = 0)
set scr_esd_defusescore "3"

// Points for player that defends bomb (default = 0)
// Points go to a defender if the attacker is close to the objective area.
// Points go to an attacker, after their bomb is planted and are defending it.
set scr_esd_defendscore "0"

// Ability for players to respawn (0 = no, 1 = yes, default = 0)
set scr_esd_respawn 1

// Respawn delay, in seconds (default = 10)
set scr_esd_respawndelay 10

// End round when all players in a team are dead (0 = no, 1 = yes, default = 1)
set scr_esd_endround_deadteam 0

// ESD mode (default = 0)
// 0 = standard SD : 1 active bomb site at a time, attackers win when the bomb explodes, defenders win if they defuse the bomb
// 1 = 2 active bomb sites, attackers win when the first bomb explodes, defused bomb removes the objective
// 2 = 2 active bomb sites, attackers have to explode both bombs to win, defenders win if they defuse a bomb
// 3 = 2 active bomb sites, attackers win when the first bomb explodes, defused bomb restores the objective
// 4 = 2 active bomb sites, attackers have to explode both bombs to win, defused bomb restores the objective
set scr_esd_mode 4