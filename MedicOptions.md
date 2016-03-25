# Introduction #

Medics have to deal with a lot of very important information on-screen, and there are a number of ways they can customize the HUD to their liking.


# Medic Options #

Before getting started, read [Settings](http://code.google.com/p/gmang-tf2hud/wiki/Settings) to learn about Overrides and Fileswaps.

## Ubercharge Placement ##

There are three possible placements for the Ubercharge meter. These are...
  * **STRETCH:** The default option. The meter is stretched across the bottom of the HUD no matter what resolution you use, with a team-colored dividing line and a notch at 50%.
  * **BOTTOM:** The meter is placed at the bottom of the HUD with a fixed width (made to fit 5:4 aspect ratios or wider), with notches at 25%, 50%, and 75%.
  * **MIDDLE:** The meter is placed between the default health and ammo elements closer to the middle of the screen, with notches at 25%, 50%, and 75%.

## TargetID Name Text Size ##

For Medics, the ability to read the names on TargetID's can be especially important. In order to allow for more legible names, a simple Fileswap is provided. To use it...
  1. Locate your ui folder. It should be in this directory: C:\Program Files\Steam\steamapps\YOUR-STEAM-USERNAME\team fortress 2\tf\resource\ui
  1. Delete the file named **TargetID.res**.
  1. Copy the file named **TargetID\_BIG.res** and paste it into the same folder. This should create a file called **TargetID\_BIG - Copy.res**.
  1. Rename the new file from **TargetID\_BIG - Copy.res** to **TargetID.res**.
  1. If TF2 is open, enter the command **hud\_reloadscheme** into console.
The reverse can be done by using the file called **TargetID\_SMALL.res** instead of **TargetID\_BIG.res**.

## Tiny Ubercharge Text ##

Because the default Ubercharge notifications are somewhat far into peripheral vision, a tiny indicator of Ubercharge percentage is placed under the crosshair.

Some users may find the Tiny Ubercharge Text distracting or too much an impediment on visibility. In this case, it can be disabled with a common override. In your ClientScheme.res file, find the following lines...
```
/// HIDE TINY UBERCHARGE TEXT UNDER CROSSHAIR //
	//"UberchargeTextTiny"			"NotVisible"
	//"UberchargeTextTinyOutline"		"NotVisible"
	//"UberchargeTextTinyShadow"		"NotVisible"
	//"UberchargeFullTinyText1"	"NotVisible"
	//"UberchargeFullTinyText2"	"NotVisible"
	//"UberchargeFullTinyText3"	"NotVisible"
	//"UberchargeFullTinyText4"	"NotVisible"
	//"UberchargeFullTinyText5"	"NotVisible"
	//"UberchargeFullTinyText6"	"NotVisible"
```
... and delete slashes to turn them into...
```
/// HIDE TINY UBERCHARGE TEXT UNDER CROSSHAIR //
	"UberchargeTextTiny"			"NotVisible"
	"UberchargeTextTinyOutline"		"NotVisible"
	"UberchargeTextTinyShadow"		"NotVisible"
	"UberchargeFullTinyText1"	"NotVisible"
	"UberchargeFullTinyText2"	"NotVisible"
	"UberchargeFullTinyText3"	"NotVisible"
	"UberchargeFullTinyText4"	"NotVisible"
	"UberchargeFullTinyText5"	"NotVisible"
	"UberchargeFullTinyText6"	"NotVisible"
```

Instead of hiding the Tiny Ubercharge Text entirely, it can simply be made transparent, though doing so removes its anti-aliasing (line smoothness). This can be done with the following override (which will disable the default Tiny Text):
```
		//Transparent Tiny Ubercharge Text
		"UberchargeTextTinyTrans"			"UberYellowTrans"
		"UberchargeFullTinyText1Trans"	"ColorGreen128"
		"UberchargeFullTinyText2Trans"	"UberchargeFullTrans"
		"UberchargeFullTinyText3Trans"	"ColorGreen128"
		"UberchargeFullTinyText4Trans"	"UberchargeFullTrans"
		"UberchargeFullTinyText5Trans"	"ColorGreen128"
		"UberchargeFullTinyText6Trans"	"UberchargeFullTrans"
		"UberchargeTextTiny"			"NotVisible"
		"UberchargeTextTinyOutline"		"NotVisible"
		"UberchargeTextTinyShadow"		"NotVisible"
		"UberchargeFullTinyText1"	"NotVisible"
		"UberchargeFullTinyText2"	"NotVisible"
		"UberchargeFullTinyText3"	"NotVisible"
		"UberchargeFullTinyText4"	"NotVisible"
		"UberchargeFullTinyText5"	"NotVisible"
		"UberchargeFullTinyText6"	"NotVisible"
```

## Ubercharge Colors ##
The colors used on Ubercharge-related elements of the HUD can be customized fully, including the colors used when reaching 100% charge. By default, ubercharge text is light yellow and flashes two shades of green when charged. The default charge yellow can be changed by using and editing the following override:
```
		"UberchargeText"			"UberYellow"
		"UberchargeTextTiny"		"UberYellow"
```
If using the transparent Tiny Ubercharge Text (see above), the following must be changed:
```
		"UberchargeTextTinyTrans"	"UberYellowTrans"
```
The 100% Ubercharge flashing can also be changed easily, though they require more lines of editing. The only variants requested for this thus far are magenta charge, obnoxious green and magenta charge, and rainbow charge.

### Magenta Ubercharge ###
The magenta full charge effect allows for greater visibility against greenish backdrops. It is enabled with the following overrides:
```
		//Magenta Ubercharge
		"UberchargeFullTinyText1"	"ColorMagenta"
		"UberchargeFullTinyText2"	"ColorRuby"
		"UberchargeFullTinyText3"	"ColorMagenta"
		"UberchargeFullTinyText4"	"ColorRuby"
		"UberchargeFullTinyText5"	"ColorMagenta"
		"UberchargeFullTinyText6"	"ColorRuby"
		"UberchargeFullMeter1"		"ColorMagenta"
		"UberchargeFullMeter2"		"ColorRuby"
		"UberchargeFullMeter3"		"ColorMagenta"
		"UberchargeFullMeter4"		"ColorRuby"
		"UberchargeFullMeter5"		"ColorMagenta"
		"UberchargeFullMeter6"		"ColorRuby"
		"UberchargeFullText1"		"ColorMagenta"
		"UberchargeFullText2"		"ColorRuby"
		"UberchargeFullText3"		"ColorMagenta"
		"UberchargeFullText4"		"ColorRuby"
		"UberchargeFullText5"		"ColorMagenta"
		"UberchargeFullText6"		"ColorRuby"
```

If you want Transparent Tiny Ubercharge Text (see above), use the following overrides instead, replacing any other Tiny Text-related overrides:
```
		//Magenta Ubercharge with Transparent Tiny Text
		"UberchargeFullMeter1"		"ColorMagenta"
		"UberchargeFullMeter2"		"ColorRuby"
		"UberchargeFullMeter3"		"ColorMagenta"
		"UberchargeFullMeter4"		"ColorRuby"
		"UberchargeFullMeter5"		"ColorMagenta"
		"UberchargeFullMeter6"		"ColorRuby"
		"UberchargeFullText1"		"ColorMagenta"
		"UberchargeFullText2"		"ColorRuby"
		"UberchargeFullText3"		"ColorMagenta"
		"UberchargeFullText4"		"ColorRuby"
		"UberchargeFullText5"		"ColorMagenta"
		"UberchargeFullText6"		"ColorRuby"
		"UberchargeTextTinyTrans"			"UberYellowTrans"
		"UberchargeFullTinyText1Trans"	"ColorMagenta128"
		"UberchargeFullTinyText2Trans"	"ColorRuby128"
		"UberchargeFullTinyText3Trans"	"ColorMagenta128"
		"UberchargeFullTinyText4Trans"	"ColorRuby128"
		"UberchargeFullTinyText5Trans"	"ColorMagenta128"
		"UberchargeFullTinyText6Trans"	"ColorRuby128"
		"UberchargeTextTiny"			"NotVisible"
		"UberchargeTextTinyOutline"		"NotVisible"
		"UberchargeTextTinyShadow"		"NotVisible"
		"UberchargeFullTinyText1"	"NotVisible"
		"UberchargeFullTinyText2"	"NotVisible"
		"UberchargeFullTinyText3"	"NotVisible"
		"UberchargeFullTinyText4"	"NotVisible"
		"UberchargeFullTinyText5"	"NotVisible"
		"UberchargeFullTinyText6"	"NotVisible"
```

### Obnoxious Ubercharge ###
The obnoxious ubercharge combines the green and magenta effects for a seizure-inducing, ridiculously visible full uber effect. It can be enabled with the following overrides:
```
		//Obnoxious Ubercharge
		"UberchargeFullTinyText1"	"ColorMagenta"
		"UberchargeFullTinyText2"	"ColorGreen"
		"UberchargeFullTinyText3"	"ColorMagenta"
		"UberchargeFullTinyText4"	"ColorGreen"
		"UberchargeFullTinyText5"	"ColorMagenta"
		"UberchargeFullTinyText6"	"ColorGreen"
		"UberchargeFullMeter1"		"ColorGreen"
		"UberchargeFullMeter2"		"ColorMagenta"
		"UberchargeFullMeter3"		"ColorGreen"
		"UberchargeFullMeter4"		"ColorMagenta"
		"UberchargeFullMeter5"		"ColorGreen"
		"UberchargeFullMeter6"		"ColorMagenta"
		"UberchargeFullText1"		"ColorMagenta"
		"UberchargeFullText2"		"ColorGreen"
		"UberchargeFullText3"		"ColorMagenta"
		"UberchargeFullText4"		"ColorGreen"
		"UberchargeFullText5"		"ColorMagenta"
		"UberchargeFullText6"		"ColorGreen"
```

If you want Transparent Tiny Ubercharge Text (see above), use the following overrides instead, replacing any other Tiny Text-related overrides:
```
		//Obnoxious Ubercharge with Transparent Tiny Text
		"UberchargeFullMeter1"		"ColorGreen"
		"UberchargeFullMeter2"		"ColorMagenta"
		"UberchargeFullMeter3"		"ColorGreen"
		"UberchargeFullMeter4"		"ColorMagenta"
		"UberchargeFullMeter5"		"ColorGreen"
		"UberchargeFullMeter6"		"ColorMagenta"
		"UberchargeFullText1"		"ColorMagenta"
		"UberchargeFullText2"		"ColorGreen"
		"UberchargeFullText3"		"ColorMagenta"
		"UberchargeFullText4"		"ColorGreen"
		"UberchargeFullText5"		"ColorMagenta"
		"UberchargeFullText6"		"ColorGreen"
		"UberchargeTextTinyTrans"			"UberYellowTrans"
		"UberchargeFullTinyText1Trans"	"ColorMagenta128"
		"UberchargeFullTinyText2Trans"	"ColorGreen128"
		"UberchargeFullTinyText3Trans"	"ColorMagenta128"
		"UberchargeFullTinyText4Trans"	"ColorGreen128"
		"UberchargeFullTinyText5Trans"	"ColorMagenta128"
		"UberchargeFullTinyText6Trans"	"ColorGreen128"
		"UberchargeTextTiny"			"NotVisible"
		"UberchargeTextTinyOutline"		"NotVisible"
		"UberchargeTextTinyShadow"		"NotVisible"
		"UberchargeFullTinyText1"	"NotVisible"
		"UberchargeFullTinyText2"	"NotVisible"
		"UberchargeFullTinyText3"	"NotVisible"
		"UberchargeFullTinyText4"	"NotVisible"
		"UberchargeFullTinyText5"	"NotVisible"
		"UberchargeFullTinyText6"	"NotVisible"
```

### Rainbow Ubercharge ###
For the fabulous at heart, a rainbow ubercharge effect is provided. It can be enabled with the following overrides:
```
		//Rainbow Ubercharge
		"UberchargeFullTinyText1"	"ColorGreen"
		"UberchargeFullTinyText2"	"ColorCyan"
		"UberchargeFullTinyText3"	"ColorBlue"
		"UberchargeFullTinyText4"	"ColorMagenta"
		"UberchargeFullTinyText5"	"ColorRed"
		"UberchargeFullTinyText6"	"ColorYellow"
		"UberchargeFullMeter1"		"ColorGreen"
		"UberchargeFullMeter2"		"ColorCyan"
		"UberchargeFullMeter3"		"ColorBlue"
		"UberchargeFullMeter4"		"ColorMagenta"
		"UberchargeFullMeter5"		"ColorRed"
		"UberchargeFullMeter6"		"ColorYellow"
		"UberchargeFullText1"		"ColorGreen"
		"UberchargeFullText2"		"ColorCyan"
		"UberchargeFullText3"		"ColorBlue"
		"UberchargeFullText4"		"ColorMagenta"
		"UberchargeFullText5"		"ColorRed"
		"UberchargeFullText6"		"ColorYellow"
```
If you want Transparent Tiny Ubercharge Text (see above), use the following overrides instead, replacing any other Tiny Text-related overrides:
```
		//Rainbow Ubercharge with Transparent Tiny Text
		"UberchargeFullMeter1"		"ColorGreen"
		"UberchargeFullMeter2"		"ColorCyan"
		"UberchargeFullMeter3"		"ColorBlue"
		"UberchargeFullMeter4"		"ColorMagenta"
		"UberchargeFullMeter5"		"ColorRed"
		"UberchargeFullMeter6"		"ColorYellow"
		"UberchargeFullText1"		"ColorGreen"
		"UberchargeFullText2"		"ColorCyan"
		"UberchargeFullText3"		"ColorBlue"
		"UberchargeFullText4"		"ColorMagenta"
		"UberchargeFullText5"		"ColorRed"
		"UberchargeFullText6"		"ColorYellow"
		"UberchargeTextTinyTrans"			"UberYellowTrans"
		"UberchargeFullTinyText1Trans"	"ColorGreen128"
		"UberchargeFullTinyText2Trans"	"ColorCyan128"
		"UberchargeFullTinyText3Trans"	"ColorBlue128"
		"UberchargeFullTinyText4Trans"	"ColorMagenta128"
		"UberchargeFullTinyText5Trans"	"ColorRed128"
		"UberchargeFullTinyText6Trans"	"ColorYellow128"
		"UberchargeTextTiny"			"NotVisible"
		"UberchargeTextTinyOutline"		"NotVisible"
		"UberchargeTextTinyShadow"		"NotVisible"
		"UberchargeFullTinyText1"	"NotVisible"
		"UberchargeFullTinyText2"	"NotVisible"
		"UberchargeFullTinyText3"	"NotVisible"
		"UberchargeFullTinyText4"	"NotVisible"
		"UberchargeFullTinyText5"	"NotVisible"
		"UberchargeFullTinyText6"	"NotVisible"
```

## Ubercharge Percentage Placement ##
![![](http://img12.imageshack.us/img12/7518/gmanghudcapuberslolthum.png)](http://img837.imageshack.us/img837/4065/gmanghudcapuberslolfull.png)

If you're using a [Layout variant](http://code.google.com/p/gmang-tf2hud/wiki/Layouts), you'll probably want to reposition your Ubercharge percentage accordingly. This is done with Overrides _that must be placed **before** any Ubercharge Color overrides in your ClientScheme_ (that is, if you have other Ubercharge overrides, put them after any you use from this section).

### Povo Placement ###
This placement is for the Povo-inspired layout, putting the Ubercharge text just to the right of the objectives icons.

The actual override to use depends on which Ubercharge Color you're using. If you're sticking to the default green, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme):
```
		//Povo Ubercharge Text Placement
		"UberchargeFullTextPovo1"		"ColorGreen"
		"UberchargeFullTextPovo2"		"UberchargeFull"
		"UberchargeFullTextPovo3"		"ColorGreen"
		"UberchargeFullTextPovo4"		"UberchargeFull"
		"UberchargeFullTextPovo5"		"ColorGreen"
		"UberchargeFullTextPovo6"		"UberchargeFull"
		"UberchargeOutlinePovo"			"OutlineDefault"
		"UberchargeShadowPovo"			"ShadowDefault"
		"UberchargeTextPovo"			"UberYellow"
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```

For the Magenta Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme):
```
		//Povo Ubercharge Text with Magenta Ubercharge
		"UberchargeFullTextPovo1"		"ColorMagenta"
		"UberchargeFullTextPovo2"		"ColorRuby"
		"UberchargeFullTextPovo3"		"ColorMagenta"
		"UberchargeFullTextPovo4"		"ColorRuby"
		"UberchargeFullTextPovo5"		"ColorMagenta"
		"UberchargeFullTextPovo6"		"ColorRuby"
		"UberchargeOutlinePovo"			"OutlineDefault"
		"UberchargeShadowPovo"			"ShadowDefault"
		"UberchargeTextPovo"			"UberYellow"
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```

For the Obnoxious Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme)
```
		//Povo Ubercharge Text with Obnoxious Ubercharge
		"UberchargeFullTextPovo1"		"ColorMagenta"
		"UberchargeFullTextPovo2"		"ColorGreen"
		"UberchargeFullTextPovo3"		"ColorMagenta"
		"UberchargeFullTextPovo4"		"ColorGreen"
		"UberchargeFullTextPovo5"		"ColorMagenta"
		"UberchargeFullTextPovo6"		"ColorGreen"
		"UberchargeOutlinePovo"			"OutlineDefault"
		"UberchargeShadowPovo"			"ShadowDefault"
		"UberchargeTextPovo"			"UberYellow"
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```

