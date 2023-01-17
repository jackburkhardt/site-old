---
title: "WedBars"
date: 2021-04-18
summary: "A version of the Hypixel server's popular Bedwars gamemode, recreated from scratch."
tags: [projects, wedbars, bedwars, spigot, plugin, bed wars, minecraft, featured]
draft: false
---

**Update:** I am currently working on a port for this plugin to the 1.13+ Spigot API. While this port is about 80% done, it is not yet suitable for production use. As always, you can view more info and submit issues on [GitHub](https://github.com/dilanx/WedBars/tree/1.13+).

WedBars is a version of the the hugely popular Minecraft minigame mode *BedWars*, which itself is a derivative of other games such as *EggWars* and *CakeWars*. This plugin was conceived by myself and Dilan partially as a "what-if" joke and partially as a Java project for me but quickly turned into a full-fledged server plugin that has become a nearly identical recreation of the Hypixel server's BedWars. It contains features such as an arena setup wizard, robust configuration options, and a MYSQL-enabled player stats system.

## Background on Bedwars

BedWars is one of if not the most popular Minecraft minigames to ever exist, and is the largest gamemode on Hypixel which is the biggest Minecraft server network ever, averaging roughly 150,000-175,000 concurrent players at the time of this writing. While not invented by Hypixel, all forms of this gamemode (including ours) follow roughly the same overall game structure. Players are placed in teams, usually Solos, Duos, 3s, or 4s, and when the game starts they spawn on a small island which which contains some shop NPCs and a resource generator. The island generators, along with higher tiers of generators in other areas of th map, spawn ingots and gems for players to spend at their NPC shops and purchase tools, blocks, team upgrades, and powerups. Every team has a bed they must defend; if the bed is broken, they become "final kills" and will not respawn once killed. Players must destroy the beds of other teams and wipe their players while defending their own bed. The game ends when one team is left standing.

## Why make another one?

I mentioned before that many forms of this gamemode exist, and while that is true, they are almost all created by large server networks with teams of paid developers and all of the code is kept secret. While I was trying to look for a Spigot plugin to run my own BedWars server with, I realized that a lot of the ones that were made by the community lacked features, polish, or updates. So Dilan and I's goal soon turned from just making another version of BedWars for private servers into making a fully-features and polished plugin that could eventually be released to the Minecraft server modding community. In addition to just being able to run our own games, ourselves or other users of this plugin could code in their own powerups or other twists on the gamemode to further improve it.

## Thinking beyond 1.8

Most Bedwars players and servers still operate on Minecraft version 1.8 from 2013 due to the different PvP mechanics. I view the PvP community's reluctance to move past 1.8 as quite a shame since there are so many fresh and innovative possibilities created by the new PvP system and new game features. So in addition to working on a version of this project for 1.8, I've been porting Wedbars to use the 1.13+ Spigot API (for support of Minecraft versions 1.13-1.17). This port is now almost complete, and once the fundamentals are working I can then turn towards implementing new features made possible by newer versions of the game. New 1.13+ features could include anything from new powerups and blocks to smaller changes like properly colored beds for each team.

## Downloads & Source
You can find the source code on [GitHub](https://github.com/dilanx/WedBars) and download nightly builds from my [Jenkins build server](http://builds.jackburkhardt.com/).