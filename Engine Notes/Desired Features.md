### Func-Timers
Func-Timers are objects that once started, execute a function at given timesteps. Helpful for frameworks because sometimes you want things to happen a second or two after everything is loaded in. Can allow for repeated calls, as sometimes having things happen every second can be helpful. Operates like a very basic coroutine. In [[MultiMouse]], it was implemented using std::chrono::clock to time things. Utilized [[Delegates]] to supply the function. [[Coroutines]] are a more complete solution to this problem, allowing the method execution to be suspended completely, and resumed where it was left off. Looking into how this is implemented may give us some clues for a more efficient and useful object.

### Debugging and Profiling Tools
In terms of profiling, I believe Visual Studio should provide everything we need. Having tools to print to a console and draw debug lines is pretty important to me, for both engine development and actually building games on top of the engine. A method to have debug messages laid throughout the code and muted or snuffed at different levels would be nice. Visual Studio debugger can also be used.

### Event System
An event system is always helpful for decoupling systems, and allowing objects to be customized with different events and delegates. Using the [[Delegates]] library should provide a powerful starting point.

### Map grid system
It seems like having a grid system for our levels and maps would simplify things for some procedural generation stuff. Maybe toggle-able, as not all types of games would want this grid?