For the Rainbow Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme)
```
		//Povo Ubercharge Text with Rainbow Ubercharge
		"UberchargeFullTextPovo1"		"ColorGreen"
		"UberchargeFullTextPovo2"		"ColorCyan"
		"UberchargeFullTextPovo3"		"ColorBlue"
		"UberchargeFullTextPovo4"		"ColorMagenta"
		"UberchargeFullTextPovo5"		"ColorRed"
		"UberchargeFullTextPovo6"		"ColorYellow"
		"UberchargeOutlinePovo"			"OutlineDefault"
		"UberchargeShadowPovo"			"ShadowDefault"
		"UberchargeTextPovo"			"UberYellow"
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```

### Valve Placement ###
This placement is for the Valve-inspired layout, putting the Ubercharge text at the bottom-right corner of the screen.

The actual override to use depends on which Ubercharge Color you're using. If you're sticking to the default green, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme):
```
		//Valve Ubercharge Text Placement
		"UberchargeFullTextValve1"		"ColorGreen"
		"UberchargeFullTextValve2"		"UberchargeFull"
		"UberchargeFullTextValve3"		"ColorGreen"
		"UberchargeFullTextValve4"		"UberchargeFull"
		"UberchargeFullTextValve5"		"ColorGreen"
		"UberchargeFullTextValve6"		"UberchargeFull"
		"UberchargeOutlineValve"			"OutlineDefault"
		"UberchargeShadowValve"			"ShadowDefault"
		"UberchargeTextValve"			"UberYellow"
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```

