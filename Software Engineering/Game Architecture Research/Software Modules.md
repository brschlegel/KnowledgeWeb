Source: https://www.tedinski.com/2018/08/14/modularity.html
## Parts of a module
---
- **Private Implementation**: Almost all the code, the module consists of, private implementation details
- **Public Abstraction**: The exposed abstractions that other modules can use
- **Public/Private dependencies**: Other modules that this module depends on
- **Incoming Dependencies**: Other modules that depend upon this module
### Public vs Private Dependencies
A module can use another completely internally, such that another module does not have to know about it to use the modules public abstractions. This would be a private dependency. If another module has to use the depedency, it is public. To change a module, all we have to understand is its dependencies, and the module itself. Therefore the only risk of a ballooning size of information to understand is the public dependencies.
## Modules and Dependencies in Practice
--- 
Oftentimes we end up with a small set of foundational modules that are used all over as public dependencies. Beyond this, we tend to keep the recursive depth of these dependencies pretty low. This leads to a "learn this first" set of modules, being the foundational modules, and all of the modules that use those dependencies. I am skeptical of this structures application to games, as so many systems overlap and co-depend.