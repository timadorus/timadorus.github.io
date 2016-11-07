---
title: "Goals and Aims of the Project Timadorus"
permalink: general_goals.html
sidebar: home_sidebar
lang: en
---


Timadorus aims to provide tools, services and context for improving the technical
base for creating MMORPGs. In order to move towards this somewhat lofty goal, Timadorus
has set a number of tasks, some of which are quite challenging. Implementing will be
the target of a long string of small steps. The ultimate vision is a MMORPG plattform
supports the same richness of possible game forms as is provided by a [Pen and Paper](https://en.wikipedia.org/wiki/Tabletop_role-playing_game).

For Timadorus not only the final goal is of interest, but also the way to get there.
The project is used a teaching and research tool for developing software as an engineering
discipline. Details on how to achieve this are given [here][general_workflow]


## Software for a new type of MMORPG ##

Timadorus wants to become an interesting MMORPG; A new MMMORPG; an MMORPG that stands
apart from existing games, so it does not become a mere clone. It owes its academic
origins capabilities that where stated as impossible by some games industry insiders
at some point.

### Non-Stop ###

''For changes to the game there must be no interruption of service!''

Shutting down the service for two hours every wednesday morning is not acceptable.
Regardless of planed or unplaned downtime.

### No Simple Point of Failure ###

'' There must be no component whose failure will interrupt the service. Degredation must
be acceptable to vast majority of users and temporary to all''.


### Continuous ###

'' There shall be no interruptions to game use that may impact immersion. Also there may
be limit to interaction for technical reasons visible to users ''

This will disallow realms, shards, zones or similar that either segregate the user base
or place limits on the interactions between avatars. Of course there may be technical
reasons to partition the game. But these must be completely transparent to the users.


### Scalable ###

''No single component should limit the number of concurrent users of the system,
regardless whether they be human or technical.''

The target size for the system is
one million concurrent clients. Also the spatial size of the game world should not
be restricted.


### Manipulation Resistant ###

''Cheating should be so hard or be of such little benefit, that nobody can extract a
relevant gain. Cheating should be, if not impossible, at least be so difficult
that it is more worth while for participant to contribute to the community rather
than damaging it. And if unwanted manipulation can not be stopped, it should at least
be detectable.''

Vital for the discussion on this goal is the consideration what actually constitutes
cheating and what is a skill full manipulation of a game design. The base for further
thought on this is the philosophy that everything that is possible should be allowed
an anything that is not allowed should not be possible.

This requirement is vital to open the client of the game to 3rd party developers.
Most current MMO games need strict control over the client to ensure a modicum of
anti-cheat measures. Some also obfuscate or even properly encrypt the network
traffic between the client and the rest of the MMO to make manipulation
harder. But the current method of controlling cheating as shown itself to be a
dead end by resulting in a constant arms race between authors of manipulation
tools on one side and the game service providers trying to detect and stop
them on the other side.


### Future Proof ###


There are few areas of computer science that develop as fast a the quality of
computer generated images and 3D worlds. Decisions made today regarding acceptable
detail fidelity ensure rendering in real-time on todays hardware can seem out-dated just
months later.

This requires a creation and management of visual resources that is unlike todays
game industry practice of re-creating most assets for each product. Rather master models should
be of the hight degree of detail possible. Processes, methods and tools to automatically
down-grade assets for in-game use must be created and deployed. This processing must take
place with as little human intervention as possible. But it should support such intervention if needed or wanted.


## Base Requirements ##

Naturally, all requirements that are placed on a production grade MMORPG today have to be
fulfilled by the new one as well:


### Interactive ###

The game must react appropriately and quickly to input by the user. While there are many
techniques to hide server delay and thus allow for a great range of the actual server
latencies, the game should feel responsive.

### Persistent ###

Although the service should never stop, it must persist the complete world state through
clients disconnecting or the game server failing partially or even fully.

Data persistence could also offer later evaluation and analysis, e.g. for e-sports, research
analysis, etc.


### Snap-Shots ###

Even if the world is not stopped and restarted, it should be possible to create snapshots to
free a certain state for analysis and debugging. This could also be used to fork game worlds.

{% include links.html %}
