---
title: "[UPCOMING] TalkTree"
date: 2021-12-18
description: "A simple branching dialogue system for use in Unity games."
tags: [projects, unity, csharp, game design]
draft: true
---
**Project Start Date:** December 18th, 2021

TalkTree is a basic branching dialogue system for use in Unity games, designed primarily for singleplayer RPGs. It was built and tested on Unity 2020.3, but your mileage may vary on other versions. Instructions, examples, and other documentation is forthcoming.

## Features
* Optional criteria for dialogue options (skills, perks, global variables, etc)
* Allows for various node chainings based on desired outcome (such as chaining NPC dialogue nodes or cyclic responses)
* Support for attaching/playing voice clips to dialogue nodes
* Support for attaching/playing animation clips to dialogue nodes
* Easy storage/editing of dialogue trees in text files, stored per npc (.npc)

## Planned features
* Dedicated graphical software/editor plugin for dialogue tree visualization and modification
* Integration support for text generators (including HTN planners such as [Step](https://github.com/ianhorswill/Step))
* Allowing multiple NPCs to speak in a single conversation
