# Ski landings
Ski landings, or ski-landing as a verb, refers to any time the player lands with ski engaged and enters ski mode, which grants special collision assistance intended to help with imprecise landings. Note that you must *land*, not merely touch the ground, so you must release your jets to ski-land. Holding jets for downward landings is a common mistake and will result in neither ski-landing nor slope deflecting, losing speed instead.

When a ski landing happens, your direction along the ground is determined by natural collision, but **your new speed is determined by applying an artificial curve based on impact angle** that determines how much of your original speed should be lost.

Here's that curve, with the speed loss of a natural inelastic collision for comparison:

![SkiOnLandVelocityLoss](https://github.com/AltimorTASDK/tribes3-advanced-physics/assets/4999944/74646175-acf7-494c-96ed-9facb2e19d8c)
*Technical note: The original curve is in terms of the dot product between your direction and the surface normal, but I've reprocessed it to be in terms of the angle between you and the slope tangent in degrees for convenience.*

Note that ski landings are always substantially better than natural collisions and **retain full speed if you're within 30 degrees of lining up with the slope**, the same effect as a slope deflect. In fact, since you can also ski-land uphill as long as it's within 30 degrees, it can be a free replacement, especially when followed by a jump off a convex slope to immediately break ground contact.

https://github.com/AltimorTASDK/tribes3-advanced-physics/assets/4999944/b767c6c8-3a16-4538-bfd1-624571bd7404

*A 20.6 degree bump on the way down and a 24.2 degree "ski landing deflect" on the way up. Jets were only used after landing. 0 speed loss from collisions.*

This might sound like it makes it really easy to ski perfectly, but in many cases, it just moves the ideal target to the edge of the 30 degree range. Being able to land on flatter ground allows immediate horizontal speed conversion and allows hitting flatter hills from trajectories that would normally be steep for them so that more jets can be used for speed gain.

https://github.com/AltimorTASDK/tribes3-advanced-physics/assets/4999944/3af52295-644e-441e-87e4-714a7bc000e0

*A 29.5 degree landing*

We can even gain speed by falling onto flat ground.

https://github.com/AltimorTASDK/tribes3-advanced-physics/assets/4999944/a11ca290-83b7-4ec1-aa1e-35a3b35433b7

*I've actually had to do this in a game of Raindance.*

It also gives you more freedom in *where* you land on a hill, allowing you to redirect yourself to the side without speed loss and line yourself up differently for upcoming hills, such as landing near the top of one hill and skimming off the next with a shallow slope deflect or another ski landing. You can also land closer to the bottom of a hill to save some time or minimize ground contact when necessary. One of the most effective ways to make use of the redirection potential is to get as vertical as possible with a steep slope deflect and ski-land on another sufficiently steep slope with a different horizontal direction. This technique works to some extent in every Tribes game, but T3's collision mechanics make it significantly more powerful and versatile.

*Technical note: Unlike early alphas, the force of gravity is identical while falling and while skiing. It barely matters, but if you aren't ski speed capped, skiing downhill generally gives more speed at the cost of time. The difference in acceleration is proportionate to the sine of the slope and the extra time spent accelerating to the bottom is inversely proportionate, so the total acceleration is the same. The difference is the Z acceleration of freefall gravity isn't the same as velocity magnitude gain unless you're going straight down, whereas slope gravity will be perfectly efficient when going downhill.*
