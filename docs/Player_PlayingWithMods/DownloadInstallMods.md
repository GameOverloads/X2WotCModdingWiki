---
layout: page
title: "Downloading and Installing Mods"
permalink: /PlayingWithMods/DownloadInstallMods/
---

This article will explain how to download and install mods. After you're done with that, go to **[this article](https://www.reddit.com/r/xcom2mods/wiki/index/starting_the_game)** to learn how to play with mods.

# How to Download Mods

## Steam Workshop

If you own XCOM 2 on steam, you can go to [**XCOM 2 Steam Workshop**](https://steamcommunity.com/app/268500/workshop/) and **Subscribe** to mods you wish to use. Steam will download and update subscribed mods automatically while you're not playing any Steam games.

All XCOM 2 mod launchers will automatically pick up mods downloaded this way, no further setup necessary.

### Troubleshooting: Steam doesn't download mods


[Go here.](/PlayingWithMods/ModTroubleshooting#i-am-subscribed-to-a-mod-but-it-doesnt-appear-in-the-mod-launcher
<!--
[Go here.](https://www.reddit.com/r/xcom2mods/wiki/mod_troubleshooting#wiki_i_am_subscribed_to_a_mod.2C_but_it_doesn.27t_appear_in_the_mod_launcher.21)
-->
## WorkshopDL

[WorkshopDL](https://github.com/VovoloGames/WorkshopDL) is a third-party standalone tool for downloading workshop mods even for games you don't own on Steam. It is essentially a [SteamCMD](#SteamCMD) with proper user interface, and it 
is the recommended way of getting mods for people who don't own XCOM 2 on steam.
<!--
[WorkshopDL](https://github.com/VovoloGames/WorkshopDL) is a third-party standalone tool for downloading workshop mods even for games you don't own on Steam. It is essentially a [SteamCMD](https://www.reddit.com/r/xcom2mods/wiki/index/download_mods#wiki_steamcmd) with proper user interface, and it 
is the recommended way of getting mods for people who don't own XCOM 2 on steam.
-->

## Skymods

[**Skymods**](https://catalogue.smods.ru/game/xcom-2/) mirrors Steam Workshop. For the most part, it offers the same mod selection as the workshop itself, but mods need to be downloaded and **[installed manually](#how-to-install-mods-manually)**, and obviously you will not be getting automatic updates.

## Steam Workshop Downloader

**[steamworkshop.download](http://steamworkshop.download/)** is a website that allows downloading individual workshop mods from Steam even if you don't own the game. It is meant as a replacement for the [**Steam Workshop Downloader**](https://steamworkshopdownloader.io/) website that has officially stopped working on May 26th, 2022.

## SteamCMD

SteamCMD is a downloadable tool that can be used to manually download mods from Steam Workshop, even if you don't own the game. 

Before you proceed:

1) **[Create a Steam account](https://store.steampowered.com/join/)**, if you don't have one already.

2) Write down mod IDs of each mod you intend to download. 

Go to [**Steam Workshop**](https://steamcommunity.com/app/268500/workshop/) and open the workshop page of the mod you want to download.

If you're using browser, you can copy the mod ID from the browser's address bar:

    https://steamcommunity.com/sharedfiles/filedetails/?id=2817073890

The number at the end is the mod ID.

If you're using Steam interface, you can click the "Share" button, and you will see a link to the mod, ending in mod ID.

Copy these mod IDs somewhere.

Now you're ready to download these mods using SteamCMD.

1) [**Download SteamCMD**](https://steamcdn-a.akamaihd.net/client/installer/steamcmd.zip) ([backup link](https://drive.google.com/file/d/1Pd4ZynLd6InwYmXRQA9ExyaIsZLVmmf0/view?usp=sharing)). Extract it to its own folder somewhere, and open `SteamCMD.exe`. A console command window will appear. Wait for SteamCMD to automatically download and install updates.

2) Enter command:

    login YourSteamName YourSteamPassword

If your account is protected by Steam Guard, you will receive an e-mail with confirmation code. Enter the code into the console.

3) For each mod ID you have written down previously, enter command:

    workshop_download_item 268500 modID

If the mod is large, you may need to wait for a while for it to download. Once the download is done, you will see a "Success" message and the path to which the mod has been downloaded. [**Example image.**](https://i.imgur.com/n5D4hi7.png)

After you download all the mods you wanted, you have to **[install them manually](#how-to-install-mods-manually)**.

## Nexusmods

Some XCOM 2 mods are available on [**Nexusmods**](https://www.nexusmods.com/xcom2/mods/). They have to be downloaded and **[installed manually](#how-to-install-mods-manually)**, as explained below.

Nexus has been mostly abandoned by the XCOM 2 modmaking community, so there are much fewer mods to choose from. However, there are a few Nexus mods that are not available on Steam due to their authors being banned from the Workshop.

# How to Install Mods Manually

1) Set up your Local Mods folder in the game's main directory.

Use this folder if you intend to play vanilla XCOM 2:

    ..\XCOM 2\XComGame\Mods

Use this folder if you intend to play XCOM 2 War of the Chosen expansion:

    ..\XCOM 2\XCom2-WarOfTheChosen\XComGame\Mods

2) Put the mods into this folder. If mods are in archives, you have to extract them. In the end, each individual mod must be in their own folder that contains the mod's `.XComMod` file. Example [image 1](https://i.imgur.com/U1XuGVb.jpg), [image 2](https://i.imgur.com/UIZ7olV.jpg).

For maximum safety and stability, the name of mod's folder should be the same as the name of the `.XComMod` file inside it, though strictly speaking this is important only for mods that replace the game's cooked assets. For War of the Chosen, the only known mod that does it is the X2 WOTC Community Highlander.
