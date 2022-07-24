---
title: "Bridging the \"Code Translation\" of Assets"
date: 2022-07-23
description: "Using text serialization and modular content to bring non-code assets to life in games."
tags: [blog, programming, game design]
draft: false
---

In a literal sense, video games are just code. But more specifically, they are collections of art, writing, sound, animation, design, and much more transformed into code. The problem is that computers can't read and understand things like art and writing in the same way that you and I can. So we have to find ways to translate it for computers! However, figuring out how to translate those things into code or implement them in a game engine is a problem with no perfect solution.

There are hundreds if not thousands of tools out there for getting various non-code aspects of games into a form that computers can understand. Many large studios have their own proprietary toolsets, such as [Obsidian's branching dialogue software](https://www.youtube.com/watch?v=oRHl2PLKwfY) or [Bethesda's Creation Kit](https://en.wikipedia.org/wiki/Creation_Engine#Creation_Kit). These studios can also afford to hire roles that specialize in this "physical to electronic" transformation, such as technical artists or scripters. Even mid-size to indie studios can get in on the latter technical roles to help bring their concepts to life.

But what about very small teams like ours? At the moment, KeyWave is composed of 5 people who all fulfill very distinct roles. I am the only programmer, and one of two who have any experience with Unity. With that in mind, let's explore some potential solutions to asset implementation problems and see why they may not work for us. I'll refer to all of the things that need to be digitized and implemented in the engine (such as writing, art, sound, etc) as "non-code assets".

### Why not make custom tooling / use existing online tools to bring non-code assets into the game?

The first option is just too complex for a team of our size and a project of this size. If I decided to make custom tooling for everything, the game itself would never be finished. As for existing online tools, we are actually using several! For example, we are using [Yarn Spinner](https://yarnspinner.dev/) for implementing our writing into the game. Yarn is awesome because it does the technical heavy lifting and avoids me having to write an entire branching dialogue system from scratch. But for some things specific to our game, custom tools just don't exist. Our game features a phone and PC with several apps, each of which may contain screens, documents, files, contacts, emails, etc. These systems are all written by me and as such, there's no existing software to allow our non-programmers to add their content to them.

### Why not implement all of the non-code assets myself (as the programmer)?

Similarly to why it doesn't make sense to write fully custom tooling, it would be a huge timesink to have to not only create the tech for the game but also implement all of the other work from our team. Trying to do so may also result in a worse final product because the way I implement something may not line up with how the designer wanted it to be implemented. It's best if programmers can be free to do their thing while designers maintain the freedom to implement their visions.

### Why not let the other designers implement their work into the game themselves?

As mentioned earlier, other than me only one other person has experience with Unity. While the other designers are more than welcome to pick up Unity and put their work in themselves, that can take a lot of time to learn and do for people who already have plenty of other work on their plates. They also may not be familiar with the current technical layout of the project, so even if they were familiar with the engine they may not know where their work should be put in the project.


So what's the solution here? In my opinion, this is where **text serialization** and **modular design** shine. I recently watched [Chad Jenkins' GDC talk](https://www.youtube.com/watch?v=aE5zrjt-gdg) about sandbox design in Kerbal Space Program as I was researching sandbox systems, and it really resonated with me. His idea was simple: if you store game content on disk as individual "modules" comprised of English text, then it becomes simple for anyone (even end users!) to add, modify, and remove content as they please. This also eases the work on the game systems, as they no longer need to be informed about how to handle every individual piece of content but rather they can follow a set of rules and have content modules swapped in and out as the user pleases while providing expected behavior.

This is the approach I have taken with KeyWave and other recent projects of mine. Rather than having our designers implement things in the engine or having me do it for them, all they need to do to add content (in our case, things like emails, contacts, texts, webpages, etc) is edit a JSON file. While JSON files do have relatively strict formatting so that deserializers can understand them, they are not super technical and are in English so that even people without coding knowledge can understand and modify them. This also makes the work easier for me; instead of having to code in or add objects for all of the various content, I can just write systems that read from various JSON files and manipulate the content as they are designed. It also allows us to quickly and easily change content without having to hunt down and modify various references in the editor or codebase.

Writing serializers and the data structures that they store is a relatively trivial process, so it frees up more time for me to focus on systems and mechanics (you know, making a game). All I provide to our designers is documentation that explains to them how the content they add should be formatted and then let them do their thing! You can check out an example of the documentation I write on our [GitHub wiki](https://github.com/jackburkhardt/KeyWave/wiki/Adding-Contacts).

I'm not claiming to have reinvented the wheel here -- I'm just reiterating what others have said about the benefits of modular approaches to game design and providing a productivity solution for tiny teams with few tech people. I highly, highly encourage you to watch Jenkins' GDC talk linked above, as he explains all of this far better than I could ever do. Thanks for reading.


Written by:

Jack Burkhardt | Lead Programmer, KeyWave
mail@jackburkhardt.com | https://jackburkhardt.com
