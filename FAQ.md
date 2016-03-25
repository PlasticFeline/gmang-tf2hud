# Introduction #

This HUD is too complicated, as you can tell by this obnoxiously wordy wiki. Hopefully, I will make an installer some day. Until then, have an FAQ.

# Table of Contents #
  1. [What's G-Mang HUD?](#What's_G-Mang_HUD?.md)
  1. [How can I contact you?](#How_can_I_contact_you?.md)
  1. [How do I install/update the HUD?](#How_do_I_install/update_the_HUD?.md)
  1. [What's an Override?](#What's_an_Override?.md)
  1. [How do I use Overrides?](#How_do_I_use_Overrides?.md)
  1. [What are Common Overrides?](#What_are_Common_Overrides?.md)
  1. [What are Pre-Overrides?](#What_are_Pre-Overrides?.md)
  1. [What are File Swaps?](#What_are_File_Swaps?.md)
  1. [How do I add/customize functionality on the Main Menu buttons?](#How_do_I_add/customize_functionality_on_the_Main_Menu_buttons?.md)
  1. [How do I use custom crosshairs?](#How_do_I_use_custom_crosshairs?.md)
  1. [How can I customize my Medic layout/Ubercharge elements?](http://code.google.com/p/gmang-tf2hud/wiki/FAQ#How_can_I_customize_my_Medic_layout/Ubercharge_elements?)
  1. [What's the deal with the Vaccinator UI?](#What's_the_deal_with_the_Vaccinator_UI?.md)
  1. [Can I change layouts to look like Povo's or Valve's?](#Can_I_change_layouts_to_look_like_Povo's_or_Valve's?.md)
  1. [How do I toggle/customize Closed Captions?](#How_do_I_toggle/customize_Closed_Captions?.md)
  1. [How do I toggle/customize Scoreboard?](#How_do_I_toggle/customize_Scoreboard?.md)

# What's G-Mang HUD? #
A weird HUD with lots of functionality. Most text is outlined, lots of bright colors are used, and there are a bunch of supported options.
  * **Wiki:** [Articles list](http://code.google.com/p/gmang-tf2hud/w/list)
  * **Screenshots:** [Cropped](http://code.google.com/p/gmang-tf2hud/wiki/ScreenshotsCropped) or [Full](http://code.google.com/p/gmang-tf2hud/wiki/ScreenshotsFull)
  * **Patch History:** [Changelog](http://code.google.com/p/gmang-tf2hud/wiki/Changelog)
  * **Download:** [File list](http://code.google.com/p/gmang-tf2hud/downloads/list)
  * **Steam Group:** [G-Mang HUD Updates](http://steamcommunity.com/groups/gmanghud)

# How can I contact you? #
If you have a question or comment, posting on either the [Gotfrag thread](http://www.gotfrag.com/tf2/forums/thread/428175/) or [ETF2L thread](http://etf2l.org/forum/general/topic-10210/?recent=274422) is a good choice. It lets other people answer the question if I'm busy, gets answers to others who didn't think to ask your question, and gives new forum users a chance to see the HUD. If you'd rather get immediate feedback (particularly if you caught a bug/error in a recent HUD update), you can talk to me on [Steam](http://steamcommunity.com/id/g-mang). Otherwise, just PM me on Gotfrag or ETF2L and I'll respond when I can.

# How do I install/update the HUD? #
Before installing or updating, you should back up your current HUD. This is easy to do.
  1. Locate your **tf** folder. It's usually here: **C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\**
  1. Rename your **resource** and **scripts** folders (if they exist). Something like **backup-resource** and **backup-scripts** is fine.
You can then safely install/update to the latest G-Mang HUD by getting the latest download [here](http://code.google.com/p/gmang-tf2hud/downloads/list) and performing the following:
  1. Open the ZIP archive containing the HUD.
  1. Within the ZIP archive, open the folder. Within this folder, you should see a **tf** folder and **readme.txt**.
  1. Open this **tf** folder and copy its **resource** and **scripts** folders.
  1. Paste into your own **tf** folder that you located in the first step of this FAQ answer.
  1. Restart TF2 if it's current running.

To uninstall the hud, simply rename, move, or delete your **resource** and **scripts** folders.

# What's an Override? #
"Overrides" are simply a way to redefine your HUD's color palette in a centralized manner. More specifically, an Override is a custom color definition that is stored in your **ClientScheme.res** file that overrides a default color definition. Instead of going to files individually to pimp out your HUD, you can just override all the colors you want by defining them in a single file. There are a few advantages to this:
  * It's much much easier to update your HUD, as you only have to worry about the contents of 1 file (**ClientScheme.res**) instead of all files you've ever recolored.
  * It's easier to customize elements that are hard to find in the HUD files, because all color definitions use the same type of nomenclature.
  * In many cases, you can make sweeping edits with very little trouble.
Also of note: Overrides are used to enable/disable elements, such as [Custom Crosshairs](http://code.google.com/p/gmang-tf2hud/wiki/Crosshairs). This avoids excessive amounts of renamed files for File Swaps, and lets you save your preferences for updates by simply backing up your list of Overrides.

# How do I use Overrides? #
To use Overrides, locate your ClientScheme.res:
  1. Locate your **resource** folder. It should be in this directory: **C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource\**
  1. Using Notepad, Wordpad, or some other plain text editor, open the file called **ClientScheme.res**.
You should see a section for Overrides. As a rule of thumb, lines of text that start with slashes (`//`) are ignored by the game code. If a wiki page tells you to use specific overrides, you can just go ahead and paste them into that section of **ClientScheme.res**. Whenever you're done editing Overrides, be sure to make a backup copy of them (or your **ClientScheme.res** file), because the file is frequently replaced in TF2 patches.

After changing **ClientScheme.res**, you must restart TF2 (if it's running) for those changes to take effect.

# What are Common Overrides? #
Common Overrides are Overrides provided for you so you don't have to go out and make/find them yourself. To enable them, simply remove the slash pairs (`//`) at the start of their lines. For example, if you want to change your damage text from magenta-colored to yellow, you should remove the `//`'s from the lines under `//Yellow Damage Text`, taking these lines:
```
/// YELLOW DAMAGE TEXT /////////////////////////
	//"DamageTextHit"				"ColorYellow"
	//"DamageTextLast"				"ColorYellow"
```
and turning them into:
```
/// YELLOW DAMAGE TEXT /////////////////////////
	"DamageTextHit"				"ColorYellow"
	"DamageTextLast"				"ColorYellow"
```
You can disable them again by adding the slashes (`//`) back into the start of those lines.

# What are Pre-Overrides? #
Pre-Overrides are just the default overrides; they make up the color palette for G-Mang HUD, chosen by yours truly. If you want to make a custom Override, copy a Pre-Override, paste it into the Custom Overrides section, and edit the new line to your heart's content.

More can be learned about Pre-Overrides from here: [OverridesList](http://code.google.com/p/gmang-tf2hud/wiki/OverridesList)

# What are File Swaps? #
File Swaps are alternative HUD files. TF2 only loads HUD files of specific names. By renaming files, you can redirect TF2 to load special options for layouts and functionality. For example, to switch your Health bar from rectangular to cross-shaped...
  1. Locate your **ui** folder. It should be in this directory: **C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource\ui\**
  1. Delete the file named **HudPlayerHealth.res**.
  1. Copy the file named **HudPlayerHealth\_CROSS.res** and paste it into the same folder. This should create a file called **HudPlayerHealth\_CROSS - Copy.res**.
  1. Rename the new file from **HudPlayerHealth\_CROSS - Copy.res** to **HudPlayerHealth.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.
The reverse can be done by using the file called **HudPlayerHealth\_BOX.res** instead of **HudPlayerHealth\_CROSS.res**.
Pretty much all File Swaps work exactly that way.

# How do I add/customize functionality on the Main Menu buttons? #
The Main Menu buttons don't come with functions because they require the user to define their preferences to work (for example, there are no universal "Home Server" bookmarks--people define it individually); additionally, but leaving their functions out of the HUD files, they allow for smoother HUD updates because overriding your HUD files won't override your button commands.

To add functionality to your main menu buttons, locate your autoexec.cfg file...
  1. Locate your **cfg** folder. It should be in this directory: **C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\cfg\**
  1. Using Notepad, Wordpad, or some other plain text editor, open the file called **autoexec.cfg**. If it does not exist, copy a different .cfg file in the **cfg** folder, rename the new copy to **autoexec.cfg**, and empty its contents.
... and paste into it the following lines...
```
//Bookmarked Servers
alias JoinHomeServer "connect ; password ; rcon_password "
alias JoinBookmark1 "connect ; password "
alias JoinBookmark2 "connect ; password "
alias JoinBookmark3 "connect ; password "

alias CreateIdle "map_background cp_dustbowl"   //Replace cp_dustbowl with preferred map

alias CreateTestServer "map cp_badlands;TestServerCVars"   //Replace cp_badlands with preferred map

alias TestServerCVars "sv_cheats 1;mp_autoteambalance 0;mp_disable_respawn_times 1;mp_respawnwavetime 0;mp_teams_unbalance_limit 0;sv_cheats 1;sv_pure 0;tf_weapon_criticals 0;tf_use_fixed_weaponspreads 1"

alias STVDemoMode "exec DEMOPLAYBACKCONFIG"   //Replace DEMOPLAYBACKCONFIG with preferred demo playback script

alias ToggleInterface ""
alias ToggleInterfaceMatch "cl_hud_minmode 1;alias ToggleInterface ToggleInterfacePub; "   //Add custom scripting after semicolon if desired
alias ToggleInterfacePub "cl_hud_minmode 0;alias ToggleInterface ToggleInterfaceMatch; "   //Add custom scripting after semicolon if desired

ToggleInterfaceMatch
```
... then edit it to your heart's content. For more information, see [MainMenu](http://code.google.com/p/gmang-tf2hud/wiki/MainMenu).

# How do I use custom crosshairs? #
Learn the basics of [Overrides](#What_are_Common_Overrides?.md) and then see [Crosshairs](http://code.google.com/p/gmang-tf2hud/wiki/Crosshairs).

# How can I customize my Medic layout/Ubercharge elements? #
Learn the basics of [Overrides](#What_are_Common_Overrides?.md) and [File Swaps](#What_are_File_Swaps?.md) and then see [MedicOptions](http://code.google.com/p/gmang-tf2hud/wiki/MedicOptions).

# What's the deal with the Vaccinator UI? #
Vaccinator's UI elements were set up by Valve in ways that don't work well with the HUD. Elements have hard-coded (unmovable) positions relative to other elements, it won't hide extra shadow/outline text (which the hud uses heavily) when ubercharge text needs to be hidden, and the meter doesn't allow for the screen-width sizing like the regular charge meter does.

**Vaccinator users:** If the Vaccinator UI is bothering you, I recommend switching to a [Cross or Povo health bar](http://code.google.com/p/gmang-tf2hud/wiki/Settings#Player_Health_Shape), using the [Bottom or Middle Ubercharge placement](http://code.google.com/p/gmang-tf2hud/wiki/MedicOptions#Ubercharge_Placement), and using the following [common overrides](http://code.google.com/p/gmang-tf2hud/wiki/Settings#Overrides):
  * /// REDUCE UBERCHARGE TEXT OUTLINE AND SHADOW //
  * /// HIDE TINY UBERCHARGE TEXT UNDER CROSSHAIR //
Before-and-after shot [here](http://i.imgur.com/fCTKpRq.jpg).

# Can I change layouts to look like Povo's or Valve's? #
Learn the basics of [Overrides](#What_are_Common_Overrides?.md) and [File Swaps](#What_are_File_Swaps?.md) and then see [Layouts](http://code.google.com/p/gmang-tf2hud/wiki/Layouts).

# How do I toggle/customize Closed Captions? #
The TF2 console command `closedcaptions "1"` enables Closed Captions; `closedcaptions "0"` disables them. For more information, see [ClosedCaptions](http://code.google.com/p/gmang-tf2hud/wiki/ClosedCaptions).

To change to more concise Closed Caption sets, use File Swaps on the .dat files in your **resource** folder. More information can be found here: [ClosedCaptions](http://code.google.com/p/gmang-tf2hud/wiki/ClosedCaptions)

Currently, the source files for Closed Captions aren't public. The main reason I'm doing this is because I want actual feedback on the current Caption sets. Once the HUD comes out of Beta, I will put the source files into the HUD files.

# How do I toggle/customize Scoreboard? #
When not using minmode, the default scoreboard is designed for 32-player games or smaller. When minmode is on, the scoreboard will switch to a 12-player variant for competitive games. Minmode can be toggled with the console command `cl_hud_minmode "x"`, where `x` is `1` to enable and `0` to disable.

In addition, there are a few [File Swaps](#What_are_File_Swaps?.md) for Scoreboards that allow you to change its functionality. Their names are listed as **ScoreboardX-Y.res** where **X** is the non-minmode function and **Y** is the minmode function; "COMP" refers to the compact scoreboard that's similar to the 12-player one, but even more concise.