# Introduction #
There are a variety of ways the HUD can be easily customized to suit your preferences.

For settings related to [Closed Captions](http://code.google.com/p/gmang-tf2hud/wiki/ClosedCaptions), [Custom Crosshairs](http://code.google.com/p/gmang-tf2hud/wiki/Crosshairs), [Medic Options](http://code.google.com/p/gmang-tf2hud/wiki/MedicOptions), [Layouts](http://code.google.com/p/gmang-tf2hud/wiki/Layouts) and see their respective wiki pages.

## Console Commands ##
The HUD has two modes: Match Mode and Pub Mode. Match mode is turned on with the following command:
`cl_hud_minmode "1"`
Pub Mode is turned on with the following command:
`cl_hud_minmode "0"`
Additionally, the following commands are recommended:
```
cl_spec_carrieditems "0"
cl_use_tournament_specgui "1"
hud_combattext "1"
```
Commands can be set to automatically run by pasting them into your autoexec file, which should be located in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\cfg\. If the file is missing, create a text document in the \cfg\ folder using Notepad and name it **autoexec.cfg**.

## Main Menu Functions ##
The custom main menu has buttons for user-defined functions. In order to specify these, copy the following code into your autoexec.cfg file, which should be located in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\cfg\ (if the file is missing, create a text document in the \cfg\ folder using Notepad and name it **autoexec.cfg**); edit the contents in quotations according to comments made after `//`.
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
If you prefer playing pubs to matches, replace the last line with `ToggleInterfacePub`.

## ClientScheme Overrides ##
> _See also: [OverridesList](http://code.google.com/p/gmang-tf2hud/wiki/OverridesList)_

**When using Overrides, it's very important that you frequently make backup copies of your ClientScheme file, as it's replaced frequently in updates (both HUD and TF2), and typos as small as forgetting a quotation mark can break your game interface entirely.**

ClientScheme Overrides require program restart to take effect.

If there are any color choices you don't like, or if there are areas of color (such as progress bar notches) you want to hide/show, you can manipulate these elements by adding Overrides to your ClientScheme file.
  1. Locate your resource folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\cfg\resource
  1. Using Notepad, Wordpad, or some other plain text editor, open the file called **ClientScheme.res**.
Toggling Common overrides:

Toggling Common overrides is the simplest and easiest form of using overrides. All you need to do is delete the `//` in front of a line in order to activate it (or add `//` to deactivate it). For example, if you had a form of color-blindness that made the magenta damage text undesirable, you should remove the `//`'s from the lines under `//Yellow Damage Text`, taking these lines:
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
If a line does not have quotes, you should not be removing any `//`'s from it. This override, among others, can be seen in [this screenshot](http://img682.imageshack.us/img682/7105/hudscreenoverridefull.png).

Custom overrides should be created under the `CUSTOM OVERRIDES` header. Users uncomfortable with HUD editing should avoid using Custom Overrides. To find a list of properties that can be given overrides, scroll down to the section called `G-MANG HUD PRE-OVERRIDES`. Copy and paste lines from this section into your `CUSTOM OVERRIDES` section (Cutting or Deleting things from the Pre-Overrides is discouraged) and edit the second string in the new lines. The following is an example custom override that turns damage text orange:
```
//////////////// COMMON OVERRIDES //////////////////
// simple overrides that can be toggled
// remove forwardslash pairs before quotations to enable
	
	//Damage Text Recolor
	"DamageTextHit"				"ColorOrange"
	"DamageTextLast"				"ColorOrange"
	
```

## File Swaps ##
By manipulating files, you can choose to switch to the cross-style health image in some places. See screenshots for examples.

### Player Health Shape ###
Some players may prefer cross-shaped health, as shipped originally with the game . This can be implemented with a simple file swap (seen in [this screenshot](http://img693.imageshack.us/img693/5921/hudscreenswapfull.png) as follows:
  1. Locate your ui folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\cfg\resource\ui
  1. Delete the file named **HudPlayerHealth.res**.
  1. Copy the file named **HudPlayerHealth\_CROSS.res** and paste it into the same folder. This should create a file called **HudPlayerHealth\_CROSS - Copy.res**.
  1. Rename the new file from **HudPlayerHealth\_CROSS - Copy.res** to **HudPlayerHealth.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.
The reverse can be done by using the file called **HudPlayerHealth\_BOX.res** instead of **HudPlayerHealth\_CROSS.res**.

### Tournament Spectator Health ###
Because of the method used for formatting rectangular health icons, the tournament spectator HUD sometimes displays awkwardly stretched death icons. To avoid this, you can swap out the rectangular health icon on the tournament spectator panels for cross health icons (seen in [this screenshot](http://img195.imageshack.us/img195/6963/hudscreenmatchcrossfull.png). Instructions for doing this follow:
  1. Locate your ui folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\cfg\resource\ui
  1. Delete the file named **SpectatorTournamentGUIHealth.res**.
  1. Copy the file named **SpectatorTournamentGUIHealth\_CROSS.res** and paste it into the same folder. This should create a file called **SpectatorTournamentGUIHealth\_CROSS - Copy.res**.
  1. Rename the new file from **SpectatorTournamentGUIHealth\_CROSS - Copy.res** to **SpectatorTournamentGUIHealth.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.
The reverse can be done by using the file called **SpectatorTournamentGUIHealth\_BOX.res** instead of **SpectatorTournamentGUIHealth\_CROSS.res**.

## File Removal ##
> _See also: [RemoveableFilesList](http://code.google.com/p/gmang-tf2hud/wiki/RemovableFilesList)_

Some HUD elements can be safely returned to their Valve defaults by simply deleting or renaming their associated files. If, for example, you dislike the custom main menu, you can set it to Valve default by renaming **gamemenu.res** in tf/resource/ and **MainMenuOverride.res** in tf/resource/ui. The best way to experiment with this is to simply rename files instead of deleting them, ensuring that you always have backups.

The custom game icon can be removed by simply deleting **game.ico** in tf/resource/.