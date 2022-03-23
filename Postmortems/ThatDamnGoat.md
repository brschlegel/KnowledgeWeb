# That Damn Goat
ThatDamnGoat is a party game I did AI and Systems Programming for, developed at Magic Spell Studios. Faculty leads, with student workers. It was good experience, and I learned a lot from my time here, but I have completely detached from the design of this game. 
## Development

### GOAP
The Goat AI was architectured using [[GOAP]]. I think I picked this as the Goat is a very central piece of the game, and it felt wrong to have the entire AI just be a big random state machine. I also wanted to introduce more intelligence to the goat by feeding the Goat goals and having him figure it out from there. Developmentally, its more interesting, but in terms of actual gameplay it doesn't seem too different to me. Looking back at it, I think this was a mistake, for several reasons
#### Square Peg, Round Hole
 Theoretically, the Goat is an agent of chaos, randomly choosing different actions for no apparent reason. In addition, the Goat is an all powerful being. If the Goat wants to do something, he can do it, regardless of the current state of the world. To begin with, the GOAP architecture is completely determinate ecosystem. This means randomness has to be introduced in another layer, such as when the goals are being chosen. While it isn't really talked about much when researching the architecture, GOAP really is all about restrictions. The benefits of GOAP really shine when you have a fairly contrained AI that must check off boxes in order to complete an action ie:
 1. Move to Gun
 2. Grab Gun
 3. Load Gun
 4. Aim At Enemy
 5. Fire
This is where the architecture shines because it allows you to skip tasks that don't need to be completed/are already done. The Goat does not really have many contraints. If he wants to do something, he will simply do it. He can run through walls, teleport wherever, fly, whatever he needs to do, and as such his action maps are relatively shallow. 
#### Opaque Design
The design is actually fairly hard to describe to a layperson. I've had lots of issues describing the capability of the goat to the designers, and all the extra terminology does not help. I'll talk more about this in its own file, but its also incredibly difficult to debug for this reason. Any error in how its set up now, and the queue is empty and the goat freezes. I put a lot of checks to try to keep this from happening, but it keeps rearing its ugly head every week or so.
#### Action and Goal Breakdown
Breaking down actions into atomic steps is very difficult, and not always very useful. As I stated before, the Goat's actions aren't terribly complex, every action is shallow. Goal break down was also a problem, and not one that I solved very elegantly. I added a GoapCompoundGoal to represent goals that are really just two different goals combined. The example is giving the crown to a player by dropping the crown to the ground, and then hitting the target to that dropped crown. Ideally, that would just be a single goal, and if the crown was on another player's head, it would be factored into that action map. I cannot think of the reason that I did not proceed this way, but instead I made a whole new object. Unfortunately, the implementation I made had a constraint that any action chosen to satisfy the preconditions must satisfy all preconditions, no combinations allowed. This was to ensure a purely linear action map, but I wonder if that lead to a increasingly ugly design for goals.

## Design
The design of ThatDamnGoat was (and currently is) a gigantic mess. Lets get into why
### Funstration 
This is a term coined by Brian, the head design lead, its a combination of frustrating and fun. There's something there for sure, there are very frustrating games that can be fun. I think offsetting the frustration with social interaction is an interesting idea, I'm not totally sure if that works. On the one hand, its easier to take things less seriously in a group. At the same time though, do people really want to get together for a frustrating experience? The frustration is also presented in a weird way, through removal of agency.
#### Creative Vision
The game is meant to be a commentary of the futility of our actions, the chaos and absurdity of life, and as such many things happen that are out of the players control. The map changes, their character changes, the Goat knocks them down, etc. I mean the game plays itself for fucks sake. Its just not fun. The player has no agency whatsoever, and its not done in a good way. Which maybe portrays the message in the way intended, but any message is lost in the vast ocean of boredom.
### Information Overload
There are 12 characters, all with their own active abilities, and their own passive buff on specific maps. There are 12 maps, with their own attributes, like launchers or ghosts. A proposed (and hopefully permanently rejected) idea was for the game objective and such to also vary during a match. In a party game. To add further fuel to the fire, these are all subject to change without any control from the player, so players are forced to play on new maps or characters constantly. For a party game, there is so much information to learn to have any idea whats going on. And then once they figure that all out, they still don't really have any control! There shouldn't be this much neccessary onboarding for a party game, and even when you go through it all it, there is no payoff.

## Production
There seems to be this attitude of scope ignorance from most of the leads. Things are suggested, and as long as they add more chaos, its approved. As I'm writing this, the project is about 2 years in development, and nearly everything is still prototype level. We have more than enough content, we just need to make any of it fun.