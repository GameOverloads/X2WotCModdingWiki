---
layout: page
title: "Mod Troubleshooting"
permalink: /PlayingWithMods/ModTroubleshooting/
---

# Preventing Problems

Follow these general recommendations to reduce the chances of problems occurring while playing with mods.

## Use Alternative Mod Launcher

The 2K Launcher has limited functionality and often fails to load mods. If your **[game release](/X2WotCModdingWiki/PlayingWithMods/X2Releases/)** supports the **[Alternative Mod Launcher](/PlayingWithMods/ModLaunchers/#alternative-mod-launcher)**, it's highly recommended you use it - it's very reliable and has a lot of features. Note: if you run Steam with administrator privileges, then make sure to launch AML **as administrator** as well.

![Run As Administrator by Right Clicking on the Shortcut or Executable](/X2WotCModdingWiki/PlayingWithMods/Player_PlayingWithMods/images/ModTroubleshooting_1.png)

## Do not enable Framerate Smoothing

If **Framerate Smoothing** is enabled in game's settings, it may interfere with **[UIScreenListeners](https://www.reddit.com/r/xcom2mods/wiki/uiscreenlisteners)** and **[ModClassOverrides](https://www.reddit.com/r/xcom2mods/wiki/index/mod_class_overrides)**, which are commonly used in mods.

![Framerate Smoothing Option in Options](/X2WotCModdingWiki/PlayingWithMods/Player_PlayingWithMods/images/ModTroubleshooting_2.png)

## Avoid playing in Ironman mode

Even without any mods, there is a risk that the game will corrupt your save, breaking your campaign forever. If you do play true Ironman, make sure to make backups of your **[Saved Games folder](#where-does-the-game-store-saves)** frequently.

## Use the right mods for the right version of the game

All XCOM 2 mods can be split into two categories:

1) **Mods made with vanilla XCOM 2 SDK.** They are intended for the vanilla XCOM 2 game, and trying to use most of them in WOTC will cause gamebreaking issues. "I have installed a bunch of mods and now my game doesn't work" problem is typically caused by using vanilla mods in War of the Chosen expansion.

How to tell if a vanilla mod is safe to use in WOTC:

* The mod description explicitly states that the mod is compatible with WOTC.

* There's a workshop comment from the mod author stating that.

* There are workshop comments from mod users stating that - less reliable, may turn out to be false.

* Almost all vanilla voicepacks and mods that add soldier cosmetics work in WOTC just fine.

**Note:** the 2K Launcher is unable to load vanilla mods with WOTC, so you have to use **[other methods](/X2WotCModdingWiki/PlayingWithMods/ModLaunchers/)** to load them.

2) **Mods made with XCOM 2 War of the Chosen SDK.** They are intended for the XCOM 2 War of the Chosen, and will not work vanilla XCOM 2.

How to tell if a mod was made for WOTC:

