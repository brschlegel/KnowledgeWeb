## Week 1
- Frustrated with rigidbodies just setting their scale back to 1 without printing any sort of warning
- Dynamic Typing really sucks and makes it harder to develop
- Feel a bit babied
- Miss being able to see the inspector while code is running
## Week 2
- Starting to actually enjoy learning the engine and working on the little prototype. May be because I told myself to stop thinking so hard about architecture and just make something that works. 
- Holy shit static typing makes working with GDScript so much more palatable
- Really not digging the script editor in engine bit tho
- Godot really seems to be a huge extension on my prop system idea like in [[MultiMouse]]
- Debugging tools are actually pretty strong
- Sometimes it can be hard to tell what node I'm actually on 
## Week 3
- Its hard to find the transform data of an object sometimes in the inspector
## Week 4
- Change your main project scene often when working on a new feature
- Working with anchors seems to not be the move at all. Use containers for UI
- Containers are an abstraction off of anchors, would have been much easier to learn
- To center text in a rich text label you have to use [Bbcode](https://docs.godotengine.org/en/stable/tutorials/ui/bbcode_in_richtextlabel.html)?
- The statement "Scenes are declarative and scripts are imperative" has given me days long headaches
- Don't really feel great about duck typing
- Probably makes sense to have unchanging roots for the world and for the GUI
- Input events persist through setting time to zero
## Week 5
- Getting vscode to work was a huge pain and I never actually figured it out. Something about a language server?
- Make sure your rigidbody is the parent of everything it should be: otherwise nothing will move with it
- String formatting is fairly easy 
- Bruh no debug draw??????
- Scenes should generally be testable on their own, but scripts and nodes dont have to be
- Remote Transform is a really interesting idea, "Scene Tree should be thought of on relational terms rather than spatial ones" [[Best Practices#Proposed Node Tree Structure]]
## Week 6
- TIlemap stuff seems intuitive enough
- Adding collision to tiles is easy 
- 2d navmesh :)
- Agents are only an implementation of the navigation API, can make your own
- make sure to save parent scenes to have changes in child scene
## Week 7
- C# has been going well
- Have to rebuild godot manually for exports and signal names
- Benefits of signal over regular c# event?
- Getting the debugger in vscode to work has been a pain
- The workflow is still a bit unfamiliar, im sure switching between scenes so much will eventually feel better
- Can call C# methods from GDScript with the .call() method
## Week 10 (lol)
- Dont get too bogged down in parent child relations. Nodes can reference siblings its alright
- https://www.youtube.com/watch?v=rCu8vQrdDDI&ab_channel=FirebelleyGames