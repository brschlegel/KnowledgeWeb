# Delegates
Post: https://simoncoenen.com/blog/programming/CPP_Delegates
Delegates is a very small library made to try to emulate Unreal Engine's delegate system. Works somewhat similarly to C# delegates, although using them is a bit more involved. Allows for both delegates, and multicast delegates (re: C# Events). Can add functions or methods, but more curiously you can also add Lambda Functions. In terms of actual implementation, its a bit beyond my pay grade for C++, especially templates.

## Function Pointers
In standard C++, the closest you get to delegates is function pointers. If used as standard, then the function has to be the same type, and also has to be from the same class. Doing this generically is a huge pain, and not trivial, so these delegates are super handy. 

## MultiMouse
Delegates were a godsend for [[MultiMouse]] I had wanted to use C# like delegates to specify what would happen with keyboard input, or to set up coroutine-like [[Desired Features#Func-Timers | FuncTimers]]. The best solution was Function pointers at the time, but due to their lack of generality, I had to do a super ugly workaround that involved putting the functions in a dedicated file and passing in the entire scene to get the context I needed. instead, using delegates allowed me to to have a much cleaner solution.

### Scripting-lite
Using delegates combined with lambda functions in MultiMouse allowed me to also include a sort of pseudo-scripting to MulitMouse objects. With Scenes and Levels they had init and update delegates, which could be hooked into by lambda functions, providingcustom scripting to individual scenes and levels. Other objects also got update delegates, as well as other delegates fit into their respective behaviour, such as entry delegates on Goals.