For the Magenta Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme):
```
		//Valve Ubercharge Text with Magenta Ubercharge
		"UberchargeFullTextValve1"		"ColorMagenta"
		"UberchargeFullTextValve2"		"ColorRuby"
		"UberchargeFullTextValve3"		"ColorMagenta"
		"UberchargeFullTextValve4"		"ColorRuby"
		"UberchargeFullTextValve5"		"ColorMagenta"
		"UberchargeFullTextValve6"		"ColorRuby"
		"UberchargeOutlineValve"			"OutlineDefault"
		"UberchargeShadowValve"			"ShadowDefault"
		"UberchargeTextValve"			"UberYellow"
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```

For the Obnoxious Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme)
```
		//Valve Ubercharge Text with Obnoxious Ubercharge
		"UberchargeFullTextValve1"		"ColorMagenta"
		"UberchargeFullTextValve2"		"ColorGreen"
		"UberchargeFullTextValve3"		"ColorMagenta"
		"UberchargeFullTextValve4"		"ColorGreen"
		"UberchargeFullTextValve5"		"ColorMagenta"
		"UberchargeFullTextValve6"		"ColorGreen"
		"UberchargeOutlineValve"			"OutlineDefault"
		"UberchargeShadowValve"			"ShadowDefault"
		"UberchargeTextValve"			"UberYellow"
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```

