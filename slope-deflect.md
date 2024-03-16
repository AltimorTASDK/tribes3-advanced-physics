# Slope deflects
Slope deflects are by far the most important advanced technique, and you're already using them. The expected use case is to allow players to naively jet up steep slopes that their jets couldn't normally scale without speed loss. However, the conditions are very generous, and luckily for us, quite simple.

### Conditions:
1. Be jetting
2. Collide with a surface you'd be able to stand on
3. Have a Z velocity greater than 0 (moving upward)

When you meet these conditions, at the end of the physics frame, after your velocity has been clipped to be tangent to the slope, your original velocity magnitude is applied to your new direction. **You deflect off the slope with full speed.** Importantly, the angle of the slope, how upward your approach is, and how long you jet for all don't matter. This results in an important property: **Any slope face can be traversed with a single frame of jets.**

At the bottom of a hill (concave part), you'll have to keep (jump)jetting up, but deflecting off the side/top of a hill (convex part) will let you clear it with full speed no matter what. This allows many energy, speed, and time optimizations. For example, rather than skiing or jetting up the curve at the bottom of a hill, jump over it (or as high as you can) and use your jets on impact, feathering them to stay above 0 Z velocity if needed. You can similarly jump/jet across bowls and valleys from partway downhill and slope deflect out to cut out the time spent skiing through while exiting at not just the normal angle, but any lesser angle from the top of the exit slope.

https://github.com/AltimorTASDK/tribes3-advanced-physics/assets/4999944/ddd7f250-2cf1-4bfc-bdd9-7895afbaf16b

https://github.com/AltimorTASDK/tribes3-advanced-physics/assets/4999944/5d22fe95-600f-45fe-940f-a18191076843
