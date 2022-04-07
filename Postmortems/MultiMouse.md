# MultiMouse
MultiMouse started as a project for a research studio that morphed into a personal project. It is a collection of minigames made with tech that allows multiple mice render as their own cursors. The minigames are built on top of a custom C++ framework that allows for quick and simple minigame production.
## Development
Everything was relatively ground-up for this project, using Box2D and OpenGL primarily, and served as a way to transition from very simple C++ to being somewhat comfortable in the language.
### Custom Framework
I really enjoyed doing some of the backend work on this project, setting up the engine framework was very rewarding. Looking back on it after some of the engines class, definitely didn't pay enough attention towards where I was allocating memory, most everything was thrown on the heap. That being said, its a 2D game that uses OpenGL primitives to render everything, so performance wasn't anything near a concern. In terms of minigame development however, the turn around is very quick. 
#### Props
I had been kicking around an idea about making minigames quickly through a "prop" system for a while, and tried somewhat unsuccessfully with Pandemonium. The idea is that many minigames can be built using reusable and general props, stitched together with some minimal scripting. An example is a Goal, that consumes a box and increments an internal counter. By adding scripting hooks to the goal's score, a few lines of code could add lots of functionality. MultiMouse was designed around this principle, with what I think was great success.