For the Rainbow Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme)
```
		//Valve Ubercharge Text with Rainbow Ubercharge
		"UberchargeFullTextValve1"		"ColorGreen"
		"UberchargeFullTextValve2"		"ColorCyan"
		"UberchargeFullTextValve3"		"ColorBlue"
		"UberchargeFullTextValve4"		"ColorMagenta"
		"UberchargeFullTextValve5"		"ColorRed"
		"UberchargeFullTextValve6"		"ColorYellow"
		"UberchargeOutlineValve"			"OutlineDefault"
		"UberchargeShadowValve"			"ShadowDefault"
		"UberchargeTextValve"			"UberYellow"
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```

### Obvious Placement ###
This placement can be used with any layout, simply providing the Ubercharge percentage to the right of your crosshair.

Before applying this placement, you may or may not want to remove the regular Ubercharge text and/or the Tiny Ubercharge text. The regular text can be removed with the following override:
```
		//Hide Default Ubercharge Text
		"UberchargeFullText1"		"NotVisible"
		"UberchargeFullText2"		"NotVisible"
		"UberchargeFullText3"		"NotVisible"
		"UberchargeFullText4"		"NotVisible"
		"UberchargeFullText5"		"NotVisible"
		"UberchargeFullText6"		"NotVisible"
		"UberchargeOutline"			"NotVisible"
		"UberchargeShadow"			"NotVisible"
		"UberchargeText"			"NotVisible"
```
The tiny text can be removed with this override:
```
		//Hide Tiny Ubercharge Text
		"UberchargeTextTiny"			"NotVisible"
		"UberchargeTextTinyOutline"		"NotVisible"
		"UberchargeTextTinyShadow"		"NotVisible"
		"UberchargeFullTinyText1"	"NotVisible"
		"UberchargeFullTinyText2"	"NotVisible"
		"UberchargeFullTinyText3"	"NotVisible"
		"UberchargeFullTinyText4"	"NotVisible"
		"UberchargeFullTinyText5"	"NotVisible"
		"UberchargeFullTinyText6"	"NotVisible"
```

