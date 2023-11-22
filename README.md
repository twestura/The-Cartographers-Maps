# The-Cartographers-Maps
Maps for The Cartographers.

This repository contains the source files used to generate the maps for *The Cartographers*.
The mod itself may be downloaded here: [https://www.ageofempires.com/mods/details/206556/](https://www.ageofempires.com/mods/details/206556/)

The maps in the repository include:

- Arabia
- Arena
- Black Forest
- Colosseum
- Eastern Coastline
- El Dorado
- Four Seasons
- Golden Lakes
- Hamburger
- Migration
- Monocle
- Nomad
- Outcrop
- Pacific Islands
- Rockslide
- Roe Rage
- Scandinavia
- Socotra
- Water Nomad
- ZeSnake
- ZeWall

## Map History

A variety of authors have contributed to Aoe2's map scripting scene over the years.
It's not always easy to track down the original of certain maps, but here I'll attempt to provide a history as best I can find it of the original authors and various maintainers of the maps.

### Arabia

The most standard Aoe2 map there is, the original version by Ensemble Studios was the bread and butter of AoC.
The particular version for this tournament is based on the version in Aoe2 DE from October 2023, authored by Chrazini.

### Arena

The best circus in town.
The map was originally included by Ensemble Studios in the Conquerors Expansion.
I've mostly rewritten this version from scratch.
The technique of generating forest lands in a circle is inspired by ideas seen in various Arena versions by Chrazini (e.g. Clown Arena).

### Black Forest

The original BF is a classic Aoe2 map from the original game, updated in AoC to include an additional South American jungle biome.
Usually BF is a 4v4 map, and the Rage Forest community maintains one of the most popular versions.

I rewrote this version, basing it mostly off of the version from AoC (in particular I do not use any of DE's Generating Objects code like Rage Forest does).
Most noteworth is the attempt to balance ponds by creating them in Land Generation rather than in Terrain Generation.

### Colosseum

An open land map with forest on the outside.
The original map was created by Chrazini for Battle of Africa.
This map is based on the version from [Battle of Africa III](https://www.ageofempires.com/mods/details/59226/).

### Eastern Coastline

A map with half land and half water, one team member starts on the mainland and the other on an island.
The original map was authored by AlgernonR, winning a map scripting competition for the [Escape Champions League](https://www.voobly.com/gamemods/mod/1010/ECL-Maps).

### El Dorado

A map where players start with Shallows under their TC, water on the ourside, Gold in the middle, and map revealers showing the Gold.
The original map was created by Gentle and has gone through various forms over the years, from having forest on the outside, to a full land map without water, to having beach terrain instead of Shallows under the TC.

This version of the script is written from scratch based on the general concept of the map.
It's pretty heavily rewritten using various features from DE.

### Four Seasons

A new map created for this tournament.
It was inspired by the map Four Quarters in [Double Cup 3](https://www.ageofempires.com/mods/details/109997/) by jasuni.

### Golden Lakes

A map by SAMEDO, with a few modifications for 9-Villager starts and 2v2 resource generation.
SAMEDO maintains a mod with the original map here: [https://www.ageofempires.com/mods/details/170898/](https://www.ageofempires.com/mods/details/170898/).

### Hamburger

A map with players on a central island, where both teams are separated by a central forest.
The original map was written by The_Prophet.
Originally a custom map, it is now an official map included with the HD and DE rereleases.

This script is a complete rewrite of the map script.
The version in DE as of October 2023 uses Connection Generation to create the forest between the players.
That implemetnation may sometimes leave gaps in the forest, where the water terrain is not covered.
This touranment's script uses `other_zone_avoidance_distance` along with DE's new terrain masking system to create the forest without gaps in terrain generation, and also leaves a few tiles of land terrain around the edges of the forest instead of a single tile of beach.

### Migration

A classic map included by Ensemble Studios in the Age of Kings.
This version is a complete rewrite of the map intended for 2v2s.

### Monocle

A map original by Chrazini, released in 2020 and used in various tournaments beginning with the [TeTe Invitational](https://www.ageofempires.com/mods/details/4136/).
Players start in a forested valley surrounded by an elevated ring of Shore Fish.
This tournament's version includes connections to ensure there are paths between players in the middle and ensures Relics spawn in a more consistent pattern.

### Nomad

A map from the Age of Kings, changed from an "age" in Aoe1 to a dedicated map in Aoe2.
This version of the map is based on the map from DE, but is modified to include both a classic start where one side of the land may touch the edge of the map, and to spawn Villagers in three groups of 3.

### Outcrop

Inspired by a custom map by Chrazini, appearing in [Red Bull Wololo Legacy](https://www.ageofempires.com/mods/details/94721/).
This tournament's script is rewritten from scratch to support a 2v2 start with players setup in a line, similar to the Special Map Frontline.

### Pacific Islands

Pacific Islands is a map script introduced by Forgotten Empires as part of the Rise of the Rajas expansion.
This tournament's script is a modified version of the script included in DE as of October 2023.

### Rockslide

Based on a map by Chrazini, initially released in 2020 for [Masters of RMS](https://www.ageofempires.com/mods/details/18265/).
This particular script decreases the size of the outer ring for 2v2s, spaces Relics more evenly, keeps Berries 1 tile away from the Mill on all sides (not just the right side), and adjust the distribution of Shore Fish to avoid the Mill and main Gold pile.

### Roe Rage

Based on the map for the [Delicious Whirled Cup 2023](https://www.ageofempires.com/mods/details/168480/) by dangerduck and TheMadCADer.
This tournament masks water for the fish under player TCs and adjusts the water and resource distribution in the center of the map to spawn more consistently.

### Scandinavia

Scandinavia was added by Ensemble Studios in the Conquerors Expansion (showing off snow terrain and footprints).
This version is a rewrite of the map, based loosely on the implementation of DE's version of the map as of October 2023.
In particular DE's implementation of lands to spawn the water is used to avoid the "octagon" of land borders displaying in one of the orientations.

### Socotra

Socotra is a tiny island first added by Forgotten Empires in *The African Kingdoms*.
This version is a rewrite loosely based on the script included in DE as of October 2023.
In particular it still uses a large empty area of water on the outside of the map instead of overriding the map size.

### Water Nomad

A map introduced by Forgotten Empires in the *Rise of the Rajas* DLC for HD.
This map spawns three groups of three Villagers, two groups of three Fishing Ships, and ensures each group of Fishing Ships spawns near a deep fish.

### ZeSnake

An original map written for this tournament.
It's an implemetnation of an idea from TheViper.

### ZeWall

A map with a Gaia Stone Wall separating teams.
Originally authored by Bazidrown and used in [Battle for Scotland](https://www.ageofempires.com/mods/details/55350/) (under the name Hadrian's Wall) and in [Wallhalla](https://www.ageofempires.com/mods/details/93668/).

This tournament rewrites most of the map script in order to balance the placement of resources for each team.
It makes use of a trick by TheMadCADer for using a restrictive terrain (here `ICYSHORE`) to force the placement of resources for each team to be on their own side of the wall.
The foundation terrain of the wall then is modified to replace this terrain with `DIRT`, hiding the presence of the ice.
