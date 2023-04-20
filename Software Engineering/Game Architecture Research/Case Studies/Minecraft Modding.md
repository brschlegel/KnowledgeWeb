\[1\]: https://moddingtutorials.org/1.19.2/advanced-blocks
## Adding Custom Items
---
Many things need to be registered to let the game know they exist. You can either register it manually, or using a deferred register. The deferred register will automatically register the item at the right time, and is just a handy little abstraction.
### Adding Food
You can add food to the game using a "Food Builder", which allows you to set various food properties, including a MobEffect Instance. 
### FuelItem
Items that can be burned as fuel must override the getBurnTime function to tell the system how to accept it into a furnace
## Overriding based functionality
---
Much of the heavy lifting in a modpack has to do with adding a custom item or block, and handling interactions while that item / block is in your hand / world. 
## Events in Forge
---
Things that happen in the world, for example, breaking a block, trigger events through the Forge event bus. This event bus informs registered listeners about some kind of action or state. Mods can also create their own events and allow other mods to listen and respond to them 