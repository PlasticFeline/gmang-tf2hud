# Introduction #
Closed captions need to be enabled in your Team Fortress 2 settings (`closecaption "1"`). Currently, only English is supported. Once the captions are finalized (meaning, at the absolute latest, the HUD coming out of beta), the source will be released with the HUD (requires Source SDK to export).

# Versions #

There are three varieties of closed captions provided.

## Full ##

The default caption variant is **FULL**, which contains all caption messages listed in the Messages section below.

## Medic ##
The **MEDIC** caption variant is a concise set of caption messages designed for competitive Medics. The messages included are:
  * **All Non-Medic Classes:** ♥ HEALED ♥, Ξ READY Ξ
  * **Medic:** “ COVER ”, % CHARGED %, Ω ÜBER Ω
  * **Sniper:** ¡ JARATE ¡

## Lite ##
The **LITE** caption variant is a concise set of caption messages designed for competitive players of all classes other than Medic. These messages are:
  * **Scout:** ≈ DRINK USED ≈, ~ DODGE ~, = TIRED =
  * **Heavy:** ○ EATING ○, ☺ EATEN ☺
  * **Engineer:** § SAPPED TELE §, § SAPPED DISPR §, § SAPPED SENTRY §, £ SENTRY £
  * **Medic:** “ COVER ”, % CHARGED %, Ω ÜBER Ω, ☼ BURNING ☼, × HIT ×
  * **Sniper:** ¡ JARATE ¡

# Colors #
Color-coding is used to indicate source of sound (generally representing a class). The following is the color key:

![http://img404.imageshack.us/img404/6039/tf2hudclasscolors.png](http://img404.imageshack.us/img404/6039/tf2hudclasscolors.png)

# Messages #
To reduce space and time usage, the HUD uses symbols and short keyphrases to convey sound meanings. The messages used are...

General:
  * ☼ BURNING ☼ : Class is on fire, IE "Fire, fire!"
  * ♫ CALLING ♫ : Class calling for medic heals, IE "Medic!"
  * ♥ HEALED ♥ : Class recently healed, IE "Thanks, Medic!"
  * Ξ READY Ξ : Class requesting that a medic pop uber, IE "Activate Ubercharge!"
  * « TELEPORTED « : Class recently exited a teleporter, IE "Thanks for the teleporter!"

Medic Only:
  * “ COVER ” : Medic making a vocalization (possible Uber cover)
  * **% CHARGED %** : Medic declaring full charge, IE "I am fully charged!"
  * **Ω ÜBER Ω** : Uber/Kritz popped
  * × HIT × : Medic taking damage

Scout Only:
  * **≈ DRINK USED ≈** : Scout recently drank Bonk or Cola (usually comes out mid-effect)
  * ~ DODGE ~ : Scout currently/recently avoided damage while under Bonk effect
  * **= TIRED =** : Bonk/Cola effect recently expired
  * ♂ SANDMAN ♂ : Sandman user in the area

Soldier Only:
  * ♯ BUGLE ♯ : Soldier _might have_ recently used Buff Banner

Heavy Only:
  * **○ EATING ○** : Heavy has started eating Sandvich or Chocolate
  * ☺ EATEN ☺ : Heavy recently finished eating Sandvich or Chocolate

Engineer Only:
  * ¥ DISPENSER ¥ : Dispenser placed
  * £ SENTRY £ : Sentry gun placed
  * ¢ TELEPORTER ¢ : Teleporter recently placed
  * **§ SAPPED TELE §** : Teleporter being sapped
  * **§ SAPPED DISPR §** : Dispenser being sapped
  * **§ SAPPED SENTRY §** : Sentry gun being sapped
  * **▼ DISPR DOWN ▼** : Dispenser down
  * **▼ SENTRY DOWN ▼** : Sentry gun down
  * **▼ TELE DOWN ▼** : Teleporter down
  * <sup> MOVING </sup> : Packing up and relocating building.
  * v MOVED v : Carried building re-planted.

Sniper Only:
  * ¡ JARATE ¡ : Jarate thrown

Spy Only:
  * ¡ PISSED ¡ : Spy hit by Jarate