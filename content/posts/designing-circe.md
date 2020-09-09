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
Scholagladiatora. More recently some scientify studies by French and Swiss grops, e.g. by [Jean
Jaque](https://www.youtube.com/watch?v=pAzI1UvlQqw). In particular the video on [Which sort is the best sword in a 
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
  especially when managing the attack of four times 66 Barbarians.


The result of combat is dependent on the particular combination of
1. Armor of the participants (it influences attack *and* defense)
1. The weapon used by the participants
1. The skill of attack and defense of the participants.

The combination of all these factors will provide a consistent result, as there is no such thing as a best weapon, but
only the right weapon, used by skilled hands against an opponent armed and armored in a particular way..

## Templates to support

The efficiency of fighting equipment, -trainign and military tactics is largely a function of the opponent the are most likely to face.
In order to get a better overview which fighting styles to support I have drawn up a list fighters througout the ages
and the opponnents they where likely facing.

### Athenian Hopplite, ca 350 B.C.E.

Weapons: Long Spear (2.5m - 3.0m), Bronze single edge sword

Armor: Linothorax, large round shield, bronze greaves, bronze helm.

Particulars of fighting style: very close packed formation (Phalanx) for mutual support. Shield wall neigh impregnable
to weapons of area. Pushing of army formations a viable combat tactic. Individula soldiers have a largely reduced combat
effectiveness, but still great reach with spear. Groups allow largely passive use of shield, in single combat it needs
to be used actively.

Combat Range: 2.0m

### Roman Legionaire, ca. 100 C.E.

Weapons: Thrusting short sword, heavy javelin

Armor: Lorica Segmentata, large rectengular shield, single bowl helmet with reinforcements and a nape guard.

Particulars of fighting style: rapid thrusts with Gladius, only passive defense through shield, armor + helmet and next
legionaire in the battle line.

Combat Range: 0.5 m

### 15th century civilian duelist

Weapons: Longsword

Particulars of fighting style: all defense through sword use, half-swording for close quarters work.

Combat Range: 2.5 m

### 16th century civilian duelist

Weapons: Thrustng Sword, off-hand dagger

Armor: buckler

Combat Range: 2.5 m

## Handling Initiative, Speed and multiple Attacks

Many roleplaying systems have a concept called Initiative that isolate the actions of the characters one after
another. The character with the higher initiative gets to complete their action fully before the next character can
begin to act. There are variations on this, where the character with the higher initiative gets to *declare* last,
thus allowing them to react to what the slower is planing, but finally all actions are completed before the next one beginns.

While this is very usefull to enable humans players to manage the pandemonium of battle and greatly aid the game master
in keeping track of the all the events taking place, it is not very realistic.

Thus I would propose a different approach that resembles the concurrent reality of combat a lot better.

1. Characters are either active of passive participants. A character can declare to be passive participant at any
time. From now on any passive actions or reactions of the character will take place unless declared otherwise
(e.g. using a shield or evading when being attacked). Usually this is visible to observers by a defensive posture,
drawing a weapon or unlimbering a shield from a travel position. A character must be aware of the potential combat
taking place and declare their intention before the combat starts or be subject to a reaction roll (see below).
1. In compat time is measured by the Combat Time Counter (CTC), a monotonic counter, starting at 0. It starts when the
first character declares the intention to enter active combat (or the GM determines this for any of the NPCs). 
1. Any action of the combatants may trigger a reaction by any other characters (e.g. reacting to being hit). If they
where previously unaware of the combat (e.g. by being ambushed), they first must make a successfull perception check.
If they have taken damage, the perception check succeeds automatically. Then they must make a Reaction Roll (RR) to
determine how fast they can enter combat. Only the when the reaction number of ticks has elapsed can they become a
passive or active participant. Until then they do not benefit from passive actions or reactions.

* while being either passive or active participant in combat, no exclusive actions (e.g. studying) can be performed.

Reaction Roll (RR): determins the number of combat ticks that 

## Armor


## Attack Resolution

Resolution takes these steps:

1. Add percentile roll ( d% ) to skill bonus in using the particular weapon. Add any circumstancial bonuses for the
attacker. Subtract any circumstancial bonuses for the defender. See table 1 for a partial list of bonuses.
1. Does the weapong connect with intended target? If not determine alternate target (other body parts, innocent
bystanders). If yes determine armor penetration.
1. Any armor (if any) will transform any attack. This may change the attack type (


## Forms of Damage

* blunt trauma
* piercing
* slashing
* elemental (fire, heat / cold, acid, etc. etc.)


## Special considerations

### Imunities, Resistances, Weaknesses

These are simply modelled as a further "virtual armor" layer beneath any other armor and transform the incoming attack
according to their function.

# Tables

## Table 1: circumstancial bonuses

* sight impairment
* combatant is bound or restricted, either by being grappled before or due to insufficient room to manouever.
* footing insufficient, slippery surface, combat while balancing on small ledge, etc.
* combatant is wounded or in serious pain or temporarily weakened.
* magic