Once you've removed the default Ubercharge percentage indicators, you can apply the Obvious placement. The actual override to use depends on which Ubercharge Color you're using. If you're sticking to the default green, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme):
```
		//Obvious Ubercharge Text Placement
		"UberchargeFullTextObvious1"		"ColorGreen"
		"UberchargeFullTextObvious2"		"UberchargeFull"
		"UberchargeFullTextObvious3"		"ColorGreen"
		"UberchargeFullTextObvious4"		"UberchargeFull"
		"UberchargeFullTextObvious5"		"ColorGreen"
		"UberchargeFullTextObvious6"		"UberchargeFull"
		"UberchargeOutlineObvious"			"OutlineDefault"
		"UberchargeShadowObvious"			"ShadowDefault"
		"UberchargeTextObvious"			"UberYellow"

```

For the Magenta Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme):
```
		//Obvious Ubercharge Text with Magenta Ubercharge
		"UberchargeFullTextObvious1"		"ColorMagenta"
		"UberchargeFullTextObvious2"		"ColorRuby"
		"UberchargeFullTextObvious3"		"ColorMagenta"
		"UberchargeFullTextObvious4"		"ColorRuby"
		"UberchargeFullTextObvious5"		"ColorMagenta"
		"UberchargeFullTextObvious6"		"ColorRuby"
		"UberchargeOutlineObvious"			"OutlineDefault"
		"UberchargeShadowObvious"			"ShadowDefault"
		"UberchargeTextObvious"			"UberYellow"
```

