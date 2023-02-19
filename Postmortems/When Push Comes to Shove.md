When Push Comes to Shove was my capstone game for my masters degree. I worked on it in a team of 5, where my role was of Programming, Software Architecture, and Design. I would also consider myself somewhat the "Creative Director" of the project, but I'm not sure if thats too arrogant. It is a local party game where you participate in shoving-themed minigames with stackable modifiers in between each round. I won't go into too much detail on the game itself as there is a huge document on it [here](https://docs.google.com/document/d/1T1UUe_1ra_th-stkinPUv0h6BBni8eblnn6tyE_Sy4s/edit)
## Development
--- 
### Animations
Concentration Queso
### Shoving/Physics
Fill out shovign
#### Hitboxes and Hurtboxes
The hitbox and hurtbox system worked incredibly well. I actually made it over the summer before capstone started, and it remained nearly unchanged throughout the entire project. It was easy to granuarly customize a specific hitbox to ignore others and add custom behavior. Centralizing everything made it so much easier to debug and follow, especially when compared to simple OnTriggerEnter only calls. Hit Handlers, and in particular the Hit Event Splitter were incredibly useful. Single point of entry, but multiple outputs, so instead of an entities response to a hit being defined by a script, it was defined by a unique collection of scripts. This was a huge boon to reusablilty, and since the Hit Event Splitter was also a hit handler, you could ignore tags hits entirely, or just ignore specific functionality, like taking damage or knockback. The system was the result of a lot of thinking and reflecting on how Unity operates, composition can be used to define behavior, and software in general. I wrote up a script for the technical award using this system [here.](https://docs.google.com/document/d/1ur-4wAHNQL5JP4mOEB-7zELTHarsVdWFWnMoeik35Pg/edit?usp=sharing)
### Minigames
fill out minigames
### Modifiers
## Design 
---
## Player on Player Interactions
Shoving people is fun 
### Minigames
we have minigames
#### Too Many Ball Minigames?
no
### Modifiers
## Pivot
---
there was a bigass pivot
## Team Dynamic
--- 
it was great

