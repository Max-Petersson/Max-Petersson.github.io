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

