---
title: State Machine
---

![This is a image!](https://via.placeholder.com/1920x1080 "Image caption")

# State Machine

- **Developed:** 2023
- **Genre:** AI System

### Overview
This finite-state machine was buillt during my master thesis were my group tried to create a soulslike boss fight along with simpler enemies. 
It consists of a StateMachine component, the states were UObjects coded in C++.

The Enemies used the pawnsense component in order to sense the player, along with some additional features in order to determine if there was a line of sight to the player.

I created two enemies with this state machine.

### Stationary Plant
![](src/images/StateMachine/StateMachineStationary.png)

If a player got to close to the plant, it would wake up. If there was a line of sight to the player, it would then decide on wether to use a ranged attack or a melee attack. 

The hurt, dead and stunned state could be entered from any state.
![](src/images/StateMachine/StationaryPlantShow.gif)

### Moving Plant
![](src/images/StateMachine/StateMachineMovingPlant.png)
This plant was my attempt at recreating the notorius dog enemies in the actual souls games.
An annoying and fast enemy. 