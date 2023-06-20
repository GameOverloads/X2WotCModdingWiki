---
layout: page
title: "Launching XCom 2"
permalink: /PlayingWithMods/ModLaunchers/
---

# Mod Launchers

## [Alternative Mod Launcher](https://github.com/X2CommunityCore/xcom2-launcher/wiki/Installation) (AML)

Best launcher overall by far. It's highly recommended that you use it. [The official AML wiki](https://github.com/X2CommunityCore/xcom2-launcher/wiki) will explain how. It also has a troubleshooting page if you face any issues with AML specifically. 

## Firaxis Launcher

This launcher was previously used by default when the game was launched through Steam interface. It is located in: 

    ..\steamapps\common\XCOM 2\Binaries\Win64\Launcher\ModLauncherWPF.exe

This launcher is barebones, but functional, and it detects mods in your Local Mods folder automatically.

Note: by default, this launcher will start the game in debug mode, and with redscreens enabled. To be able to play the game in the regular mode, you have to add `-noRedscreens` and `-review` [launch arguments](https://www.reddit.com/r/xcom2mods/wiki/launch_arguments#wiki_old_firaxis_launcher).

## 2K Launcher

This launcher is used by default when the game is launched through Steam interface. It is located in:

    ..\steamapps\common\XCOM 2\Launcher\launcher.exe

Unfortunately, it has issues that make it extremely undesirable to use:

1) Sometimes the launcher becomes unable to launch the game, even when not using any mods.

2) Most of the time, it doesn't detect mods in your Local Mods folder.

3) It doesn't let you use vanilla mods with WOTC. 

Using vanilla mods with WOTC is a bad idea most of the time, but in some isolated cases it is perfectly fine to do, notably vast majority of vanilla voicepacks work in WOTC without any issues.

4) Sometimes that mod launcher fails to load mods, period.

5) Sometimes the launcher "forgets" you already have the game purchased and fails to launch the game.

The community had to come up with [awkward hacks](https://steamcommunity.com/sharedfiles/filedetails/?id=2145343945) to address this.

## No-Steam Versions

Only the steam version officially supports mods, but it's possible to play with mods with other versions as well. First, try getting Alternative Mod Launcher to work without Steam by using a workaround [**explained here**](https://github.com/X2CommunityCore/xcom2-launcher/wiki/FAQ#is-there-a-way-to-use-aml-without-steam) (note: doesn't work for Epic Games Store version of the game)

Alternatively, you can configure the game to load mods without using any mod launcher. This method was organized and written by Rand and confirmed to work with the GoG version of the game.

1) **[Download mods](/X2WotCModdingWiki/PlayingWithMods/DownloadInstallMods)** and **[install them manually](/X2WotCModdingWiki/PlayingWithMods/DownloadInstallMods#how-to-install-mods-manually)**.

2) Write down file names of `.XComMod` files of all mods that you wish to use, without the extension. For example, if the file name is `AugmentsWotCCodexBegone.XComMod`, then write down `AugmentsWotCCodexBegone`.

You will need these names later.

3) Locate your `DefaultModOptions.ini` file:

Use this file if you intend to play vanilla XCOM 2:

    ..\XCOM 2\XComGame\Config\DefaultModOptions.ini

Use this file if you intend to play XCOM 2 War of the Chosen expansion:

    ..\XCOM 2\XCom2-WarOfTheChosen\XComGame\Config\DefaultModOptions.ini

4) Open that file. Under the `[Engine.XComModOptions]`, add a line for each mod `ActiveMods="ModFilenameYouCopiedExactly"`. For example:

    [Engine.XComModOptions]
    
    ActiveMods="TerrorFromTheDerp"
    ActiveMods="AnnounceDemo"
    ActiveMods="AvengerAssembled"
    ActiveMods="Squadsize_EU"

All done. You can now launch the game normally and play with mods. Notes: 

* Mods may not be detected on your first launch of the game. So if nothing works, try launching the game again.
* The order of modnames in this file does not matter.