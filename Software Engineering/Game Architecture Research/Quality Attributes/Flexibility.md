--- 
\[1\]: https://dzone.com/articles/the-seven-virtues-of-a-good-design
A flexible program does not require rigid parameters or preconditions. One routine/module can be used in different ways, or process different kinds of data. The ability of a system to adapt to future changes

### Postel's rule
"Be conservative in what you do, be liberal in what you accept from others". Chose the most generic type for inputs and most specific for outputs.
### Composition Over Inheritance
Composition allows much easier and fine grained variance in functionality when compared with inheritance
### Come down to earth
Of course, at the end of the day you need to take a stand somewhere. We want to ensure the code is readable and understandable in some sense, and keep that coupling low.

## Definition in terms of [[Software Modules|Modules]]
---
Flexibility could be thought of in terms of the size of the public abstractions of our different modules. Having private implementations is nice, but anything that is hidden behind that private-public wall cannot be extended upon. 
### [[System Boundaries]]
To make a system extensible or re-usable is to make it closer to a system boundary. The more modules extend it, the more the design becomes more difficult to change in the future. We really don't want to be making these unnecessarily, so we need to be sure that the design *should be* a system boundary.