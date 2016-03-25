# Introduction #
Patches can be found on the [Downloads](http://code.google.com/p/gmang-tf2hud/downloads/list) page.

## Beta Version ##
#### Beta 31 (2013 February 09) ####
  * Patched files in accordance with recent updates
  * Fixed HUD elements for MvM Heavy Rage Meter and Spy Sapper Meter
  * Added support for Vaccinator; it's not pretty, see FAQ: http://code.google.com/p/gmang-tf2hud/wiki/FAQ#What%27s_the_deal_with_the_Vaccinator_UI?

#### Beta 30 (2012 October 27) ####
  * Patched files in accordance with latest TF2 update.

#### Beta 29 (2012 August 20) ####
  * Gave proper HUD elements to all weapons.
  * Fixed main menu buttons having slightly different shades of white.
  * Fixed "Marked for Death" not appearing above health bar.
  * Updated Scout drink meter to be based on 8-second duration instead of 6.
  * Added MvM scoreboard to all existing scoreboards (no user work required).
  * Made a ton of other adjustments to accommodate MvM content.

#### Beta 28 (2012 May 3) ####
My HUD editing stuff is still on my old computer, so the panels for new weapons aren't in yet. Sorry about that.
  * Patched numerous files in accordance with latest update.

#### Beta 27 (2011 October 16) ####
Sorry about the response time. :S In the process of moving!
  * Patched numerous files in accordance with latest update.

#### Beta 26 (2011 July 07) ####
Still haven't had the chance to test the new weapons, but I haven't had any reports about them, so I hope they're working!
  * Patched ClientScheme in accordance with latest update.
  * Improved main menu (most notably, fixed those nasty button glitches for notifications).
  * Released source files for Closed Captions.

#### Beta 25 (2011 June 23) ####
Because I don't have the new items (and couldn't even equip them if I did due to the current Steam cloud unavailability), this patch will likely require a followup.
  * Patched files in accordance with Uber Update (including some main menu revision). New unlock HUD elements are likely to have problems, because I cannot test them at the moment.
  * Trying a new method for outlining crosshairs (currently just being used on the ring crosshair). If results are good, HUD crosshair and text outlines will get a big upgrade in the future.
  * Made a custom coach spectator screen.
  * Slightly adjusted tiny ubercharge text to stay outside of ring crosshair.
  * Fixed spacing mistake on the 36-12 scoreboard on minmode 0.

#### Beta 24c (2011 May 06) ####
If you plan on rendering and submitting replays, you'll wanna grab this corrected patch. Otherwise, you can just keep using 24b. Apologies for the hectic situation.
  * Corrected incompatibility with replay editing/rendering panel text.
  * Added optional main menu fileswap for those who want to have access to the Saxxy buttons and obnoxious applause sounds. ;)

#### Beta 24b (2011 May 06) ####
Sorry, I've been having massive computer problems these past few days, so this took longer to release than normal, and it isn't the big patch I've been working on.
  * Patched files in accordance with latest TF2 update.

#### Beta 24 (2011 April 14) ####
Full update required. Unable to do all normal tests due to steam non-connectivity, so a "version b" may be appearing tomorrow.
  * Patched files in accordance with latest TF2 update.
  * Added "Ring" and "Ring (plain)" custom crosshairs with accompanying Common Override.

