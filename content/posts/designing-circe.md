---
title: "Designing Circe"
date: 2020-08-30T14:16:29+02:00
draft: true
author: 'cypherfox'
slug: designing-circe
tags: [Game Design]
---

## A bit of history

I started pen-and-paper (PnP) roleplaying games with the 1983 revision of D&D basic set (aka [the red
box](https://en.wikipedia.org/wiki/Dungeons_%26_Dragons_Basic_Set#1983_revision)) when I was 14 years old. I got
permanently infected by the magic and sense of empowerment and agency this form of entertainment would grant me. I have
never stopped playing.  

But from the very beginning, I chaffed at the numerous small inconsistencies (e.g. why does a longsword does more damage
than any other one-handed weapon? Wwhere can I see an orginal medieval [studded leather
armor](https://forgottenrealms.fandom.com/wiki/Studded_leather)? Answer: nowhere. It never existed. The only thing that
looks like it is actually a form of armor more closely resembling [banded
mail](https://forgottenrealms.fandom.com/wiki/Banded_mail), but with a fabric covering, called a
[brigandine](https://en.wikipedia.org/wiki/Brigandine)).

The years since then, I have played numerous other PnP games, and have been [LARPing]() for close to 20 years. At some
point took an active interest in HEMA. Especially after seeing a [demonstration
video](https://www.youtube.com/watch?v=ohmLaZHStmI) by the Gladiatores and watching videos by many HEMA practitioners
like Mike Loades ([Down from horseback in armour](https://www.youtube.com/watch?v=WMuNXWFPewg)) and [Matt Easton]() of
Scholagladiatora. In particular the video on [Which sort is the best sword in a
one-on-one duel](https://www.youtube.com/watch?v=9qJBGlChcXU). Answer: it depends. 

At some point I decided to design a new combat system for PnP roleplaying games from the ground up. The result of this
work is the Computer Implementable Realistic Combat Environment (CIRCE). CIRCE is influenced by some concepts of the
attack and critical resolution tables of 2nd edition / classic [RoleMaster](https://en.wikipedia.org/wiki/Rolemaster),
but acnowledges the fact that there are too many tables and calculation to be handled in RM2 and thus CIRCE is
intetended to be used with software aid from the outset.

## Aims of CIRCE

From the sources above, I can state a number of goals for CIRCE 

* **Forget Hollywood.** In an PnP it does not have to have look good on screen. The expensive star actor does not have ot be
  visible. It need not be save for extras. It has to feel right.
* **Design a combat system, not a fencing system.** The latter is much to detailed for most players as it requires each
  individual strike, lunge and riposte to be called out individually. I have seen a product in the early 1990s that did
  this and made the difference very obvious. Unfortunately I do not rember its name.
* **Minimize dice rolls for resolution.** Instead of numerous dice rolls to resolve actually hitting the target,
  determining the amount of damage and potentially specific damages, there should only be minimal number, ideally a
  single roll that allows resolution. Have you ever felt betrayed when that natural 20 on the attack roll only returned
  3 points of damage, since you futzed the damage roll?
* **Appropriate damage location.** If only the small finger of the target peeks out behind an inpenetrable wall, it should not be
  possible to inflict mortal damage due to massive bleeding of internal organs.
* **Corectly handle armor damage**. Depending on the weapon, an attack may either circumvent the armor or overcome it's
  protection, damaging it in the process. Thus the damage an armor takes while protecting the wearer should depend on
  the weapon.

Non-goals are also vital to the form of the design:

* **Resolving attacks must be possible by starting players unaided.** As the "computer implementable" part of the name
  implies, CIRCE is planed to be implemented as computer programm from the very beginning. I assume that all players
  have a computer or tablet when playing the game, each connected to the internet (or to each other in a pinch). Thus
  the attack resolution can be done by the computers and be displayed in a compelling way. The dice rolls should be done
  by the players, as this is an integral part of the PnP experience. But the GM can let computer resolve the attacks,
  expecially when dealing with four times 66 Barbarians.


The result of combat is dependent on the particular combination of
1. Armor of the participants (it influences attack *and* defense)
1. The weapon used by the participants
1. The skill of attack and defense of the participants.

The combination of all these factors will provide a consisten result, as there is no such thing as a best weapon, but
only the right weapon, used by skilled hands against an opponent armed and armored in a particular way..


## Attack Resolution



## Forms of Damage
