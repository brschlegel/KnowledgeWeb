# Coroutines
Documentation: https://docs.unity3d.com/Manual/Coroutines.html

### Destroying/Disabling Objects
One of the main issues with Coroutines I have run into is if the object that the script is attached to is either disabled or destroyed, that coroutine stops running. This can be helpful for some things, for example a destroyed enemy shouldn't be scanning for the player, but when trying to apply debuffs or the like it can be very frustrating. The solution might be a global coroutine manager class that can be used to call coroutines from an object that is always active. Its worth keeping in mind that you can start a coroutine from any Monobehaviour

### Global Coroutine Manager
No problems so far with the coroutine manager in WhenPushComesToShove. Its really helpful to be able to specify when a coroutine should die with the object. It may be helpful to have a coroutine manager as a non-static object to be put on the "root", as many times having a completely global manager isn't neccessary or wanted, rather just a manager for that entity.

## WaitForSeconds
WaitForSeconds generates garbage whenever you make a new one, especially for cooldowns or things that are called often you should just cache them in a static dictionary