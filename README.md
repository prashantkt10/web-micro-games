# Procedural Maze Runner

A minimalist, first-person 3D maze microgame built with Three.js. Procedurally generated labyrinth, patrolling enemies (Yuka), basic AI adaptation (TensorFlow.js), collectibles, hazards, HUD, and difficulty scaling via localStorage.

## How to run
- Just open `index.html` (landing hub) or `games/maze-runner.html` in a modern browser (Chrome/Edge/Firefox). No build step.
- Pointer lock: click the canvas to capture the mouse.
- If you prefer a local server, any static server works (e.g., `python -m http.server`).

## Controls
- Desktop: WASD to move, Mouse to look, Shift to sprint, Space to jump.
- Mobile: Dual on-screen joysticks appear automatically.

## Goal
- Reach the red portal before time runs out.
- Avoid enemies and spikes; grab blue orbs for points.

## Scoring
- Score = (time left * 10) + 50 per collectible.
- Best score and difficulty persist via `localStorage`.

## Notes
- All dependencies are via CDN: Three.js r168, Yuka 0.7.8, TensorFlow.js latest.
- Walls use InstancedMesh for performance; collisions via raycasting.
- Enemies patrol using Yuka path-following; hazards damage on contact.
- An AI hook tracks average speed and may spawn more enemies mid-run.
- For custom AI/difficulty, extend `predictPlayerSkill()` or call `generateAndBuildMaze()` mid-game.

## License
MIT (for this sample). Third-party libraries retain their own licenses.

## Structure
- index.html: landing hub
- games/maze-runner.html: Procedural Maze Runner game