For the Obnoxious Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme)
```
		//Obvious Ubercharge Text with Obnoxious Ubercharge
		"UberchargeFullTextObvious1"		"ColorMagenta"
		"UberchargeFullTextObvious2"		"ColorGreen"
		"UberchargeFullTextObvious3"		"ColorMagenta"
		"UberchargeFullTextObvious4"		"ColorGreen"
		"UberchargeFullTextObvious5"		"ColorMagenta"
		"UberchargeFullTextObvious6"		"ColorGreen"
		"UberchargeOutlineObvious"			"OutlineDefault"
		"UberchargeShadowObvious"			"ShadowDefault"
		"UberchargeTextObvious"			"UberYellow"
```

For the Rainbow Ubercharge theme, use the following override (remember, place it **before** your other Ubercharge Color overrides in ClientScheme)
```
		//Obvious Ubercharge Text with Rainbow Ubercharge
		"UberchargeFullTextObvious1"		"ColorGreen"
		"UberchargeFullTextObvious2"		"ColorCyan"
		"UberchargeFullTextObvious3"		"ColorBlue"
		"UberchargeFullTextObvious4"		"ColorMagenta"
		"UberchargeFullTextObvious5"		"ColorRed"
		"UberchargeFullTextObvious6"		"ColorYellow"
		"UberchargeOutlineObvious"			"OutlineDefault"
		"UberchargeShadowObvious"			"ShadowDefault"
		"UberchargeTextObvious"			"UberYellow"
```