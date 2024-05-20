---
title: GOAP
---

# GOAP

- **Developed:** 2023
- **Genre:** AI System

### Overview
GOAP stands for Goal Oriented Action Planning and is a way to design and define AI Behavior.
Unlike state machines. Where you have predefined transitions between states, a GOAP system will determine what actions to take in order to reach a goal.

This system was created during my master thesis. Were me and two others wanted to create a soulslike boss fight, minions and a npc.
The AI for the trader was very simple, if there is no player nearby his stand, he would simply idle. If a player was to come near his stand, he would run towards the stand and give the player potions, once the player no longer is near the stand he would go back to idling.

![](src/images/GOAP/GoapShow.gif)

The way this system works is that the Agent, (the trader in this case) has a list of action that it can perform, and a set of goals which it will try to fulfill based on its available actions. 

Different goals have different priorities.

When no player is near the stand. The goal of doint nothing has the highest priority, as soon as the player moves near the stand, the Goal of serving the customer shoots to the sky and the planner will figure out a plan on how to make this happen.

Here is the code behind the planning:
![](src/images/GOAP/Planner.png)
![](src/images/GOAP/BuildGraph.png)

The BuildGraph function gets recursively called until it no longer can build any nodes. Thereby resulting in a plan. 
The Actions have some fields exposed to the editor, in order to cut down on compilation time and for ease of altering.

A plan can look something like this:

![](src/images/GOAP/Goal.png)
Here we see a goal that is serve the customer. The wanted outcome of an action is "isServingCustomer" = true

![](src/images/GOAP/Action.png)

Here we can see the preconditions that need to be met in order for this to be an available action. And what effect that will come after this action has resolved.

![](src/images/GOAP/Action1.png)

Followed by

![](src/images/GOAP/Action2.png)

And the "customerWaiting" is a worldState which gets triggered when a customer is waiting.