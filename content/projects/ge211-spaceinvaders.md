---
title: "Space Invaders using ge211"
date: 2021-03-13
description: "Simple space invaders game made using Jesse Tov's ge211 engine."
tags: [projects, space invaders, ge211, C, C++]
draft: false
---
**Project Start Date:** March 2021 | **Project Finish Date:** March 2021

![mainscreen](/resources/spaceinvaders/mainscreen.png)

This is a very basic Space Invaders game made as a final project for Northwestern University's CS 211 course. The game is programmed using C++ and rendered using [ge211](https://github.com/tov/ge211), an engine made by Professor Jesse Tov using the SDL2 libraries. It was made in roughly 5 days, and the programming reflects that pretty well. It's not the finest piece of programming, but it's also the first large C++ program I've made, much less a game.

# Design specifications

These are the design specifications we submitted for this project:

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

As with most game design, a lot of the issues we had came down to resource constraints, mainly our skill level and due dates. We made our specification in a way that had a smaller but more flexible scope, so that depending on how progress was going we could increase or decrease the amount of things we include while still remaining true to the original spec. One such example was that we only had time to program one level, but made it so that players could configure every aspect of the level to be as difficult or as easy as they would like. Another simplification we made was having a random alien shoot from the entire vector of living aliens versus only the bottom rows shooting, and just making those alien lasers pass through other aliens. This made programming alien shooting much easier.

Some of the other difficulties came down to hit detection for lasers and getting the vector of aliens to render properly. Thankfully some of this code was very similar to code we had to write for previous assignments, so we were able to adapt that design to our current program. Another annoying thing to program were the "animations" we had for when player ships got destroyed, but rather than actually animate that we decided to have a timer run for a few frames that would render an explosion sprite at the player location. This was a solid workaround, but was still a little tricky to get working. We also had a sprite made for alien explosions, but after several failed or very broken attempts to implement that we decided to give up as time was running out and it was not required by our spec.

# Gallery and Downloads

**WARNING: If you are a current CS 211 student, *do not* download this and attempt to use or submit any part of this code. There is copy protection in both my game and in the class grading servers that WILL detect plagarism and WILL get you an academic integrity violation.**

Here’s a gallery of images for the game and a video demo. There’s also downloads of the game available below; CMakeLists are provided but you will have to compile the program yourself as I have not set it up to create a standalone .exe yet with all the libraries included.

[Download the Space Invaders source code here](https://github.com/jackburkhardt/ge211-spaceinvaders)

![explode](/resources/spaceinvaders/explode.png) ![lategame](/resources/spaceinvaders/lategame.png) ![lose](/resources/spaceinvaders/lose.png)