* War of the Chosen DLC is **[marked as required](https://i.imgur.com/Mx1yNAx.png)**.

* It has "WOTC" in its name.

*  In Alternative Mod Launcher, the "For WOTC" column will say "true" for WOTC mods. 

* It changes something that exists only in WOTC (e.g. Lost or Factions).

## Be careful about using mods with known issues

Check the [List of Problematic Mods](/X2WotCModdingWiki/PlayingWithMods/ProblematicMods/) to see if any of the mods you are using are known to cause problems. Maybe you should avoid using them.

## Use bugfix mods for other mods when necessary

Check the [List of Mods with Fixes Available](/X2WotCModdingWiki/PlayingWithMods/ModsWithFixes/) to see if any of the mods you are using have bugfix mods available.

## Use newer and better mods when possible

Check the [List of Superseded Mods](/X2WotCModdingWiki/PlayingWithMods/SupersededMods/) to make sure you're using the best and latest versions of popular mods.

## Do not remove mods mid campaign

Some mods can cause issues if removed mid-campaign. Unfortunately, there's no easy way for a regular mod user to know which mods can be removed mid-campaign safely. Mods that make no gameplay changes are usually safe to remove, especially mods that only add soldier cosmetics, but if a mod makes gameplay changes or adds new items, it's generally better to keep it until your next campaign, unless the presence of the mod is causing gamebreaking issues.

## Regenerate User Config often

You should **[Regenerate User Config](#regenerate-user-config)** every time before starting a new campaign. It can also resolve some issues caused by removing mods mid-campaign.

## Alien Hunters and Highlander

If you have the **Alien Hunters DLC**, and you are using Highlander of version 1.22 or higher, then you should also install the [**[WOTC] Alien Hunters Community Highlander**](https://steamcommunity.com/sharedfiles/filedetails/?id=1796402257) plugin.

Do not install this plugin if you do not have the Alien Hunters DLC, otherwise you may experience game breaking issues. You may also see an empty popup window from time to time.

******
# Frequently Asked Questions 

## Are there are any error logs or crash dumps? 

The latest log file is:

    ..\Documents\My Games\XCOM2 War of the Chosen\XComGame\Logs\Launch.log

Previous logs are also stored in the same folder.

The log file is rarely helpful in determining the cause of a crash, but some mods print debug messages into the log, so if you want to help a mod author fix a bug in their mod, giving your log file to them might be helpful.

Even without any mods, the game tends to spam a lot of warnings and errors into the log, so don't be alarmed. Errors and warnings that mention NetObject are safe to ignore. 

The game also stores crashdumps, but they can be used only with debug tools we do not have.

## How do I use the console?

The debug/cheat console is often used to resolve various issues with the game. **[Go here for instructions.](https://www.reddit.com/r/xcom2mods/wiki/index/console_commands)**

## Where does the game store saves?

`..\Documents\my games\XCOM2 War of the Chosen\XComGame\SaveData\`

## What is the maximum number of mods I can play with?

According to [**this post**](https://www.reddit.com/r/xcom2mods/comments/mdz8qt/combining_mods_into_one_for_personal_use_lower/), if you have more than 1292 mods, the game will be unable to create save game files. There are no other known limits.

Depending on how many "big" mods you are using - mods that take up a lot of computer memory - you may run out of virtual memory, causing a crash.

******
# Troubleshooting

XCOM 2 by itself is not a very stable game and sometimes crashes and corrupts saves even without any mods installed. Playing with incompatible or bad mods may make it crash more often. This article will help you solve some of the most common issues with the game, but there is no way to make it absolutely stable.

Look for your problem in the list below.

## My game crashes on launch even without any mods!

[**Verify integrity**](#verify-game-integrity) of the game's files. This will make sure your game itself is fine. 

Install **[Visual C Redistributables](https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/)**, **[DirectX](https://www.microsoft.com/en-us/download/details.aspx?id=35)**, update drivers for your hardware.

Check the integrity of Windows itself by using **[SFC and DISM](https://www.windowscentral.com/how-use-dism-command-line-utility-repair-windows-10-image)** console commands.

If the game still doesn't work after that, look into other software and hardware problems with your PC.

## My game crashes with mods!

1. Take a long hard look at your mod list. Make sure you are using the [right mods for your version of the game](#use-the-right-mods-for-the-right-version-of-the-game). For example, **[Long War 2](https://steamcommunity.com/sharedfiles/filedetails/?id=844674609)** will never work with WOTC, use **[Long War of the Chosen instead](https://github.com/long-war-2/lwotc/wiki/Installing-Long-War-of-the-Chosen)** instead.

2. If the game always crashes in the same spot, like when starting the game, or after completing Gate Crasher or loading a specific mission, use [Binary Search](#binary-search) to find problematic mod(s).

3. Keep in mind XCOM 2 is not a particularly stable game, and it is more or less normal for it to crash once in a while. 

## My game freezes on launch!

Do you get a white or black XCOM 2 window that never loads? 

If so, open the [**Launch.log file**](#are-there-are-any-error-logs-or-crash-dumps), and see if there's a "crash detected" message at the end. 

If there is, then this is effectively a crash. Follow the "My game crashes" troubleshooting steps above.

If not, you most likely have to wait just a few minutes more for the game to launch. The game can take a while to launch if you have a lot of mods and you store your game on a slow storage device.

If the game still doesn't load even after 15 minutes or more, then treat this problem as a crash anyway.

## The game is not loading mods!

1. If you're using the 2K Launcher, look into **[other methods](/X2WotCModdingWiki/PlayingWithMods/ModLaunchers/)** of loading mods, as the 2K Launcher often fails to load mods.

2. If you're using the Alternative Mod Launcher, make sure you do not have `-regenerateinis` [launch argument](https://www.reddit.com/r/xcom2mods/wiki/launch_arguments/) enabled. It makes the game recreate configuration files every time you start the game, wiping the list of active mods. Disable it and launch the game twice, the game should start loading mods on the second launch.

3. Make sure Framerate Smoothing is disabled in game's settings, it prevents many mods from working.

4. An overzealous antivirus may interfere with Alternative Mod Launcher's ability to launch the game or write the list of mods to the game's configuration file.

5. Cloud backup software that monitors the Documents folder, such as OneDrive, can also prevent the game from working properly, since it stores its configuration in the Documents folder.

## My save file got corrupted!

Unfortunately there is no known way of recovering corrupted saves. Load a previous save or start a new campaign.

## I get a white screen in Tactical!

Nobody knows exactly what causes this bug or how to prevent it. The suspected culprits are mods that affect the camera zoom distance or rotation angles, like [Free Camera Rotation](https://steamcommunity.com/sharedfiles/filedetails/?id=616359783). A temporary fix is simply saving and loading.

## I get huge lag on Geoscape!

"Geoscape" refers to the "world map" screen in Strategy. This lag is a symptom of **[Mod Class Override](https://www.reddit.com/r/xcom2mods/wiki/index/mod_class_overrides)** conflicts. If you use **[Alternative Mod Launcher](/X2WotCModdingWiki/PlayingWithMods/ModLaunchers/)**, you get warnings about those. The only MCO conflict that is safe to ignore is the `X2Action_MoveClimbWall` one. All others should be treated as hard conflicts that mean you cannot use these mods together.

## I am subscribed to a mod, but it doesn't appear in the mod launcher!

This issue can appear in several different ways:

1) Steam has failed to download the mod. First, confirm this is actually the case by trying to find the mod in the workshop folder using the ModID method **[described here](https://www.reddit.com/r/xcom2mods/wiki/wotc_modding/mod_folder)**.

If the mod is there, then try the other solutions mentioned below.

If the mod is not there, then it means Steam has not downloaded the mod. This can happen for two main reasons:

1. You have the launcher or any other Steam game open, which normally prevents Steam from downloading content.

1. Steam has malfunctioned. 

Your options are the same in either case:

1. Unsubscribe from the mod.

1. Restart PC.

1. Start Steam.

1. Subscribe to the mod.

1. Wait a few minutes for the download to start and complete. You can monitor download status via the bar at the bottom.

1. Start your mod launcher and see if the mod is there.

1. If the mod still doesn't download, try **[Verifying Integrity of game's assets through Steam](#verify-game-integrity)**, which will verify and force download subscribed mods as well. 

1. If the mod still doesn't download, then contact Steam support or [**download the mod from elsewhere.**](/X2WotCModdingWiki/PlayingWithMods/DownloadInstallMods/)

2) You are using the Alternative Mod Launcher and the mod is hidden. 

Solution: In AML, enable the toggle **Options -> Show hidden mods**. Find the problematic mod, right click it and select "Unhide".

**Why the mod has become hidden?**

When using AML, you're supposed to get rid of unwanted mods by right clicking them and selecting Delete. This will:

1. Delete the mod from your storage device.
1. Delete the mod's entry in AML's settings.json file.
1. Unsubscribe you from the mod on Steam. 

If you just unsubscribe from the mod from Steam, this will also delete the mod's files, but the mod's entry in AML's settings.json will remain.

The next time you launch AML, it will show a popup warning, saying that a mod is missing, and offering to hide the mod. If you close the popup without reading or understanding it, then the mod will become hidden, and will remain hidden even if you resubscribe to the mod.

3) You are using the Alternative Mod Launcher and you cannot see the mod because of the filters or the search bar. Empty the search field by clicking on the red cross icon near it, and remove all active filters by clicking the "Clear" button in the lower right corner. 

![Example image.](/X2WotCModdingWiki/PlayingWithMods/images/ModTroubleshooting_ModHiddenSearch.png)

******
# Fixes

## Regenerate User Config

**Purpose:** removing broken or unnecessary configuration added by mods. 

The User Config folder is located at:

    ..\Documents\my games\XCOM2 War of the Chosen\XComGame\Config\

1. Delete or rename this folder. Only this folder. **DO NOT** touch the config folder in the game installation directory.

1. Start the game without any mods, then exit the game. The game will use the default configuration files to recreate the config folder, effectively resetting the game's settings to their defaults, as well as any configuration changes you have done in [Mod Config Menu](https://steamcommunity.com/sharedfiles/filedetails/?id=667104300).

1. Start the game again with mods you want to play with. Change the game's settings however you prefer and configure the mods through Mod Config Menu, if you want to. Exit the game.

1. All done. The next time you start the game you can begin playing normally.

Note: if you have to do this fix every time just to be able to launch the game, then the problem is not with the configuration files, the problem is with the mods you're trying to use.

## Verify Game Integrity

**Purpose:** fixing broken game's files.

<!-- [Video instruction for verifying the game through Steam](https://youtu.be/dGMkYLu091s) -->

<iframe width="560" height="315" src="https://www.youtube.com/embed/dGMkYLu091s" title="How to Verify Integrity of Game Files on Steam
" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Verifying the game through Steam will reset any changes you may have done to the game's or mod's files. So if you have manually changed configuration files for some of your workshop mods, these changes will be undone.

If you're using a non-steam version, use whichever platform you have acquired XCOM to verify game's files or reinstall it.

If you're using a pirated version of the game, then we cannot help you.

Make sure to [**regenerate user config**](#regenerate-user-config) after game's files are verified.

## Binary Search

**Purpose:** finding problematic mod(s) in the quickest way.

["What is Binary Search?"](https://www.mwmythicmods.com/argent/tech/bin_srch.html)

**Before you start:**

* If your current campaign is in **Ironman** mode, backup your Saves folder: `..\Documents\my games\XCOM2 War of the Chosen\XComGame\SaveData\`
* If your Character Pool has soldiers with mod-added cosmetic body parts, backup the Character Pool file: `..\Documents\my games\XCOM2 War of the Chosen\XComGame\CharacterPool\DefaultCharacterPool.bin`
* If you are using Alternative Mod Launcher, save your your current mod list as a text file on the Profiles tab.

![Profiles tab in Alternate Mod Launcher](ModTroubleshooting_ProfilesTab.png)

**The search:**

Disable half of your currently enabled mods. Remember or write down which mods you disabled. 

Start the game and check if your problem has gone away. Keep in mind that some problems will not be resolved when loading a mid-mission save, even if the culprit mod has been removed. In those cases, you will have to load a save on Avenger and deploy on a mission to check for the problem.

If the problem is still there - repeat the process. Disable half of your currently disabled mods, and check again.

If the problem has gone away, then it means it was likely caused by one of the mods you have disabled. Now, disable all mods, and enable the mods that you have disabled on the previous step. 

Now the problematic mod(s) should be in the group of mods you have active.

Disable half of this group, and check if the problem has gone away. And so on.

Repeat the process until you have just one mod that causes the problem.

When you find the problematic mod(s), it would be great if you were to send a bug report to the mod author. 

# Additional Resources #
*****

* [Deacon's Top Ten Guide to Troubleshooting Long War 2 (and XCom 2)](https://pavonisinteractive.com/phpBB3/viewtopic.php?t=23701)


# What kind of PC do I need to play XCOM 2 with lots of mods?

1. A CPU with good per-core (single thread) performance will make the game run generally faster. This generally includes i5 and i7 Intel CPUs past 6th generation, as well as Ryzen Zen 2 CPUs. 

1. You will need a sufficiently powerful GPU (Graphics Card) to play the game at high settings. Generally anything at the level of GTX 1060 6GB or above is more than enough. Naturally, you will need a more powerful GPU if you wish to play at 2k or 4k resolution with high framerate. Ideally you should use an nVidia GPU for the hardware PhysX support.

1. Having your operating system (Windows) and the game installed on an SSD will improve loading times, particularly if it's a PCIE NVME SSD. This is also where your [windows page file](https://www.tomshardware.com/news/how-to-manage-virtual-memory-pagefile-windows-10,36929.html) should be.

1. More RAM will let you play with more mods that take up a lot of disk space, especially voicepacks. 16 GB is generally good enough, but even that may not be enough if you have lots of mods with large file size. You can see the mod filesize in Steam Workshop interface, as well as in the Alternative Mod Launcher.

![Mod sizes in a Steam Workshop item](/X2WotCModdingWiki/PlayingWithMods/images/ModTroubleshooting_ModFilesize.jpg)
