---
title: Idun
---

![This is a image!](src/images/PlanetSide.png "Image caption")

# IDUN

- **Developed:** 2021-2024
- **Company** Idun Interactive
- **Genre:** RTS, Tower Defense, Resource Management
- **Role:** Intern Programmer

### Overview
Idun Interactive is the company where I had my internship.

The gameplay consisted of going to a planet, killing a bunch of aliens while either protecting an objective or completing one.
My role was to implement the meta gameplay, what happened in between the quests. And so I created a Space Station!

The gameloop revolved around completing missions down on the planet, gathering resources from killing aliens. And then going to the Space Station in order to unlock new turrets or upgrade them. This was done by unlocking rooms, which in turn would unlock better materials used for more advanced Turrets.

![](src/images/SpaceStation.gif)

The rooms needed to be moveable and should have different functionalites and upgrades.
When on the planet side, the space station is visible and it is also a representation on how it looks on the inside, the game supported multiple profiles and the space station had to be able to recieve incoming save data and translate it into rooms and the update the visual representation of the space station. Shown below.

![](src/images/HotReload.gif)

I also created a crafting system, almost everything in the game can be used as materials for crafting, and the output of a recipe can also be almost anything.

The actual space station is a 2 dimensional array och Classes that persists between levels. Each instance has a Roomdata associated with it, dictating if the room is a storage, production, producer or merchant room. 

Special thanks to Gustav Hagerling, former VFX lead at dice and CEO of Idun interactive for giving me the opportunity to work with him!