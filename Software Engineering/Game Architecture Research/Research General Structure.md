Really what I am looking at is building a system with various hooks to plug minigames into. As such, Egert recommended looking at other such systems, like Consoles, Game Engines, Mods, or other minigame collection code, to build out that taxonomy of how different systems handle that problem.
## Problem Statement
We need a way to quickly prototype minigames. In a broader sense, we want to build a system that has interfaces to create new content and behaviors on top of, without having to repeat ourselves often. 
## Characteristics
Through these systems I will be looking at some characterstics, how they are built in and how they are used.
### Flexibility
You may need to add features that the core does not support. How is that handled?
### Modifiability
Coupling, does a change in a minigame effect the rest of the system? Should the system protect minigames from coupling within itself?
###  Usability
Above all, the architecture needs to be simple enough to be understood and worked with. This is the limiting factor of the extensibility and decoupling aspects of the architecture.

## What are we doing?
With all of that out of the way, how are we doing things, and why? How are the characteristics of our system defined. 
