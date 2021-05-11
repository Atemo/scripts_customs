# Scripts customs for rAthena

[50rebirth_add_status_points.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/50rebirth_add_status_points.txt)


Based on this request : http://rathena.org/board/topic/82507-rebirth-system-50-rebirths/

The player can rebirth x times. The player receive extra status points each Rebirth.
Settings :
```
OnInit:
	.reset_max = 50;		// how much reset max
	.change_reward = 30;	// after 30 rebirth, change reward
	.num_status = 300;		// + X number of status points

// item required <item ID>, <number>
	setarray .item_req, 501, 5,
						502, 2,
						503, 3;
	.size_item = getarraysize( .item_req );

// additionnal items after rebirth >> .change_reward
// <item ID>, <number>
	setarray .add_item_req, 601, 1;

// rewards <item ID>, <number>
	setarray .reward, 504, 1;
	.size_reward = getarraysize( .reward );
	end;
```
--------------------------------------------------------------------------------------------------------------------------------

[align_dromedary.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/align_dromedary.txt)


A simple script where the player need to align the dromedary in the same direction to winning... nothing for now. Just for fun.

--------------------------------------------------------------------------------------------------------------------------------
[ann_highest_lvl.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/ann_highest_lvl.txt)


A simple and very old script.
Announce the player with the highest level in the server. Check the max level each level up.

--------------------------------------------------------------------------------------------------------------------------------
[buff_guild_woe.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/buff_guild_woe.txt)

A very old script.
Buff all guild members in the same map of the guild leader during the woe.
Have a cooldown of 10 mins.
Only for guild leader.

--------------------------------------------------------------------------------------------------------------------------------

[check_item_player.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/check_item_player.txt)

Based on this request : http://rathena.org/board/topic/82507-rebirth-system-50-rebirths/

Check the amount of Items in the inventory, storage guild storage, cart of the specific player.
The player must be offline to be accurate.

--------------------------------------------------------------------------------------------------------------------------------

[clean_poring_race.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/clean_poring_race.txt)


Simple cleaning of a poring race.

--------------------------------------------------------------------------------------------------------------------------------

[cmd_banker.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/cmd_banker.txt)


Works like a banker.
`@bn` : display the amount of zeny in bank in a message
`@withdrawlbn <value>` : withdrawl an amount of zeny
`@depositbn <value>` : deposit an amount of zeny

--------------------------------------------------------------------------------------------------------------------------------

[display_guild_info.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/display_guild_info.txt)


Display informations of a select guild - castle own, master, members online/offline...

--------------------------------------------------------------------------------------------------------------------------------

[gatcha.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/gatcha.txt)


A simple script where the player can get some defined items at some rates using some defined item.

```
Example:
	// 50% to get something using a gold coin (id: 671). Then [20/(20+30+50)]% (which is.. 20%) to get the item id 2462.
	setarray .p0, 671,50,	2462,1,20,	1161,1,30,	5394,1,50;
```

--------------------------------------------------------------------------------------------------------------------------------

[hourly_points.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/hourly_points.txt)


Give a reward for staying 1 hour IG.
It exists a lot a hourly points npc, it was just for fun.

--------------------------------------------------------------------------------------------------------------------------------


[hunter_hunted.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/hunter_hunted.txt)

Based on this request : http://rathena.org/board/topic/80798-pvp-script-hunters-hunted/

Players register in the npc. After 10 mins, the npc give a unique and random number 1-128 and a target.
The player kill his target => 3 points, otherwise => 1 point.
5 players with 30 points => end of event.
`@hunter` command to display hunter points of player online.

Settings :
```
OnInit:
	.npc_name$ = "^ff0000- [ Hunter NPC ] -^000000";
	.malus_logout = 3;			// num malus points if log out ? (0: disabled)
	.point_main = 3;			// points when killing main target / - points for main killed
	.point_others = 1;			// points when killing others targets
	.event_map$ = "geffen";		// event map
	.min_player = 10;				// number min players to start
	setarray .reward,	30, 501, 1,	// Typo : <points min>, <item ID>, <amount items>
						29, 502, 1,
						19, 503, 1,
						 9, 504, 1,
						 1, 505, 1;
```
--------------------------------------------------------------------------------------------------------------------------------


[instance_time_round.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/instance_time_round.txt)

Based on this request : http://rathena.org/board/topic/78529-instance-script/?hl=instance

An old script.

An instance on `1@guild`.
Players must be in party.
Spawn the amount and ID of mob/difficulty/number depending on the number of player in the party.
Players have a limited time to kill the mobs each round. If they fail => end.
Each round, they gain some points saved in the variable `#hero_points`.

Settings are under `OnInit`.

--------------------------------------------------------------------------------------------------------------------------------


[party_3vs3.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/party_3vs3.txt)

Based on this request : http://rathena.org/board/topic/81997-my-ideal-pvp-mode/

An old script.
A game 3vs3. Players of a team must kill all players of other team. Killed player revive after some secondes defined by the setting.
Reward at the end for all winner.


--------------------------------------------------------------------------------------------------------------------------------


[queue_bg_on_official.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/queue_bg_on_official.txt)

An old script before the bg queue update.

A sample queue system to register in official bg.
Diff of official bg at the end of the script.


--------------------------------------------------------------------------------------------------------------------------------

[sell_a_item_in_my_inventory.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/sell_a_item_in_my_inventory.txt)

Sell a specific Item in the inventory vs some Items defined under `OnInit`.

--------------------------------------------------------------------------------------------------------------------------------

[total_time_online.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/total_time_online.txt)

Rank of player/account online.
Give reward by mail each week to the defined top online.

Another version at the end of the script with a sql table.

--------------------------------------------------------------------------------------------------------------------------------

[track_map.txt](https://github.com/Atemo/scripts_customs/blob/master/olds_scripts/track_map.txt)

Display a viewpoint for each player on the same map of the user.

--------------------------------------------------------------------------------------------------------------------------------

