Source: https://dev.to/ruizb/declarative-vs-imperative-4a7l#:~:text=Declarative%20programming%20is%20a%20paradigm,which%20mutate%20the%20program's%20state.
## What are they?
Declarative programming describes **WHAT** a program does, without explicitly specify its control flow. Imperative programming describes **HOW** a program should do something, by explicitly specifying each instruction. Because everything needs to distill down into a set of instructions for the GPU, declaritive programming is a sort of abstraction on top of Imperative programming. Engines, interpreters, and compilers are what make the journey from declarative to imperative code. Imperative code can be thought of as the **implementation details** of the software. Declarative code makes all of its state-changes at the end of its instructions, likely with an API call
## Why do I care?
In general, we should try to write declarative code when we can, as software is read and debugged by humans. Overall, games are complicated enought that you will be doing both imperative and declarative programming. It may be useful to find a way to seperate these paradigms; This section of the code only does Imperative stuff or Declarative stuff, but never both. Maybe systems are made imperatively, while content is designed declaratively? Honestly, I don't really see how the benefits are worth the changes. There are ideas about keeping things immutable that are worthwhile, but the complete shift seems like a bad idea to me.