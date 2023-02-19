# Composition vs Inheritance
source 1: https://www.youtube.com/watch?v=wfMtDGfHWpA&ab_channel=FunFunFunction
The basic idea is: 
Inheritance is what an object is
Composition is what an object has/does

## Multimouse
Multimouse was architectured in a very inheritance based way. This allowed me to utilize polymorphism a ton, which was handy for storage. In the same vein though, it resulted in me sometimes utilizing classes that weren't exatcly designed to be abstract, but were never really instanced. An example is the PhysicsPolygonObject class. When looking for behavior, I would often have to go searching through the inheritance tree to find where its actually coded in.