## General Info ##
> Current version: [Beta 31 (2013 February 09)](http://code.google.com/p/gmang-tf2hud/downloads/detail?name=gmanghudpublicbeta31.zip)

> Screenshots still quite outdated, sorry. :S

The G-Mang TF2 HUD is a Team Fortress 2 interface that focuses on practicality over aesthetics. It's derived from Valve's minmode HUD (minmode now just toggles 12p and 32p scoreboard) and is not meant to be compatible with other HUDs.

If you'd like announcements on HUD updates, you can join the [G-Mang HUD Updates steam group](http://steamcommunity.com/groups/gmanghud).

Supported aspect ratios are 5:4, 4:3, 16:10, 16:9, 2:1, preferred resolution 1440x900 (anything wider than 5:4 should probably work).

Information about the HUD can be found on [the wiki](http://code.google.com/p/gmang-tf2hud/w/list). Newer users might want to check out the [FAQ](http://code.google.com/p/gmang-tf2hud/wiki/FAQ).


Enjoy,

G-Mang

## Screenshots ##
Screenshots are a couple versions outdated; new ones are on the way.
  * _For cropped screenshots, see: [ScreenshotsCropped](http://code.google.com/p/gmang-tf2hud/wiki/ScreenshotsCropped)_
  * _For full-size screenshots, see: [ScreenshotsFull](http://code.google.com/p/gmang-tf2hud/wiki/ScreenshotsFull)_

The HUD generally uses compact, centered elements with bright colors for maximum clarity, as seen here:
> [![](http://img718.imageshack.us/img718/7519/hudcapheavythumb.png)](http://code.google.com/p/gmang-tf2hud/wiki/ScreenshotsCropped)
Screenshots can be found [here (cropped)](http://code.google.com/p/gmang-tf2hud/wiki/ScreenshotsCropped) or [here (full-size)](http://code.google.com/p/gmang-tf2hud/wiki/ScreenshotsFull).

## Installation ##
If you're familiar with using a custom HUD, skip to the **Settings** section.

### Backup ###
Before installing, you should back up your current HUD. This is easy to do.
  1. Locate your tf folder. It's usually here: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\
  1. Rename your **resource** and **scripts** folders (if they exist). Something like **backup-resource** and **backup-scripts** is fine. If you ever want to uninstall the HUD, simply change the names back.
You can return to the default TF2 HUD by renaming or deleting the new **resource** and **script** folders that came with the G-Mang HUD.

### File Transfer ###
To install the HUD, simply open the zip archive and extract the contents of its **tf** folder into your own **tf** folder, which is usually located here: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\ .

### Settings ###
  * _See: [Settings](http://code.google.com/p/gmang-tf2hud/wiki/Settings)_

The following CVAR settings are recommended:
```
cl_spec_carrieditems "0"
cl_use_tournament_specgui "1"
hud_combattext "1"
```
You can make these run automatically by pasting them into your **autoexec.cfg** file, which should be here: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\cfg\ (if it's not, create a text file with notepad called **autoexec.cfg**).

There are a variety of ways to customize the hud, including changing the color scheme, choosing between layout options, and switching some elements to default. See [Settings](http://code.google.com/p/gmang-tf2hud/wiki/Settings).

The HUD has two modes: Match Mode and Pub Mode. Toggling between the two is done with the `cl_hud_minmode "#"` command, with `"1"` being Match Mode and `"0"` being Pub Mode.

## Special Thanks ##
Special thanks goes to all the private beta testers, especially Dec and Remedy, and all the public beta feedback-givers, especially Basik, Seacow, and Winnie.

And of course, thanks to all the hud makers out there who let me learn from their sharing, including (in no particular order): m0re, flame, povohat, perl, berg, idnk, revan\_xp, numlocked, broesel, link. Extra special thanks to noid.

## Updates ##
  * _See: [Changelog](http://code.google.com/p/gmang-tf2hud/wiki/Changelog)_
Updates will become less frequent when the HUD moves out of the Beta stage. Features currently planned/in-the-works are revisions to presently untouched panels, closed captions, and eventually an integrated script set.

### Latest Update(s) ###

#### Beta 31 (2013 February 09) ####
  * Patched files in accordance with recent updates
  * Fixed HUD elements for MvM Heavy Rage Meter and Spy Sapper Meter
  * Added support for Vaccinator; it's not pretty, see FAQ: http://code.google.com/p/gmang-tf2hud/wiki/FAQ#What%27s_the_deal_with_the_Vaccinator_UI?