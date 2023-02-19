# Entity Component Systems
Mainly following the principle of [[Composition vs Inheritance | Composition over Inheritance]], the architecture consists of Entities, Components, and Systems (obviously). Entities are like your gameobjects, and are assigned components based on their attributes. In order to change an entities attributes, you can add/remove components at run-time as well.

## Data driven approach
source: https://medium.com/@savas/nomad-game-engine-part-2-ecs-9132829188e5
Entities are simply an int id, and components are simply data containers. Each component has its own manager that handles the functionality using arrays of components. This is done so that in memory, things are stored contiguously, which is more effectient than the entities holding their own components.
