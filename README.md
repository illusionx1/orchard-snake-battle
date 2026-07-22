# Orchard Snake Battle

A browser-based, single-file multiplayer snake game built with vanilla JavaScript and the HTML5 Canvas API. Eat fruit to grow, cut through smaller rivals, leap over enemies with a special ability, and battle your way through a 10-level story mode against a final boss.

![Made with JavaScript](https://img.shields.io/badge/Made%20with-JavaScript-yellow)
![No dependencies](https://img.shields.io/badge/Dependencies-None-green)

## Features

- **Battle Mode** — Free-play mode against 0–3 computer-controlled snakes on any map, at any difficulty.
- **Story Mode** — 10 hand-tuned levels of increasing difficulty, capped off with a boss fight against the Orchard Warden. Beating the boss permanently unlocks the Orchard Dash ability.
- **AI opponents** — Four difficulty tiers (Easy, Medium, Hard, Insane), each governed by independently tuned heuristics: wall-avoidance probability, snake-avoidance behavior, pathfinding quality, and dash frequency. Pathfinding uses a flood-fill algorithm (60-cell lookahead) to avoid self-trapping.
- **Size-based combat** — Grow bigger than a rival and you can cut clean through its body; cross one your size or bigger and you're the one who falls. Defeated snakes scatter their body as fruit for survivors to eat.
- **Special ability** — Once unlocked, press `E` to dash and leap clean over any snake in your path, walls and obstacles permitting.
- **Custom snake colors** — Pick from a 16-color quick palette or enter any hex code / use the native color picker.
- **Multiple maps** — Orchard (open field), Grove (scattered clusters), Hedge Maze (walled inner ring), and Pillars (evenly spaced obstacles).
- **Smooth, responsive rendering** — Fixed-timestep game loop with `requestAnimationFrame` interpolation for consistent 60 FPS movement, plus a 2-move input buffer so quick direction changes are never dropped.
- **Persistent progress** — Story progress, ability unlock, best score, and color choice are all saved locally via `localStorage`.
- **Responsive design** — Scales to fit any screen size, with device-pixel-ratio-aware canvas rendering for crisp visuals on both desktop and mobile (Android/iOS).

## How to Play

1. Open `snake.html` in any modern web browser — no installation or build step required.
2. Choose **Battle** or **Story mode** from the main menu.
3. Pick your snake color, map, opponents, and difficulty (or story level).
4. Controls:
   - **Arrow keys / WASD** — move
   - **Space** — pause
   - **E** — dash / leap over snakes (once unlocked)
   - **Swipe** — move (touch devices)

## Tech Stack

- Vanilla JavaScript (ES6)
- HTML5 Canvas API
- CSS3 (responsive, clamp-based scaling)
- `localStorage` for persistence

No frameworks, build tools, or external dependencies — it's a single self-contained HTML file.

## Project Structure

```
snake.html   # Entire game: markup, styles, and logic in one file
```

## Running Locally

Since this is a single static HTML file, you can either:

- Double-click `snake.html` to open it directly in a browser, or
- Serve it locally for a more consistent experience:
  ```bash
  python3 -m http.server 8000
  ```
  then visit `http://localhost:8000/snake.html`

## License

Feel free to use, modify, and build on this project.
