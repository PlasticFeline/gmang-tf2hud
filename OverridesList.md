# Introduction #

**When using Overrides, it's very important that you frequently make backup copies of your ClientScheme file, as it's replaced frequently in updates (both HUD and TF2), and typos as small as forgetting a quotation mark can break your game interface entirely.**

For instructions on applying Overrides, see [Settings](http://code.google.com/p/gmang-tf2hud/wiki/Settings).

# Naming Conventions #
Descriptions for Preoverrides will be written on a per-request basis, as most of them can be understood by context and Conventions, which follow. For custom crosshair conventions, see [Crosshairs](http://code.google.com/p/gmang-tf2hud/wiki/Crosshairs).

## Keywords ##
  * `AmmoClip`: Ammo currently loaded in the weapon.
  * `AmmoReserve`: Ammo carried but not loaded.
  * `Bonk`: Scout's Bonk Energy Drink/Crit-A-Cola.
  * `Bow` or `BowCharge`: Huntsman.
  * `Building`: Engineer's buildings' status display.
  * `CH`: Custom crosshair. See [Crosshairs](http://code.google.com/p/gmang-tf2hud/wiki/Crosshairs).
  * `CTF`: Capture-the-flag game mode.
  * `DamageText`: Damage values/combattext.
  * `EngyMetal`: Engineer's metal count.
  * `Heads`: Eyelander heads.
  * `ItemEffectMeter`: Meter used for cloak, buff banner, jarate, sandman.
  * `Killboard`: The kill/domination/revenge/capture notifications board displayed to all players.
  * `Killer`: Freeze cam panel.
  * `Player`: Actual player (self/you).
  * `QS`: Loadout quickswitch panel.
  * `SB`: Scoreboard.
  * `SBMain`: Background area on the scoreboard.
  * `SpecHP`: Health meter shown when looking at team mates.
  * `Sticky`: Demoman's stickybomb.
  * `Team`: Team selection menu.
  * `TournySpec`: Panels shown when spectating a tournament game.
  * `TournySpecHP`: Health meter on `TournySpec`
  * `Ubercharge`: Medic uber/kritz meter and text.
  * `UberchargeFull`: Colors used at full uber/kritz.

## Preoverride Conventions ##
  * Progress/Charge Meters...
    * `Notch`: the slashes used to indicate progress/usage of bars that fill up and empty
      * `NotchF`: A notch that goes in front of the charge meter, usually somewhat transparent, and usually accompanied by a NotchB.
      * `NotchB`: A notch that goes behind the charge meter, usually not transparent, and usually accompanied by a NotchF.
    * `Void`: The area of color placed behind the actual meter, which becomes visible when the meter is emptied.
    * `Bar`: Lines/areas that outline the meter space itself.
  * Text...
    * `Outline`: Manual outlining of text created by copying the text field eight times behind the text, spacing them out one unit in each direction (NW N NE E SE S SW W), and making them dark.
    * `OutlineCorrect`: Optional extra outlining provided when outline spacing looks wrong.
    * `Shadow`: Shadow copy of a text field placed slightly southeast of original text. Usually not noticeable on manually outlined text unless placed out further than 1 unit.

## Definition Conventions ##
  * Color...
    * `ColorCOLOR` (such as `ColorRed`): A plain color, possibly referenced by numerous Preoverrides. All colors use full saturation/brightness where applicable, with no transparencies.
    * `ColorXXXCOLOR` (such as `Color064Red`): A plain color that's darker than usual, possibly referenced by numerous Preoverrides. The number describes the color value; for example, `Color064Green` would be `0 64 0 255`.
    * `ColorCOLORYYY` (such as `ColorRed128`): A plain color given transparency, possibly referenced by numerous Preoverrides. The number describes the opacity; for example, `ColorYellow128` would be `255 255 0 128`.
    * `ColorXXXCOLORYYY` (such as `Color032Grey128`): A darkened plain color with transparency, possibly referenced by numerous Preoverrides. The first number describes color value, the second number describes opacity; for example, `Color128Grey160` would be `128 128 128 160`.
  * `Default`: A unique color. The phrase "default" refers to the color I chose by default, not necessarily a Valve default.

# Override List #
Information about each override is written after slashes (`//`) on the same line.

## Common Overrides ##
```
//////////////// COMMON OVERRIDES //////////////////
// simple overrides that can be toggled
// remove forwardslash pairs before quotations to enable
	
	/// PERMANENT DOT CROSSHAIR ////////////////////
		"CHPermaDotBG"			"ColorBlack" //Color of permanent dot custom crosshair outline
		"CHPermaDotFG"			"ColorGreen" //Color of permanent dot custom crosshair center

	/// ACHIEVEMENT TRACKER TEXT CROSS CROSSHAIR ///
		"CHAchText"			"ColorGreen" //Color of achievement tracker text-based cross-shaped custom crosshair
				
	/// PERMANENT RING CROSSHAIR //////////////
		"CHPermaRing"			"ColorMagenta096" //Color of permanent ring custom crosshair inner ring
		"CHPermaRing2"			"ColorBlack096" //Color of permanent ring custom crosshair outline rings
				
	/// REDUCE UBERCHARGE TEXT OUTLINE AND SHADOW //
		"UberchargeShadow"		"NotVisible"
		"UberchargeOutline"		"NotVisible"
				
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

	/// ALTERNATE PLAYER HEALTH COLORS /////////////
		"PlayerHPColorSelf"				"ColorWhite"
		"PlayerHPColorSelfLow"			"ColorVermillion"

	/// YELLOW DAMAGE TEXT /////////////////////////
		"DamageTextHit"				"ColorYellow" //Color of damage values that appear above hits
		"DamageTextLast"			"ColorYellow" //Color of latest damage dealt written in HUD

	/// HIDE TARGE INDICATORS //////////////////////
		"TargeVoid"				"NotVisible"
		"TargeNotchF"				"NotVisible" //Notch for Targe minicrit
		"TargeNotchB"				"NotVisible" //Notch for Targe minicrit
		"TargeStickyNotchF"			"NotVisible" //Notch for Targe crit range
		"TargeStickyNotchB"			"NotVisible" //Notch for Targe crit range
		"StickyVoid"				"ProgressVoid" //Normally unnecessary due to persistence of TargeVoid

	/// INCREASE STICKY NOTCHES ////////////////////
		"StickyNotchExtraF"			"TargeNotchFDefault" //Extra notches
		"StickyNotchExtraB"			"TargeNotchBDefault" //Extra notches

	/// HIDE TEAM COLOR FROM PLAYER HP /////////////
		"PlayerHPGrey"				"HPGreyDefault" //Plain color that overlaps HP box edges

	/// HIDE PLAYER HP OUTLINE /////////////////////
		"PlayerHPOutline"			"NotVisible"

	/// CORRECTIVE OUTLINE SPACING /////////////////
		"PlayerHPOutlineCorrect"		"OutlineDefault"
		"AmmoClipOutlineCorrect"		"OutlineDefault"
		
	/// HIDE BONK ACTIVE NOTCHES ///////////////////
		"BonkActiveNotchL"			"NotVisible" //Long notches on active section of bonk meter
		"BonkActiveNotchS"			"NotVisible" //Short notches on active section of bonk meter

```

## PreOverrides ##
Using a program like Notepad++, you can search the entirety of your /ui/ folder to find instances of these Preoverrides. If after doing this and reading the full Override Conventions list, you are still confused, leave a comment and I'll add a description to the override.
```
/////////////// G-MANG HUD PRE-OVERRIDES ///////////////
// default theme choices on HUD
// for advanced users only
	
	"ProgressVoid"				"ProgressVoidDefault"
	
	"VersionText"				"ColorWhite032"
	
	"ClassNum"					"ColorWhite128"
	"FullTeamsText"				"ColorRed"
	"GameMenuTitle"				"ColorWhite200"
	"GameMenuDarkness"			"ColorBlack180"
	"HighlanderText"			"HighlanderTextDefault"
	"TeamBluePanel"				"TeamBluePanelDefault"
	"TeamBlueText"				"TeamBlueTextDefault"
	"TeamButton"				"ColorWhite"
	"TeamCount"					"ColorWhite"
	"TeamRandomPanel"			"TeamRandomPanelDefault"
	"TeamRandomText"			"TeamRandomTextDefault"
	"TeamRedPanel"				"TeamRedPanelDefault"
	"TeamRedText"				"TeamRedTextDefault"
	"TeamSpecPanel"				"TeamSpecPanelDefault"
	"TeamSpecText"				"TeamSpecTextDefault"
	
	"PlayerHPBar"				"ColorBlack"
	"PlayerHPColor"				"HealthGreen"
	"PlayerHPColorSelf"				"HealthGreen"
	"PlayerHPColorSelfHigh"			"HealthHigh"
	"PlayerHPColorSelfLow"			"HealthLow"
	"PlayerHPColorHigh"			"HealthHigh"
	"PlayerHPColorLow"			"HealthLow"
	"PlayerHPGrey"				"NotVisible"
	"PlayerHPOutline"			"OutlineDefault"
	"PlayerHPOutlineCorrect"	"NotVisible"
	"PlayerHPNotchF"			"ColorBlack128"
	"PlayerHPNotchB"			"ColorWhite192"
	"PlayerHPShadow"			"ShadowDefault"
	"PlayerHPVoid"				"HPVoidDefault"
	
	"AmmoClipColor"				"ColorWhite"
	"AmmoClipOutline"			"OutlineDefault"
	"AmmoClipOutlineCorrect"	"NotVisible"
	"AmmoClipShadow"			"ShadowDefault"
	"AmmoReserveColor"			"Color200Grey"
	"AmmoReserveShadow"			"ShadowDefault"
	
	"DamageTextHit"				"ColorMagenta"
	"DamageTextLast"			"ColorMagenta"
	"DamageTextLastOutline"		"OutlineDefault"
	"DamageTextLastShadow"		"ShadowDefault"
	
	"KillBoardBlack"			"KillBoardBlackDefault"
	"KillBoardBlue"				"KillBoardBlueDefault"
	"KillBoardRed"				"KillBoardRedDefault"
	"KillBoardSelfText"			"ColorWhite"
	"KillBoardWhite"			"KillBoardWhiteDefault"
	
	"SBBlueBG"					"SBBlueBGDefault"
	"SBBlueTeamName"			"SBBlueTeamNameDefault"
	"SBBlueTeamScore"			"HUDBlueTeamSolid"
	"SBDeaths"					"SBDeathsDefault"
	"SBInfoBG"					"ColorBlack096"
	"SBKDOutline"				"OutlineDefault"
	"SBKDShadow"				"ShadowDefault"
	"SBKDSymbol"				"TransparentBlack"
	"SBKills"					"ColorGreen"
	"SBMainBG"					"ColorBlack112"
	"SBMainBG2"					"ColorBlack112"
	"SBMainBG2MM"				"SBMainBG2MMDefault"
	"SBMainBGMM"				"SBMainBGMMDefault"
	"SBMap"						"SBMapDefault"
	"SBRedBG"					"SBRedBGDefault"
	"SBRedTeamName"				"SBRedTeamNameDefault"
	"SBRedTeamScore"			"HUDRedTeamSolid"
	"SBServerBG"				"ColorBlack064"
	"SBServerName"				"TanLight"
	"SBServerTime"				"ColorWhite"
	"SBSpectators"				"TanLight"
	"SBStats"					"ColorWhite128"
	"SBStatsBG"					"ColorBlack064"
	"SBTeamNameOutline"			"OutlineDefault"
	"SBTeamNameShadow"			"ShadowDefault"
	"SBTeamPlayerCount"			"ColorWhite"
	"SBTeamScoreOutline"		"OutlineDefault"
	"SBTeamScoreShadow"			"ShadowDefault"
	"SBVerticalLine"			"ColorBlack064"
	"SBWaiters"					"TanLight"
	
	"KillerHPColor"				"HealthGreen"
	"KillerHPExtraBar"			"ColorBlack096"
	"KillerHPGrey"				"HPGreyDefault"
	"KillerHPOutline"			"OutlineDefault"
	"KillerHPOutlineCorrect"	"NotVisible"
	"KillerHPShadow"			"ShadowDefault"
	"KillerHPVoid"				"HPVoidDefault"
	
	"QSClassText"				"ColorWhite128"
	"QSNegative"				"QSNegativeDefault"
	"QSSlotText"				"ColorWhite200"
	
	"TimerGain"					"ColorGreen"
	
	"CTFPlayingTo"				"TanLight"
	"CTFPlayingToPanel"			"CTFPlayingToBGDefault"
	"CTFScoreBlue"				"HUDBlueTeamSolid"
	"CTFScoreOutline"			"OutlineDefault"
	"CTFScoreRed"				"HUDRedTeamSolid"
	"CTFScoreShadow"			"ShadowDefault"
	
	"StopWatchDescription"		"Color210Grey128"
	"StopWatchPoints"			"ColorStopWatchTint"
	"StopWatchTime"				"ColorWhite"
	
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
	
	"ItemEffectMeterBar"		"ColorBlack"
	"ItemEffectMeterNotchB"		"ColorWhite"
	"ItemEffectMeterNotchBB"	"ColorBlack"
	"ItemEffectMeterNotchF"		"ColorBlack143"
	"ItemEffectMeterVoid"		"ProgressVoidDefault"
	
	"SpecTopBar"				"SpecTopBarDefault"
	
	"SpecHPColor"				"HealthGreen"
	"SpecHPExtraBar"			"ColorBlack096"
	"SpecHPGrey"				"HPGreyDefault"
	"SpecHPOutline"				"OutlineDefault"
	"SpecHPShadow"				"ShadowDefault"
	"SpecHPVoid"				"HPVoidDefault"
	
	"TournySpecClassBG"			"ColorBlack096"
	"TournySpecRespawn"			"TournySpecRespawnDefault"
	"TournySpecRespawnOutline"	"OutlineDefault"
	"TournySpecRespawnShadow"	"ShadowDefault"
	"TournySpecTopBar"			"TournySpecTopBarDefault"
	"TournySpecUberCharge"		"ColorYellow"
	"TournySpecUberOutline"		"OutlineDefault"
	"TournySpecUberShadow"		"ShadowDefault"
	
	"TournySpecHPColor"			"HealthGreen"
	"TournySpecHPExtraBar"		"ColorBlack096"
	"TournySpecHPGrey"			"HPGreyDefault"
	"TournySpecHPNM"			"TournySpecHPNMDefault"
	"TournySpecHPOutline"		"OutlineDefault"
	"TournySpecHPShadow"		"ShadowDefault"
	"TournySpecHPVoid"			"Color015Grey"
	
	"BonkActiveMid"				"Color200Green"
	"BonkActiveBot"				"Color064Green"
	"BonkActiveNotchL"			"ColorYellow128"
	"BonkActiveNotchS"			"ColorYellow"
	"BonkActiveTop"				"Color064Green"
	"BonkBlackness"				"ColorBlack"
	"BonkEffectThreshB"			"ColorRed"
	"BonkEffectThreshF"			"ColorRed128"
	"BonkInactiveBot"			"Color064Red"
	"BonkInactiveMid"			"ColorRed150"
	"BonkInactiveNotch"			"ColorBlack"
	"BonkInactiveTop"			"Color064Red"
	
	"StickyBar"					"ColorBlack"
	"StickyCount"				"ColorWhite"
	"StickyCountOutline"		"OutlineDefault"
	"StickyCountShadow"			"ShadowDefault"
	"StickyNone"				"Color200Grey128"
	"StickyNoneShadow"			"Color042Grey192"
	"StickyNotchB"				"StickyNotchBDefault"
	"StickyNotchExtraB"			"NotVisible"
	"StickyNotchExtraF"			"NotVisible"
	"StickyNotchF"				"StickyNotchFDefault"
	"StickyVoid"				"NotVisible"
	
	"HeadsColor"				"ColorYellow"
	"HeadsOutline"				"OutlineDefault"
	"HeadsShadow"				"ShadowDefault"
	
	"TargeBar"					"ColorBlack"
	"TargeNotchB"				"TargeNotchBDefault"
	"TargeNotchF"				"TargeNotchFDefault"
	"TargeStickyNotchB"			"StickyNotchBDefault"
	"TargeStickyNotchF"			"StickyNotchFDefault"
	"TargeStretchNotchB"		"ColorWhite"
	"TargeStretchNotchBB"		"ColorBlack"
	"TargeStretchNotchF"		"ColorBlack143"
	"TargeVoid"					"ProgressVoidDefault"
	
	"BuildingBar"				"ColorBlack"
	"BuildingBuildText"			"ColorRed"
	"BuildingBuiltPanel"		"ColorBlack080"
	"BuildingHPBG"				"ColorBlack192"
	"BuildingIconColor"			"ColorWhite"
	"BuildingIconLv1"			"BuildingIconLv1Default"
	"BuildingIconLv2"			"BuildingIconLv2Default"
	"BuildingIconLv3"			"BuildingIconLv3Default"
	"BuildingIconPanel"			"ColorBlack040"
	"BuildingNotBuilt"			"BuildingNotBuiltDefault"
	"BuildingNotchB"			"ColorWhite"
	"BuildingNotchBB"			"ColorBlack"
	"BuildingNotchF"			"ColorBlack143"
	"BuildingRecharge"			"ColorYellow"
	"BuildingVoid"				"ProgressVoidDefault"
	"BuildingUpgradeShadow"		"ShadowDefault"
	"SapperPanel"				"ColorBlack064"
	"UpgradeColor"				"MetalColor"
	"DispMetalColor"			"ColorYellow_192"
	"DispMetalShadow"			"ShadowDefault"
	"RocketsColor"				"ColorMagenta_192"
	"SGKillsColor"				"ColorRed_192"
	"SGShellsColor"				"ColorYellow_192"
	"TPColor"					"ColorGreen_192"
	
	"JusticeColor"				"ColorYellow"
	"JusticeOutline"			"OutlineDefault"
	"JusticeShadow"				"ShadowDefault"
	
	"MoveableBG"				"ColorBlack096"
	"MoveableIcon"				"ColorWhite"
	
	"EngyMetalCount"			"MetalColor"
	"EngyMetalGain"				"ColorGreen"
	"EngyMetalLoss"				"ColorRed"
	"EngyMetalOutline"			"OutlineDefault"
	"EngyMetalShadow"			"ShadowDefault"
	
	"BlutsaugerGain"			"ColorGreen"
	
	"UberchargeBar"				"ColorBlack"
	"UberchargeBarF"			"ColorBlack143"
	"UberchargeBarB"			"ColorWhite"
	"UberchargeFullMeter1"		"ColorGreen"
	"UberchargeFullMeter2"		"UberchargeFull"
	"UberchargeFullMeter3"		"ColorGreen"
	"UberchargeFullMeter4"		"UberchargeFull"
	"UberchargeFullMeter5"		"ColorGreen"
	"UberchargeFullMeter6"		"UberchargeFull"
	"UberchargeFullText1"		"ColorGreen"
	"UberchargeFullText2"		"UberchargeFull"
	"UberchargeFullText3"		"ColorGreen"
	"UberchargeFullText4"		"UberchargeFull"
	"UberchargeFullText5"		"ColorGreen"
	"UberchargeFullText6"		"UberchargeFull"
	"UberchargeFullTextObvious1"		"NotVisible"
	"UberchargeFullTextObvious2"		"NotVisible"
	"UberchargeFullTextObvious3"		"NotVisible"
	"UberchargeFullTextObvious4"		"NotVisible"
	"UberchargeFullTextObvious5"		"NotVisible"
	"UberchargeFullTextObvious6"		"NotVisible"
	"UberchargeFullTextPovo1"		"NotVisible"
	"UberchargeFullTextPovo2"		"NotVisible"
	"UberchargeFullTextPovo3"		"NotVisible"
	"UberchargeFullTextPovo4"		"NotVisible"
	"UberchargeFullTextPovo5"		"NotVisible"
	"UberchargeFullTextPovo6"		"NotVisible"
	"UberchargeFullTextValve1"		"NotVisible"
	"UberchargeFullTextValve2"		"NotVisible"
	"UberchargeFullTextValve3"		"NotVisible"
	"UberchargeFullTextValve4"		"NotVisible"
	"UberchargeFullTextValve5"		"NotVisible"
	"UberchargeFullTextValve6"		"NotVisible"
	"UberchargeNotchB"			"ColorWhite"
	"UberchargeNotchBB"			"ColorBlack"
	"UberchargeNotchF"			"ColorBlack143"
	"UberchargeOutline"			"OutlineDefault"
	"UberchargeOutlineObvious"			"NotVisible"
	"UberchargeOutlinePovo"			"NotVisible"
	"UberchargeOutlineValve"			"NotVisible"
	"UberchargeShadow"			"ShadowDefault"
	"UberchargeShadowObvious"			"NotVisible"
	"UberchargeShadowPovo"			"NotVisible"
	"UberchargeShadowValve"			"NotVisible"
	"UberchargeText"			"UberYellow"
	"UberchargeTextObvious"			"NotVisible"
	"UberchargeTextPovo"			"NotVisible"
	"UberchargeTextValve"			"NotVisible"
	"UberchargeTextTiny"		"UberYellow"
	"UberchargeTextTinyTrans"	"NotVisible"
	"UberchargeTextTinyOutline"	"OutlineDefault"
	"UberchargeTextTinyShadow"	"ShadowDefault"
	"UberchargeFullTinyText1"	"ColorGreen"
	"UberchargeFullTinyText1Trans"	"NotVisible"
	"UberchargeFullTinyText2"	"UberchargeFull"
	"UberchargeFullTinyText2Trans"	"NotVisible"
	"UberchargeFullTinyText3"	"ColorGreen"
	"UberchargeFullTinyText3Trans"	"NotVisible"
	"UberchargeFullTinyText4"	"UberchargeFull"
	"UberchargeFullTinyText4Trans"	"NotVisible"
	"UberchargeFullTinyText5"	"ColorGreen"
	"UberchargeFullTinyText5Trans"	"NotVisible"
	"UberchargeFullTinyText6"	"UberchargeFull"
	"UberchargeFullTinyText6Trans"	"NotVisible"
	"UberchargeVoid"			"ProgressVoidDefault"
	
	"BowCharge175Notch"			"BowCharge175NotchDefault"
	"BowCharge175Area"			"BowCharge175AreaDefault"
	"BowCharge200Notch"			"BowCharge200NotchDefault"
	"BowCharge200Area"			"BowCharge200AreaDefault"
	"BowCharge260Notch"			"BowCharge260NotchDefault"
	"BowCharge260Area"			"BowCharge260AreaDefault"
	"BowCharge300Notch"			"BowCharge300NotchDefault"
	"BowCharge300Area"			"BowCharge300AreaDefault"
	"BowCharge360Notch"			"BowCharge360NotchDefault"
	"BowCharge360Area"			"BowCharge360AreaDefault"
	"BowChargeBar"				"ColorBlack"
	"BowChargeVoid"				"ProgressVoidDefault"
	"BowNotchB"					"BowNotchBDefault"
	"BowNotchF"					"BowNotchFDefault"

```