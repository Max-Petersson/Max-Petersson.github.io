---
title: State Machine
---

# State Machine

- **Developed:** 2023
- **Genre:** AI System

### Overview
This finite-state machine was buillt during my master thesis were my group tried to create a soulslike boss fight along with simpler enemies. 
It consists of a StateMachine component, the states were UObjects coded in C++. These were somewhat editable in blueprints with variables being exposed in order to cut down on compilation time as well as just makeing the easier to alter.
![](src/images/StateMachine/BP_Dodge.png)

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

Every moving plant had a bounds box that represented the area where it patrolled, contributing to more intereresting movement.
I also noticed that some of the dogs would try to evade a strike when they had been hit. So I made them subscribe to the event that fired when the attack began. And if they were damaged recently, they had a chance of going for an evade.

![](src/images/StateMachine/MovingPlantShow.gif)

### Additional information
This state machine also handled the damage that the plants would take, so the base damage would be sent to the current state, which would then in turn signal back with the amount of damage it should take. This way, it was easy to for example make it so that stunned plants take more damage!