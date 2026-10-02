# Robot Soccer Pong

[Open the editable scene in Strata](https://tejaswigowda.com/strata-editor/#repo=jordan77-lang/strata2&file=pong/pong.json).

The ball is a classic soccer ball with 12 black pentagons and 20 white hexagons. The player is a blue robot; the computer is an orange robot. An elevated sideline camera shows both robots, the two netted goals, and the soccer pitch within a 180-by-180-unit grass field.

- `pong.json`: self-contained Strata project, including the scoreboard image. Open it with **File > Open** in Strata.
- `pong.glb`: matching portable 3D scene for use with the existing `pong.js` controller.
- `pong.js`: game controller with the same sideline camera as the editor. Movement, scoring, collisions, reset, and sound are unchanged.
- `pong-preview.png`: preview captured in the Strata editor with Playwright.

The original `Ball`, `Player_Paddle`, and `Computer_Paddle` objects retain their names, UUIDs, transforms, and collision geometry. Their old surfaces are hidden; the replacement models are children of those same objects. The ball keeps its original 0.35-unit radius. The marked pitch keeps the original playing dimensions. The scoreboard sits on the far sideline, clear of both goals. Grass textures are embedded in the project.

Validated in Playwright: scene loading, GLB loading, player movement, robot collision bounce, scoring, reset, and 600 simulated game frames.

![Robot Soccer Pong](pong-preview.png)
