This repo will be amended to document the full details of every advanced physics mechanic in T3 in both theory and practical use.

![ShowQADebug](https://github.com/AltimorTASDK/tribes3-advanced-physics/assets/4999944/4a16dfc9-c607-45d4-bb47-8ab85c64b924)

Precise information was obtained by enabling `ShowQADebug=True` in `%LOCALAPPDATA%/Topaz/Saved/Config/Windows/GameUserSettings.ini` for position and velocity display, capping my framerate to 60 to ensure consistent deltatime and that I record every frame, and analyzing crafted scenarios frame by frame to deduce the logic. `ShowQADebug` uses the engine units of cm and cm/s, and the Z axis is up.

Some numbers and curves were also obtained by datamining and verified in-game after getting permission from Prophecy's community manager. My understanding is that game science is okay. If you know how and do the same, please respect Prophecy, don't go around leaking unused/unreleased stuff, and don't do anything more than inspect the files on your drive. Curve visualizations are generated with [this tool](https://github.com/AltimorTASDK/ue-curve-graph).

## Recommended reading order
1. Slope deflect
2. Ski landing

## Binds
The binds used in the input display are:
| Key              | Action        |
| ---------------- | ------------- |
| Space            | Ski           |
| Control          | Jump          |
| Right Click      | Jet           |
| Mouse Wheel Down | Jet (bhop)    |
