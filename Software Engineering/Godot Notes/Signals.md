https://docs.godotengine.org/en/stable/getting_started/step_by_step/signals.html
Signals are Godot's events, seems like the engine is built around them pretty heavily. 
## Reference By Name
Like alot of Godot, the way you get references to which signal to connect to and which method to register is by string, which seems fragile to me. Also annoying as renaming the function is a breaking change
## Registering through GUI or Code
You can connect to a signal through code or through the engine GUI. It actually shows in the code editor that a method is connected to a signal which is handy, but connection through code still might be more traceable.
## GDScript
Creating signals in GDScript is pretty damn easy, all you do is say `signal signal_name`. When you do it like this its all hooked up in the editor as well and you can register to signals using the GUI