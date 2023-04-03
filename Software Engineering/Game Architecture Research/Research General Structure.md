Really what I am looking at is building a system with various hooks to plug minigames into. As such, Egert recommended looking at other such systems, like Consoles, Game Engines, Mods, or other minigame collection code, to build out that taxonomy of how different systems handle that problem.
## Problem Statement
We need a way to quickly prototype minigames. In a broader sense, we want to build a system that has interfaces to create new content and behaviors on top of, without having to repeat ourselves often. 
## Characteristics
Through these systems I will be looking at some characterstics, how they are built in and how they are used.
### Flexibility
One way you could do this is simply load in content, or you could have lots of hooks and communication back and forth. Somewhat precariously defined as number of hooks into the main system
### Extensibility 
You may need to add features that the core does not support. How is that handled?
### Maintainability
Coupling, does a change in a minigame effect the rest of the system? Should the system protect minigames from coupling within itself?

## What are we doing?
With all of that out of the way, how are we doing things, and why? How are the characteristics of our system defined. 