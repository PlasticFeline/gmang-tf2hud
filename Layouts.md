# Introduction #

Though the HUD has a variety of features one might wish to use, it's not designed for parts of it to be copied over to other HUDs. In light of this, layout schemes are provided that may be preferable to players who are used to other HUDs.

Fileswaps and overrides are used to change layouts. Information about these can be found on [Settings](http://code.google.com/p/gmang-tf2hud/wiki/Settings).


# Valve Style #

![![](http://img340.imageshack.us/img340/9902/hudcapoptionvalvethumb.png)](http://img89.imageshack.us/img89/8439/hudcapoptionvalvefull.png)

Players that like the default TF2 HUD can use the Valve-inspired layout. This only requires two fileswaps:

  1. Locate your ui folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource\ui
  1. Delete the file named **HudPlayerHealth.res**.
  1. Copy the file named **HudPlayerHealth\_VALVE.res** and paste it into the same folder. This should create a file called **HudPlayerHealth\_VALVE - Copy.res**.
  1. Rename the new file from **HudPlayerHealth\_VALVE - Copy.res** to **HudPlayerHealth.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.

  1. Locate your ui folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource\ui
  1. Delete the file named **HudAmmoWeapons.res**.
  1. Copy the file named **HudAmmoWeapons\_VALVE.res** and paste it into the same folder. This should create a file called **HudAmmoWeapons\_VALVE - Copy.res**.
  1. Rename the new file from **HudAmmoWeapons\_VALVE - Copy.res** to **HudAmmoWeapons.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.

In addition to these, the [Valve Alternate Ubercharge Percentage Placement](http://code.google.com/p/gmang-tf2hud/wiki/MedicOptions#Ubercharge_Percentage_Placement) is recommended.

# Povo Style #

![![](http://img156.imageshack.us/img156/1812/hudcapoptionspovothumb.png)](http://img210.imageshack.us/img210/833/hudcapoptionspovofull.png)

With Povohat's retirement from HUD editing, PVHud users may wish to try a new HUD with a similar appearance. This can be done using G-Mang HUD with an override and three fileswaps.

To perform the override...

  1. Locate your resource folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource
  1. Using Notepad, Wordpad, or some other plain text editor, open the file called **ClientScheme.res**.
  1. Hit Ctrl+F to bring up the search bar and search for `Alternate Player Health Colors`.
  1. Remove slashes to turn these lines...

```
/// ALTERNATE PLAYER HEALTH COLORS /////////////
	//"PlayerHPColorSelf"				"ColorWhite"
	//"PlayerHPColorSelfLow"			"ColorVermillion"
```

> ... into this:

```
/// ALTERNATE PLAYER HEALTH COLORS /////////////
	"PlayerHPColorSelf"				"ColorWhite"
	"PlayerHPColorSelfLow"			"ColorVermillion"
```

Save and quit TF2 if it's running.

The fileswaps are as follows:

  1. Locate your ui folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource\ui
  1. Delete the file named **HudPlayerHealth.res**.
  1. Copy the file named **HudPlayerHealth\_POVO.res** and paste it into the same folder. This should create a file called **HudPlayerHealth\_POVO - Copy.res**.
  1. Rename the new file from **HudPlayerHealth\_POVO - Copy.res** to **HudPlayerHealth.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.

  1. Locate your ui folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource\ui
  1. Delete the file named **HudAmmoWeapons.res**.
  1. Copy the file named **HudAmmoWeapons\_POVO.res** and paste it into the same folder. This should create a file called **HudAmmoWeapons\_POVO - Copy.res**.
  1. Rename the new file from **HudAmmoWeapons\_POVO - Copy.res** to **HudAmmoWeapons.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.

  1. Locate your ui folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource\ui
  1. Delete the file named **HudObjectiveFlagPanel.res**.
  1. Copy the file named **HudObjectiveFlagPanel\_COMPACT.res** and paste it into the same folder. This should create a file called **HudObjectiveFlagPanel\_COMPACT - Copy.res**.
  1. Rename the new file from **HudObjectiveFlagPanel\_COMPACT - Copy.res** to **HudObjectiveFlagPanel.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.

In addition to these, the [Povo Alternate Ubercharge Percentage Placement](http://code.google.com/p/gmang-tf2hud/wiki/MedicOptions#Ubercharge_Percentage_Placement) is recommended.