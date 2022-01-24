# Procedural Generation Notes
source 1: https://umm-csci.github.io/senior-seminar/seminars/spring2017/stangl.pdf


## Map Generation 
source: https://www.youtube.com/watch?v=TlLIOgWYVpI&t=467s&ab_channel=RoguelikeCelebration
-   Simple Room-Placement
	- Pick a random rectangle, if there already isnt a room there, make one. Keep picking rooms, and then connect them with corridors
-   BSP Rooms
	- Binary space partition, divide the map in half, randomly choose if you want to divide vertically or horizontally, and keep going until you get the size of room you want. Then repeat. Similiar results to SRP, but better spaced out.
 -   Cellular Automata
	- Make a random map. Apply cell life rules to each tile, and repeat
-  Drunken Walk
	- Put a drunkard in a map full of walls. He smashes through walls ie: anywhere he walks is open space. Place another drunkard wherever in the open space. Bonus is that the map is completely contiguous
-  Diffusion LImited Aggregation 
	- Start with seed space, and then randomly fire particles from random spots on the map. If you hit an edge of the open space, then open the closed space connected to that edge. Leads to a winding pattern, lots of small cooridors. Completely contiguous.
	-  Central Attractor
		- Always shoot at the center of the map, leading to a much more open space in the middle
	-  Erosion
		- Take another map and shoot particles at it, giving it a more organic looking structure
-  Voronoi Diagrams
	- Place the seeds around the map, and then each space joins its closest seed. You can change your distance heuristic for different effects
-  Dijsktra Maps
	- Choose a starting point, and then flood fill every walkable point, marking the iteration step that the tile was reached. Can be use to remove unreachable areas

## Noise
source 2: https://rtouti.github.io/graphics/perlin-noise-algorithm

### Perlin Noise
Smooth moving values from -1,1. Completely continuous as well.

### Layering Noise
