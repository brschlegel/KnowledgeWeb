## 3 Case Study Q's
---
### What do we know?
- Stricter/better definition of coupling
- Ways of breaking objects into modules?
### How should that inform what we do/did?
- How we architecture our code
- How we write new code
- How we determine what must be rewritten
### What can we see from what we did?
- Measure with better definition of coupling
- Literally count the number of modules unique to a specific minigame
## What's my goal?
---
Every minigame created should add a new set of tools for us to use in other minigames.
## Reduce code unique to each minigame
Doing this in a scientific way would require me to define "code" and "unique" in a rigerous and useful way.
## Things to keep in mind
- How are we breaking things down into reusable modules? 
- Make sure your incentives are in line; You could end up stretching modules to do things they shouldn't for the sake of keeping module count low.
### Process to build new minigame
1. Break down minigame into required modules
2. Create the coupling diagrams for the minigame, attempting to get as many independent modules as possible
3. Code the minigame?
