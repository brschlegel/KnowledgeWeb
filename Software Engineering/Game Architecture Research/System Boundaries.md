-- ---
\[1\]: https://www.tedinski.com/2018/02/06/system-boundaries.html
System boundaries are code that we cannot easily change the design of, mostly due to the fact that its a publicly exposed interface for third-party developers. They could be totally external, or even fictional to limit communication between teams. Can also be totally unintentional; so widely used that the costs of changing it are just too high.
### Breaking Changes
Not being able to make breaking changes is what truly defines the system boundary. As most good design is iterative, and you cannot iterate on this, its important to get the design on these boundaries correct the first time.
### Why create these boundaries
We create boundaries because its the only way to make true reusable code. It lets us completely [[Decoupling|Decouple]] the system from its users by way of an abstraction. Then we can reuse it across many different users. Sometimes its nice to deliberately cut off modules from the rest of the system. so its incredibly clear its independent.
### Higher Stakes
Its much easier to shrug your shoulders and just try something, knowing that if it becomes a problem its easy enough to refactor later. The defining features of a system boundary however is that you cannot just refactor it later.