--- 
\[1\]: https://gameprogrammingpatterns.com/architecture-performance-and-games.html
"The key goal of software architecture: minimize the amount of knowledge you need to have in-cranium before you can make progress". If 2 pieces of code are coupled, you cannot understand one without understanding the other.
### Cost of Decoupling
Decoupling sounds really great in theory, which is why there's so much hype around abstraction, modularity, etc. Adding and abstraction, or when trying to plan for extensibility, you are neccessarily speculating what you will need. If you get it wrong, it becomes extra code to write, debug, and most importantly understand. Instead of reducing your mental load via decoupling, you end up having to parse through layers of abstraction and generalization.