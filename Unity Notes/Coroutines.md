# Coroutines
Documentation: https://docs.unity3d.com/Manual/Coroutines.html

### Destroying/Disabling Objects
One of the main issues with Coroutines I have run into is if the object that the script is attached to is either disabled or destroyed, that coroutine stops running. This can be helpful for some things, for example a destroyed enemy shouldn't be scanning for the player, but when trying to apply debuffs or the like it can be very frustrating. The solution might be a global coroutine manager class that can be used to call coroutines from an object that is always active. Its worth keeping in mind that you can start a coroutine from any Monobehaviour