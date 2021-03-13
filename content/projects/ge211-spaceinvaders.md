---
title: "Space Invaders using ge211"
date: 2021-03-13
description: "Simple space invaders game made for CS 211 using Jesse Tov's ge211 engine."
tags: [space invaders, ge211, C, C++]
draft: false
---
**Project Start Date:** March 2021 | **Project Finish Date:** March 2021

![mainscreen](/resources/spaceinvaders/mainscreen.png)

This is a very basic Space Invaders game made as a final project for Northwestern University's CS 211 course. The game is programmed using C++ and rendered using [ge211](https://github.com/tov/ge211), an engine made by Professor Jesse Tov using the SDL2 libraries. It was made in roughly 5 days, and the programming reflects that pretty well. It's not the finest piece of programming, but it's also the first large C++ program I've made, much less a game.

# Design specifications

These are the design specifications we submitted for the project:


- The aliens are initially placed in a large grid near the top of the screen
- The aliens, as a whole block, move slowly to one side of the screen, move down, and then continue to the other side of the screen.
- The player's ship is y-locked near the bottom of the screen, but can move back and forth using the left and right arrow keys. There will be continuous control — If the user holds down either of the arrow keys, the ship should continue to move in that direction.
- The player can shoot a laser directly up using the spacebar, but there is a brief "cooldown" period between shots
- The aliens also shoot lasers straight downwards, often hitting shields in the process. (In play testing, if this makes the game too easy, the shots can be targeted at the player)
- If an alien is hit, it disappears from the screen
- If the player is hit, you lose a life. 3 lives lost is game over. The life count will be displayed with a few small icons in the corner of the screen. Every time the player’s ship is destroyed, one of the icons will disappear.
- After losing a life, the player will respawn in the center of the screen. The ship will appear destroyed through a different image or animation for a few seconds, but then will immediately respawn without any invincibility frames.
- There are a few "shields" directly above the player, near the bottom of the screen. They can take a few (TBD) hits from both the aliens and the player to protect the player, but eventually break once their hit-count is depleted. The shields are unmoving arches.
- If the aliens reach the bottom of the screen -- the player's y-position -- it is game over
- A simple point system keeps track of the player's score for hitting the aliens

# Challenges



# Gallery and Downloads

**WARNING: If you are a current CS 211 student, *do not* try downloading this and attempt to use or submit any part of this code. There is copy protection in both my game and in the class grading servers that WILL detect plagarism and WILL get you an academic integrity violation.**

Here’s a gallery of images for the game and a video demo. There’s also downloads of the game available below; CMakeLists are provided but you will have to compile the program yourself as I have not set it up to create a standalone .exe yet with all the libraries included.

[Download the Space Invaders source code here](https://github.com/jackburkhardt/ge211-spaceinvaders)

