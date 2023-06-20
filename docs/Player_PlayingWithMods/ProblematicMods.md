---
layout: page
title: "List of Problematic Mods"
permalink: /PlayingWithMods/ProblematicMods/
---


# List of Problematic Mods

The following mods are known to cause gamebreaking issues.

# Sensor Fences

[Sensor Fences](https://steamcommunity.com/sharedfiles/filedetails/?id=1732068221) crashes the game after completing the mission if one of the fences was destroyed. Usually it's possible to load a save and continue playing, this issue will not cause the the game to crash again in the same spot.

# Quick Soldier Info

[\[WOTC\] Quick Soldier Info](https://steamcommunity.com/sharedfiles/filedetails/?id=1125117314) sometimes causes the camera to get stuck under terrain for some people. Usually happens during the Avenger Defense mission. You can disable this mod temporarily to get through the problematic spot, and then enable it again.

Also, allegedly this mod is responsible for making building roofs no longer transparent. Supposedly, disabling its feature of taking photos mid-tactical in MCM fixes the problem.

# Tactical Armory UI

[Tactical Armory UI](https://steamcommunity.com/sharedfiles/filedetails/?id=1962124733) is known to cause crashes while scrolling through equipment.

# Automatic Gatecrasher Fail

These mods are known to cause the bug where upon starting a new campaign, the first mission - Gatecrasher - is automatically failed. The bug happens when a mod submits the NewGameState in `InstallNewCampaign()`, or creates a Game State in `OnLoadedSavedGame()`, but does not add it to History.

* TBD

# Map Mods

Vast majority of map mods are known to cause gamebreaking issues, such as generating missions that always crash during the load, or failing to place objectives properly so the mission cannot be completed without the use of cheats. If you care about having stable gameplay, avoid map mods like fire.