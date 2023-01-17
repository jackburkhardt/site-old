---
title: "Northwestern Minecraft Server"
date: 2021-03-24
summary: "A long-standing Minecraft survival server developed for the Northwestern community."
tags: [projects, minecraft, server, northwestern, featured]
draft: false
---

I designed, developed, and hosted several iterations of a Minecraft server for the Northwestern community, open to all students of all skill levels. This server was created shortly after our class received admission to Northwestern, which happened to coincide with the start of the COVID-19 pandemic and early quarantine orders. It gave members of our class the opportunity to meet and engage with one another despite only being able to communicate virtually. Since then, this server has had 3 major iterations (plus a brief [Pixelmon](https://pixelmonmod.com/) spinoff), with a forth on the way as of November 2021. Each iteration has coincided with a summer or winter break, and starting with the 2nd and 3rd map incoming members of the class of 2025 also joined us.

While I don't have accurate metrics across server iterations, over 250 players from the Northwestern community have been manually added to the server's whitelist, with tens of players consistently online during school breaks. As life returns to being in person once more, player activity has dwindled as people are more occupied with activities in the real world. But especially throughout the pandemic, this server provided a fun place for Northwestern community members to meet and hang out with one another, and has led to the creation of several friendships lasting to this day. It's also been a way for me to test out certain Minecraft server development and design methodologies without having to compete to build an organic playerbase. I've been developing Minecraft servers for nearly a decade at this point, but it is sometimes difficult to test new ideas when you're also trying to manage the business aspects and retain a player count to test with.

Here are some key tenets of my design of these servers and how I went about implementing them:

### Accessibility for new or inexperienced players 
A driving goal of my design was for this server to accommodate players of any skill level, whether they've never played before or have been playing for a decade. I explain more about how this works below, but some key focuses were on providing resources for help and allowing extra or more advanced content to be optional for inexperienced players.

Upon logging in, players would receive a book with information about the server itself, its rules, and any custom content. We also had [written documentation](https://docs.google.com/document/d/1M3Pj1upfYACaIvH_9hX_CI2bOQamLUoKqvhOX_qquZ0/edit?usp=sharing) for some common server commands that players would frequently find themselves using. For the first two maps, we also chose to implement cross-compatibility between Java and Bedrock editions of the game, so that console or mobile users could also join in. This feature was later removed in map 3 due to moderation difficulties and missing Minecraft features that hurt the Bedrock player experience.

### Focus on community building
My biggest concern was that players would just log in and run off to their own section of the map, never interacting with anyone else until they got bored enough to stop playing. There were a few ways I went about mitigating this, including implementing a world border to contain players to a common space, disabling spawn region protection to encourage community projects, and running various whole-server events to bring players together. Some of these events included a holiday-themed visit to the "North pole" (named after a player, North), a gladiator fighting tournament, and collective tackling of difficult dungeons that were added in map 3.

These seemed to work well, and very soon after the start of each map players would form villages together and would frequently ask others to play with them. Some of these groups even got so tight that they became friends once they ended up on campus, and have remained strong friendships throughout college.

### Impactful and attractive gameplay changes
Another way to entice players and keep them engaged with the server was done though the addition of content not present in the base ("vanilla") game or in a singleplayer world. These included expansive cave generation with new formations and biomes, new world biomes with varying flora and structures, and additions to game lore such as abandoned villages or dungeons ruled by monsters. The dungeons became especially important when they premiered in map 3, as they were full of loop but extremely difficult for players to defeat on their own. Players often banded together to tackle these, and would leverage tools like the web map to try and find as many of them as possible. There was also an MMO-style skills system that players could level up to unlock special abilities and attributes.

Despite all of these things, this server was actually very close to vanilla Minecraft. While some of these features were new or enhancements to existing Minecraft features, none of them were so over-the-top as to detract from the original game's experience. This was an intentional choice of mine as I wanted players to be able to engage as much or as little with the custom content as they felt like.

### High performance servers
My goal was to have as little bloat as possible that would affect this server's performance, since its baseline demands were so high -- tens of players all over the map exploring and doing stuff at once plus activity loggers for our web map and moderation tools requires a lot of computing power. My solution on the software side was to keep the number of server plugins down and use server software such as [Paper](https://github.com/PaperMC/Paper) to help meet our needs. I programmed in any extra features that were essential to the server but did not require an entire plugin. On the hardware side, this server ran on a recently purchased Dell R430 machine with faster CPU, SSD, and RAM speeds to keep up with the processing demands.

## World downloads

You can find world downloads [here](https://drive.google.com/drive/folders/1FR7JbUFGJXvERUmktMjmRGRukG1UjnBE?usp=sharing).

If the server is still up, you can view a web map of the current server here: https://map.numc.me

## Pictures
TODO