#### Beta 23 (2011 March 10) ####
Pretty big update; screenshots pending.
  * Removed health notch effect (caused display problems for some users).
  * Added new scoreboard option, "slim".
  * Made changes to compact scoreboard.
  * Expanded the 32-player scoreboard into a 36-player one.
  * Added overrides for scoreboard visibility options (will add a wiki article about scoreboard options soon). (noid's idea)
  * Created new winpanels that fit between the damage value and crosshair.
  * Added a notice to main menu for when the HUD breaks or is outdated. (broesel's idea)
  * Changed various timer and objective panels to match the rest of the HUD.
  * Revised quickswitch panel to remove needless information and fit more weapons without scrolling.
  * Made stopwatch panel really bare-bones and centered.
  * Changed arena team composition panel to fit between damage value and crosshair.
  * Customized tournament setup panels to match rest of HUD.
  * Made the non-minmode spectator screen match the minmode version.
  * Added a fileswap for spectator tournament player panels to be placed on the upper-screen instead of lower.
  * Made kill notices smaller and less visible in minmode 0, and more visible in minmode 1. (noid's idea)
  * Made small spacing corrections to the payload and control point panels.
  * Repositioned demoman health and sticky indicators to avoid overlapping with control point icons.
  * Moved health gain animation to upper-center screen to avoid looking weird on different layouts.
  * Made small correction to HudPlayerHealth that caused improper spacing for notches on some resolutions.

#### Beta 22 (2011 February 04) ####
[FAQ](http://code.google.com/p/gmang-tf2hud/wiki/FAQ) is now up on the wiki. Hopefully it's helpful.
  * Fixed KOTH timers being hidden after the latest patch.
  * Changed sizing and spacing of control point icons.
  * Revised TargetID for improved visibility and cleanliness (old versions still available via File Swap).
  * Revised disguise panel for improved visibility, cleanliness, and screen space.
  * Changed targetID/spectator health boxes to make the "box tops" not visible when not being used.
  * Made the main menu background somewhat less dark.
  * Added flashing colors to player HP notches based on buff/hurt status.

#### Beta 21 (2011 February 03) ####
  * Patched files in accordance with latest TF2 update.
  * Fixed small spacing issue on CP labels.

#### Beta 20 (2011 January 21) ####
  * Fixed control point file oversight from latest patch.
  * Altered ClientScheme layout to make editing clearer and easier.
  * Added more alternate ubercharge places (Valve and Obvious).
  * Added fileswap (StatPanel\_BaseHIDDEN.res) that should hide "You did better than your previous best" notices (please let me know if it doesn't work).

#### Beta 19 (2011 January 19) ####
  * Made minor additions to hudlayout and clientscheme in accordance with update.
  * Adjusted main menu elements to avoid overlapping the main page buttons with the developer console panel.
  * Added fileswaps for main menu to correct poor spacing on some resolutions.
  * Added local idle button (alias CreateIdle "map\_background cp\_dustbowl").
  * Fixed some syntax mistakes (closing brackets were missing in some files).
  * Removed game.ico correction file from HUD contents (apparently Valve switched to the correct one at some point on their own, not sure when).

#### Beta 18b (2010 December 21) ####
If you got everything working, don't bother updating. If the crosshairs are confusing you, go ahead and patch.
  * Changed custom crosshairs to be disabled by default.
  * Minor tweaks to ClientScheme.
  * Added comment to hudlayout for people wanting to track achievements on Engineer.

#### Beta 18 (2010 December 20) ####
Wiki and screenshots are currently getting expanded and udpated.
  * Added options for ClosedCaptions, separating it into FULL (all captions), MEDIC (concise captioning for medics), and LITE (concise captioning for other classes). Added captions for Engineer picking up and dropping buildings. See [Closed Captions wiki page](http://code.google.com/p/gmang-tf2hud/wiki/ClosedCaptions).
  * Updated custom crosshairs significantly (though still a WIP feature), adding two text-based crosshairs and improving consistency. See [Crosshairs wiki page](http://code.google.com/p/gmang-tf2hud/wiki/Crosshairs).
  * Adjusted a variety of hud animations and added new full Ubercharge effect options (Magenta, Obnoxious, Rainbow); see [Medic Options wiki page](http://code.google.com/p/gmang-tf2hud/wiki/MedicOptions).
  * Improved Tiny Uber Text for smoother appearance, added semi-transparent option.
  * Fixed main page displaying usable item icons in the corner.
  * Altered sizing and spacing of some objectives panels.
  * Added Povo-inspired layout options for health and ammo with corresponding health, uber, and ctf panel options. RIP pvhud. :( See [Layouts wiki page](http://code.google.com/p/gmang-tf2hud/wiki/Layouts).
  * Added Valve-style layout for health and ammo (places them in corners). See [Layouts wiki page](http://code.google.com/p/gmang-tf2hud/wiki/Layouts).

#### Beta 17 (2010 November 1) ####
  * Added Achievement-Tracker crosshair (as well as minmode-based and permanent crosshairs); currently in experimental state with only three shapes (+, small +, dot); track an achievement to get the crosshair, find options in ClientScheme overrides, remove with file swap. (Thanks to noid for achievement tracker crosshair idea!)
  * Added scoreboard file swaps along with a new scoreboard type, COMPACT (minimalist 12p). Screenshot: [here](http://img51.imageshack.us/img51/3627/tf2hudcompscoreboardscr.jpg)
  * Adjusted crosshair ubercharge for better appearance; added transparent variant.
  * Updated content in ClientScheme to avoid possible issues with recent updates.
Big apologies to people waiting for the HUD update. Long story short, I accidentally patched my HUD copy before even checking to see if anything broke, and then assumed the update didn't break anything. Won't happen again. I recommend using the 32-COMP scoreboard and the "Ubercharge Under Crosshair" override.

#### Beta 16b (2010 October 20) ####
  * Fixed trade chat text not displaying due to missing new font in ClientScheme.

#### Beta 16 (2010 October 20) ####
  * Made edits to Tiny Ubercharge Text override (bigger font, changes colors like full-sized text).
  * Added version number to main menu.
  * Added instructions for keeping class icons visible permanently (Ctrl+F PERMACLASS in ClientScheme.res)
  * Updated ClientScheme.res in accordance with latest patch.

#### Beta 15 (2010 October 02) ####
  * Added milk effect to health in accordance with Polycount update.
  * Edited HudAnimations\_tf, hudlayout, ClientScheme, and MainMenuOverride in accordance with Polycount update.
  * Edited scoreboard formatting to properly place duel panel.
  * Adjusted health gain text positioning.

#### Beta 14b (2010 September 30) ####
  * Edited scoreboard formatting in accordance with Polycount update.

#### Beta 14 (2010 September 30) ####
  * Slightly changed ClientScheme in accordance with Polycount update.
  * Edited main menu in accordance with Polycount update.

#### Beta 13 (2010 September 11) ####
  * Revised most meters to be wider and spaced better vertically
  * Added a bunch of file swaps for meters
  * Changed default bonk meter to middle
  * Changed default quickswitch placement to east
  * Made timer subtext outlined
  * Trimmed some fat from ClientScheme

#### Beta 12 (2010 August 11) ####
  * Fixed issue with CTF winlimit display
  * Added file swap for quickswitch placement
  * Adjusted arena player count placement
  * Hid map team goal notification panel

#### Beta 11 (2010 July 16) ####
  * Tweaked normal payload icons so they don't overlap ubercharge/bonk meter
  * Added file swap for larger name text on TargetID
  * Added file swap for classic-style Bonk/CAC meter

#### Beta 10 (2010 July 09) ####
  * Fixed inconsistencies with Engineer update
  * Applied new icons to Engineer building panels and targetID
  * Added file swap for classic Medic ubercharge meter

#### Beta 09 (2010 June 19) ####
Might want to look at screenshots.
  * Closed captions implemented, see [ClosedCaptions](http://code.google.com/p/gmang-tf2hud/wiki/ClosedCaptions)
  * Added health value color changes based on overhealed/normal/hurt status
  * Revised Medic elements (pretty different, try it for a few days before raging at me)
  * Similarly revised Bonk/Crit-A-Cola element (but can't auto-stretch to full width while maintaining indicators)
  * Implemented system that makes class image visible while disguised but otherwise hidden, dropping support for class image file swap
  * Added file swap for cross version of player health, dropping support for close version of health and ammo
  * Added override for small uber percentage text near crosshair
  * Cut down on kill cam panel
  * Tweaked minmode 0 scoreboard and tournament panels to fit 32 players on more aspect ratios
  * Moved various objective elements to make room for new Bonk and Medic layout
  * Shrunk CTF elements
  * Made minor edits to ClientScheme listing ordering for the new [OverridesList](http://code.google.com/p/gmang-tf2hud/wiki/OverridesList) page

#### Beta 08 (2010 June 16) ####
  * Added new main menu (see Settings for function customization)
  * Added non-TFC game icon
  * Added full payload and payload race support with tweaked visuals.
  * Provided tournament spectator health cross file swap
  * Revised bonk/cola bar (yellow notches are 1s each and have clientscheme overrides)
  * Fixed KOTH panel highlight glitch
  * ~~Increased size of ubercharge text~~ (forgot to include, will be in next update)
  * Made consistency and optimization fixes

#### Beta 07 (2010 June 11) ####
  * Edited clientscheme to be compatible with latest update.
  * Made minor optimization/consistency changes.
  * Added custom quickswitch panel.

#### Beta 06 (2010 May 27) ####
  * Corrected issue with TF2 update.
  * Revised disguise panel for better placement and usability.
The original Beta 06 accidentally had the PlayerClass image visible by default instead of hidden. This was fixed (and was the only change) in 06b.

#### Beta 05 (2010 May 23) ####
Major, sweeping update; complete replacement of **/resource/** and **/scripts/** recommended.
  * Converted color setup to scheme properties and added overrides (see Settings).
  * Mitigated grey/color health bar option to an override instead of a swap (removed extra hudplayerhealth files).
  * Added Common overrides for some simple options.
  * Set class icon visibility to hidden by default.
  * Spaced health and ammo further out (can be set to old default with file swap).
  * Made other slight spacing adjustments.
  * Changed the method used for player health positioning (hopefully more resolution-neutral).
  * Cleaned out hires and lores lines.

#### Beta 04 (2010 May 20) ####
  * Added bleed icon from TF2 update. (Minor, hotfix update.)

#### Beta 03 (2010 May 20) ####
  * Added team color tint to health bar outline (can be disabled, see Settings).
  * Added option to hide class image (see Settings).
  * Adjusted spacing on class selection screen for better usability.

#### Beta 02 (2010 May 19) ####
  * Fixed very minor placement issue with disguise info panel.

#### Beta 01 (2010 May 18) ####
  * Initial public release.