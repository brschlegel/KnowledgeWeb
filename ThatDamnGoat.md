## Development

### GOAP
The Goat AI was architectured using GOAP. I think I picked this as the Goat is a very central piece of the game, and it felt wrong to have the entire AI just be a big random state machine. Looking back at it, I think this was a mistake, for several reasons
#### Square Peg, Round Hole
 Theoretically, the Goat is an agent of chaos, randomly choosing different actions for no apparent reason. In addition, the Goat is an all powerful being. If the Goat wants to do something, he can do it, regardless of the current state of the world. To begin with, the GOAP architecture is completely determinate ecosystem. This means randomness has to be introduced in another layer, such as when the goals are being chosen. While it isn't really talked about much when researching the architecture, GOAP really is all about restrictions. The benefits of GOAP really shine when you have a fairly contrained AI that must check off boxes in order to complete an action ie:
 1. Move to Gun
 2. Grab Gun
 3. Load Gun
 4. Aim At Enemy
 5. Fire
This is where the architecture shines because it allows you to skip tasks that don't need to be completed/are already done. The Goat does not really have many contraints. If he wants to do something, he will simply do it. He can run through walls, teleport wherever, fly, whatever he needs to do, and as such his action maps are relatively shallow.

## Design
