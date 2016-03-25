# Introduction #

The HUD comes with a small sampling of custom crosshairs with unique functionality. These crosshairs can be used in conjunction with Valve's in-game crosshairs and/or netgraph crosshairs should they be desired. Custom crosshairs may not display properly on especially small or large resolutions.

# Crosshair Types #
![![](http://imgur.com/IAVt2.png)](http://imgur.com/IAVt2.png)

By default, custom crosshairs are disabled. For those interested in trying them out, _Achievement tracker Text cross_ and the _Permanent Dot_ crosshairs are recommended (provided as Common Overrides).

There are currently five kinds of crosshair shapes that come with the HUD:
  * **Text cross:** The text cross is a small, thin plus sign (+). Its foreground color can be customized, but its outline cannot.
  * **Circle:** Also based on text, but shaped like a circle. Its foreground color can be customized, but its outline cannot.
  * **Dot:** The smallest possible outlined crosshair of a 1x1 dot above a 2x2 dot. Both foreground and outline colors can be changed.
  * **Big cross:** Drawn using areas of color in the HUD, forming a large plus sign (+). Both foreground and outline colors can be changed.
  * **Small cross:** Drawn using areas of color in the HUD, forming a thick--but relatively short--plus sign (+). Both foreground and outline colors can be changed.

There are currently three modes for crosshair display:
  * **Achievement tracker:** The custom crosshair is visible whenever you are tracking an achievement that would appear on your current class (open your achievements, find one you haven't done, and check the box for "Show on HUD"); leaving this enabled removes the actual visibility of achievement trackers. For example, if you track the achievement "Out of the Park", the custom crosshair will be visible whenever you go Scout, but the actual achievement tracker will not appear. If you have already done all achievements for a given class, track general achievements instead (holiday ones are a good choice); if you've done all general achievements as well, you'll have to use another method of displaying a custom crosshair (google "netgraph crosshair"). When making custom scripts, you can make this crosshair appear and disappear automatically with the console command `hud_achievement_tracker`. The crosshair is placed in front of all other crosshairs (including Valve's).
  * **Minmode:** The custom crosshair is visible whenever minmode is on (console command `cl_hud_minmode 1`). This allows for scripting a class-specific crosshair even when you can't track any achievements, though it may cause conflicts with scoreboard toggling (you might want to fileswap for a non-changing scoreboard). The crosshair is placed behind all other crosshairs except the Permanent custom crosshair.
  * **Permanent:** The custom crosshair is visible whenever the default Valve HUD would show your class icon (generally at all times while alive and not looking at scoreboard). The crosshair is placed behind all other crosshairs.

# Recommended Crosshairs #
The two recommended custom crosshairs are the Achievement tracker Text cross Custom crosshair and the Permanent Dot Custom crosshair. To make these easier to enable, they have been provided as Common Overrides. To use these...

  1. Locate your resource folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource
  1. Using Notepad, Wordpad, or some other plain text editor, open the file called **ClientScheme.res**.
  1. Remove slashes to turn these lines...

```
/// PERMANENT DOT CROSSHAIR ////////////////////
	//"CHPermaDotBG"			"ColorBlack"
	//"CHPermaDotFG"			"ColorGreen"
	
/// ACHIEVEMENT TRACKER TEXT CROSS CROSSHAIR ///
	//"CHAchText"			"ColorGreen"
```
> ... into this:

```
/// PERMANENT DOT CROSSHAIR ////////////////////
	"CHPermaDotBG"			"ColorBlack"
	"CHPermaDotFG"			"ColorGreen"
	
/// ACHIEVEMENT TRACKER TEXT CROSS CROSSHAIR ///
	"CHAchText"			"ColorGreen"
```
Save and restart TF2 if it's currently running.

# Adding Custom Crosshairs #
Before adding custom crosshairs, any other crosshairs under the same "mode" (see above) should be removed.

## Achievement Tracker Crosshairs ##
The following are overrides for each crosshair shape available for the Achievement tracker display mode.

Text Cross:
```
		"CHAchText"					"ColorGreen"
```

Circle:
```
		"CHAchCircle"				"ColorGreen"
```

Dot:
```
		"CHAchDotBG"				"ColorBlack"
		"CHAchDotFG"				"ColorGreen"
```

Big Cross:
```
		"CHAchBigHorizBG"				"ColorBlack"
		"CHAchBigHorizFG"				"ColorGreen"
		"CHAchBigVertBG"				"ColorBlack"
		"CHAchBigVertFG"				"ColorGreen"
```

Small Cross:
```
		"CHAchSmallHorizBG"			"ColorBlack"
		"CHAchSmallHorizFG"			"ColorGreen"
		"CHAchSmallVertBG"			"ColorBlack"
		"CHAchSmallVertFG"			"ColorGreen"
```

## Minmode Crosshairs ##
The following are overrides for each crosshair shape available for the Minmode display mode.

Text Cross:
```
		"CHMinmodeText"					"ColorGreen"
```

Circle:
```
		"CHMinmodeCircle"				"ColorGreen"
```

Dot:
```
		"CHMinmodeDotBG"				"ColorBlack"
		"CHMinmodeDotFG"				"ColorGreen"
```

Big Cross:
```
		"CHMinmodeBigHorizBG"				"ColorBlack"
		"CHMinmodeBigHorizFG"				"ColorGreen"
		"CHMinmodeBigVertBG"				"ColorBlack"
		"CHMinmodeBigVertFG"				"ColorGreen"
```

Small Cross:
```
		"CHMinmodeSmallHorizBG"			"ColorBlack"
		"CHMinmodeSmallHorizFG"			"ColorGreen"
		"CHMinmodeSmallVertBG"			"ColorBlack"
		"CHMinmodeSmallVertFG"			"ColorGreen"
```

## Permanent Crosshairs ##
The following are overrides for each crosshair shape available for the Permanent display mode.

Text Cross:
```
		"CHPermaText"					"ColorGreen"
```

Circle:
```
		"CHPermaCircle"				"ColorGreen"
```

Dot:
```
		"CHPermaDotBG"				"ColorBlack"
		"CHPermaDotFG"				"ColorGreen"
```

Big Cross:
```
		"CHPermaBigHorizBG"				"ColorBlack"
		"CHPermaBigHorizFG"				"ColorGreen"
		"CHPermaBigVertBG"				"ColorBlack"
		"CHPermaBigVertFG"				"ColorGreen"
```

Small Cross:
```
		"CHPermaSmallHorizBG"			"ColorBlack"
		"CHPermaSmallHorizFG"			"ColorGreen"
		"CHPermaSmallVertBG"			"ColorBlack"
		"CHPermaSmallVertFG"			"ColorGreen"
```

# Custom Crosshair Overrides #
The following constitute all custom crosshair-related pre-overrides:
```
		"CHAchCircle"				"NotVisible"
		"CHAchDotBG"				"NotVisible"
		"CHAchDotFG"				"NotVisible"
		"CHAchBigHorizBG"				"NotVisible"
		"CHAchBigHorizFG"				"NotVisible"
		"CHAchBigVertBG"				"NotVisible"
		"CHAchBigVertFG"				"NotVisible"
		"CHAchSmallHorizBG"			"NotVisible"
		"CHAchSmallHorizFG"			"NotVisible"
		"CHAchSmallVertBG"			"NotVisible"
		"CHAchSmallVertFG"			"NotVisible"
		"CHAchText"					"NotVisible"
		"CHMinmodeCircle"				"NotVisible"
		"CHMinmodeDotBG"				"NotVisible"
		"CHMinmodeDotFG"				"NotVisible"
		"CHMinmodeBigHorizBG"				"NotVisible"
		"CHMinmodeBigHorizFG"				"NotVisible"
		"CHMinmodeBigVertBG"				"NotVisible"
		"CHMinmodeBigVertFG"				"NotVisible"
		"CHMinmodeSmallHorizBG"			"NotVisible"
		"CHMinmodeSmallHorizFG"			"NotVisible"
		"CHMinmodeSmallVertBG"			"NotVisible"
		"CHMinmodeSmallVertFG"			"NotVisible"
		"CHMinmodeText"					"NotVisible"
		"CHPermaCircle"					"NotVisible"
		"CHPermaDotBG"				"NotVisible"
		"CHPermaDotFG"				"NotVisible"
		"CHPermaBigHorizBG"			"NotVisible"
		"CHPermaBigHorizFG"			"NotVisible"
		"CHPermaBigVertBG"				"NotVisible"
		"CHPermaBigVertFG"				"NotVisible"
		"CHPermaSmallHorizBG"			"NotVisible"
		"CHPermaSmallHorizFG"			"NotVisible"
		"CHPermaSmallVertBG"				"NotVisible"
		"CHPermaSmallVertFG"				"NotVisible"
		"CHPermaText"				"NotVisible"
```
Text crosshairs only have a single element (outline is always black, entire crosshair is one shape). Dot crosshairs have two elements (foreground dot, which is usually green, and background dot, which forms the outline and is generally black). Big and Small crosshairs have four elements: horizontal foreground, vertical foreground, horizontal background, and vertical background. One can decipher these elements within the keywords in the overrides (see "Crosshair Types" above for definitions):
  * `CH`: Stands for "crosshair". All custom crosshair elements use this prefix.
  * `Ach`: Stands for "achievement tracker". These elements appear while the Achievement tracker is on.
  * `Minmode`: Self-explanatory. These elements appear while minmode is enabled.
  * `Perma`: Stands for "permanent". These elements are almost always visible.
  * `Circle`: Self-explanatory: These elements are Text-based circle crosshairs.
  * `Dot`: Self-explanatory. These elements form Dot-shaped crosshairs.
  * `Big`: Stands for "Big cross". These elements form Big cross-shaped crosshairs.
  * `Small`: Stands for "Small cross". These elements form Small cross-shaped crosshairs.
  * `Text`: Self-explanatory. These elements are Text-based cross crosshairs.
  * `Horiz`: Stands for "Horizontal rectangle". These elements constitute the "row" portion of the Short cross and Big cross crosshairs.
  * `Vert`: Stands for "Vertical rectangle". These elements constitute the "column" portion of the Short cross and Big cross crosshairs.
  * `BG`: Stands for "Background rectangle". These elements form the outlines for all custom crosshairs that aren't Text-based.
  * `FG`: Stands for "Foreground rectangle". These elements form the inner color for all custom crosshairs that aren't Text-based.

By reading the aforementioned pre-overrides using the above keywords, one can fully customize their HUD crosshairs. For example, making a Minmode Small cross Crosshair with red inner color and a white outline would be done with these overrides:
```
		"CHMinmodeSmallHorizBG"			"ColorWhite"
		"CHMinmodeSmallHorizFG"			"ColorRed"
		"CHMinmodeSmallVertBG"			"ColorWhite"
		"CHMinmodeSmallVertFG"			"ColorRed"
```