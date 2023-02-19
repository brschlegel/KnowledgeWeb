Source: https://docs.godotengine.org/en/stable/tutorials/best_practices/introduction_best_practices.html
## Scene Organization
---
When possible, scenes should have no dependencies. When a scene does have to interact with an external dependency, using [[Dependency Injection]] is suggested. 
### Dependency Injection in Godot 
Connecting a parent method to a child signal is the best way to respond to behavior in the child. There is a FuncRef property that can operate like a delegate, and is a way of starting behavior in the parent from the child. In general, you should favor keeping data in house anyway, but if you must require additional context, you can implement a \_get\_configuration_warning() function to warn users in-engine if that context is not met.
### Proposed Node Tree Structure
A "Main" node serves as the etnry point of the game. Also serves as birds eye view of the other data and logic in the program. Nodes that encompass the world and the GUI are the children of main. The children of the "World" node would be akin to the "level".
- Main
	- World
	- GUI
Each subsystem within the game should have its own section in the SceneTree. Parent child relations should only be used when nodes are effectively different elements of the parent. If children need to position themselves within the transform hierarchy of a node but isn't really a "part" of that node, then you can use a [Remote Transform](https://docs.godotengine.org/en/stable/classes/class_remotetransform2d.html#class-remotetransform2d). Overall, the SceneTree should be thought of in relational terms rather than spatial ones. If a node is dependent on its parent's existence, then they should be children. If not, they can be somewhere else in the SceneTree. 
## When to use Scenes vs Scripts
---
### What is the difference?
The difference can be hard to parse out at times, as often a Scene will have an associated root script. The best practices page says: "Scenes are declarative, scripts are imperative" (See [[Declarative vs Impertative Programming]]). Scenes include a selection of nodes, how they are organized, and the signal connections between them, while a scripts is, well a script. 
### "When to use"?
Of course the answer is you should use both almost always. They are confusingly referencing whether you should build out an object using the editor (Scenes), or make them in the constructor via script. The arguments for using a script for this to me seem incredibly flimsy. I guess if you use a script, you can register it inside of the editor so it can be used like any other node. You can just instance a packed scene for most of my use cases however.
## Autoload vs Regular Nodes
---
Autoload nodes are engine built singletons, being able to be called from anywhere and existing outside the normal scene tree.
### Problems Caused
Because autoloads are global, they can be called from anywhere. This makes it hard to hunt down the source of a bug relating to that system. In addition, if there are errors in that node, all nodes using it could break. 
### Ways to avoid using Autoloads
_Resource_ is a type that operates similarly to Unity's _Scriptable Object_. If you wanted to store some data in a single location, resources are your best bet.
### Overall
Overall these are just static classes. Static classes are really not the devil everyone says they are, especially when working on solo projects.
## Avoiding using Nodes for everything
--- 
There are multiple lighter data types that can be used: 
- Object
	- You have to manage your own memory for this, not really sure what this actually gives you
	- Maybe a reference to pass around?
- Reference
	- Like an object, but don't need memory management. Used often as data storage
- Resource
	- Probably what you will actually end up using, they have the ability to save and load data into files
	- Have inspector compatability as well
## Godot Interfaces
---
GDScript does not implement interfaces like C# does, as the language uses [[Duck Typing]]. Because of this, accessing data or logic on a seperate object takes the form of asking if that object implements that specific method/data. This seems sloppy to me honestly, but does allow for some good flexibility. There are ways of detecting if a node has the method you want: `node.has_method(string)`. You can even wrap these in an `assert()` method to trigger errors if the given method or property is not available. The best practices doc also mentions that you can use groups (tags) to imply that an interface exists. Of course, this also means that you as a developer have to hold yourself to that. I am not sure if the added freedom is worth it, or if you aren't losing much by not explicitly laying out interfaces.
## Project Organization
--- 
## Style Guide
- Use **snake_case** for folder and file names. C# scripts get **PascalCase**
- Use **PascalCase** for node names
