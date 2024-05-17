---
title: Flesh And Stone
---

![This is a image!](src/images/FleshAndStone1.gif)

# Flesh And Stone

- **Developed:** 2023
- **Genre:** Hack n slash, Arena Fighter, 

### Overview
Flesh And Stone was an eight week, Unreal Engine 5 project that I worked on during my time at Yrgo.
The team consisted of four programmers and three artists. 
My responsibilities were:
- AI for ranged and melee Golems
- Boss fight
- Damage system

The AI for all of the enemies were created with behaviour trees and Blueprint nodes.

### Boss

![](src/images/FleshAndStone.gif)

The boss fight consisted of four phases. With each phase the boss's moveset changed, and the endlag of its moves was reduced.
Movesetwise, the combos the boss would perform depended on Line of sight and distance to the player. 

The conditions were

- If line of sight not clear.

- If the line of sight was clear but distance to player was far. 

- If the line of sight was clear and distance to player was near.

Each condition had its own combo or two that the boss could randomly pick. Couple that a poise meter and you have the boss fight!

![](src/images/BossBehaviourTree.png)

### Basic Golem
The basic golem AI was really simple, walk towards the player, when near enough, try to attack. 
I hade a much more advanced system for it, where the AI would take turns trying to attack the player based on who the player was currently battling, but this was simply not as fun as having thoughtless punching bags and so the group made a collective decision to dumb it down!

### Ranged Golem
This AI was created using only Blueprints, it would only channel its attack if it had a clear line of sight of the player. If it was hit during this channel, the channeling would cancel. This enemy was stationary so no movement logic was needed.

### Level Design
