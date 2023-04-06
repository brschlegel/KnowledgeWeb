--- 
\[1\]: https://docs.unrealengine.com/5.0/en-US/gameplay-framework-in-unreal-engine/
The gameplay framework is Unreal's structure for building out core systems. You can build ontop of their objects, and alot of the connections will have already been made for you.
## Overview of the Structure
---
### Players and Enemies
Characters in the game, whether player controlled or AI controlled are represented by a Pawn, and an attached Controller. The pawn is the physical representation of the character, while the controller is responsible for directing a pawn. The controller is moderated coupled with the pawn, but the pawn as defined by the framework is not neccassarily coupled to the controller. It is mentioned that a pawn is completely capable of accepting input and handling its own logic. Worth noting that the seperation of pawn and controller makes things so much easier in systems where the AI and the Player control the same type of characters. In a system without that, its a strange abstraction, if not totally unwarrented.
## Game Modes and State
Game modes define the rules through which the game is played. Examples are how many players present, how pausing works , transitioning between levels, etc. Information about rule-related events, such as players joining, how long the game has been running, etc, is stored on the Game State.
#### AGameMode and AGameModeBase
AGameModeBase is the base class of all Game Modes, and contains overridable base functionality regarding multiplayer features like joining, as well as initialization. AGameMode has even more functionality for multiplayer matches, including a full state-machine to track gameplay flow, like Entering Map, In Progress, etc. 
#### Creating Derived Blueprints
Game mode blueprints can set defaults on default pawn, controller, playerstate, and other gameplay framework classes. This gives a powerful foundation to build your game on top of, utilizing all the connections already laid out for you.

