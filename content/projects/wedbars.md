---
title: "WedBars"
date: 2021-04-18
description: "A version of bedwars created from scratch based on the Hypixel server."
tags: [wedbars, bedwars, spigot, plugin, bed wars, minecraft]
draft: true
---
**Project Start Date:** March 2021 | **Project Finish Date:** Ongoing

WedBars is a version of the the hugely popular Minecraft minigame mode *BedWars*, which itself is a derivative of other games such as *EggWars* and *CakeWars*. This plugin was concieved by myself and Dilan partially as a "what-if" joke and partially as a Java learning project for me but quickly turned into a full-fledged server plugin that has become a nearly identical recreation of the Hypixel server's BedWars. It contains features such as an arena setup wizard, robust configuration options, and a MYSQL-enabled player stats system.

# Background on Bedwars

BedWars is one of if not the most popular Minecraft minigames to ever exist, and is the largest gamemode on Hypixel which is the biggest Minecraft server network ever, averaging roughly 150,000-175,000 concurrent players at the time of this writing. While not invented by Hypixel, all forms of this gamemode (including ours) follow rougly the same overall game structure. Players are placed in teams, usually Solos, Duos, 3s, or 4s, and when the game starts they spawn on a small island which which contains some shop NPCs and a resource generator. The island generators, along with higher tiers of generators in other areas of th map, spawn ingots and gems for players to spend at their NPC shops and purchase tools, blocks, team upgrades, and powerups. Every team has a bed they must defend; if the bed is broken, they become "final kills" and will not respawn once killed. Players must destroy the beds of other teams and wipe their players while defending their own bed. The game ends when one team is left standing.

# Why make another one?

I mentioned before that many forms of this gamemode exist, and while that is true, they are almost all created by large server networks with teams of paid developers and all of the code is kept secret. While I was trying to look for a Spigot plugin to run my own BedWars server with, I realized that a lot of the ones that were made by the community lacked features, polish, or updates. So Dilan and I's goal soon turned from just making another version of BedWars for private servers into making a fully-features and polished plugin that could eventually be released to the Minecraft server modding community. In addition to just being able to run our own games, ourselves or other users of this plugin could code in their own powerups or other twists on the gamemode to further improve it.

# The process

Dilan really carried this project. Since he had an extensive Spigot plugin and Java programming background, he was able to guide me and also tackle a lot of the more tricky parts of the code. This was my first time working with Java in years and using the Spigot API, so most of my time was spentll fumbling though the javadocs.

Dilan programmed most of the game logic while I handled a lot of the powerups, event listeners, and other quality of life features.