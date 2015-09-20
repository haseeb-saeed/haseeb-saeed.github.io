---
layout: post
title: Pokemon Stardrop
cover: pokemon_stardrop/cover.png
date:	2015-04-22
categories: posts
---

Pokemon Stardrop was an original game set within the Pokemon universe; built upon Pokemon Fire Red, this ROM hack boasted an original storyline with new gameplay features, maps, graphics, and music.

## Building a Pokemon Game

Apart from some spritesheets and music (and the base game itself), Pokemon Stardrop was built entirely by me. The story begins with the player's father being kidnapped by Team Rocket. The entire story revolves around the protagonists journey to rescue their dad and stop Team Rocket from their plan of world domination and Pokemon enslavement.

Although there were plenty of tools available for hacking Pokemon Fire Red, I concsciously tried to use as few as possibly, mainly because I wanted to learn as much about how the game was constructed as I could and also because some of the tools were buggy and could often accidentally break existing things in the game. The tools I ended up using were:

* A map editor
* A script editor (that would compile scripts and insert them into the ROM)
* Tools for extracting compressed and uncompressed graphics
* A hex editor
* Photoshop/Paintshop Pro
* A tilemap editor
* A trainer editor (to modify trainers to battle against)
* A tool for inserting music

Some of the tools I decided not to use were other editors that would edit the Pokemon data, item data, etc; I was able to do this manually by searching the specific hex strings in the ROM and modifying them appropriately.

![_config.yml]({{ site.baseurl }}/images/pokemon_stardrop/screenshots_3.png)

Many areas of the ROM were relatively unknown or very poorly documented to the hacking community. Some of these things that I came became proficient in modifying (and wrote tutorials on and helped others out with) were:

* Modifying the map of the world
* Resizing overworld sprites, allowing for larger graphics in the game
* Creating custom voicegroups, allowing for music tracks to have a larger variety of different instruments

## New Features

![_config.yml]({{ site.baseurl }}/images/pokemon_stardrop/screenshots.png)

Some of the features that I implemented that were not originally available in Pokemon FireRed or that were not common to Pokemon games at the time were:

* Minigames, such as a minigame to allow the player to dig and find treasure
* Lots and lots of sidequests
* A berry system that would allow the player to plant and watch berries grow
* All 386 Pokemon available for capture

## Scripting

Pokemon FireRed has its own primitive scripting language for creating events. The language itself was pretty limited in what it would do, and since I didn't know enough about the implementation to add my own additions to the language, I often had to come up with unique ways to try and implement things.

![_config.yml]({{ site.baseurl }}/images/pokemon_stardrop/screenshots_2.png)

Some of the highlights of the lanuage were:

* Variables - predefined locations in memory that could be set from 0x0 - 0x1000. The only operations on variables were setting a value, copying a value, addition/substraction, and equality comparison
* Flags - essentially variables that would only ever be set to 0 or 1 (basically a boolean variable)
* Specials - these basically activate some predefined event that was hardcoded into the ROM (a screen flash, healing pokemon, etc.)
* Operations for directly manipulating RAM
* Message boxes for printing dialogue
* Movement operations to move sprites around
* Call, return, gosub, goto functions for calling or moving to other routines

More info coming soon...
