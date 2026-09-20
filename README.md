# ASTEROIDS

A single-file, dependency-free Asteroids clone rendered on an HTML5 canvas with a faint CRT look, synthesized retro audio, and touch controls. Everything — markup, styles, game logic, and sound — lives in [index.html](index.html).

## Play

Open [index.html](index.html) in any modern browser. No build step, server, or install required.

```bash
git clone https://github.com/stormwild/asteroid-game.git
cd asteroid-game
start index.html        # Windows
# open index.html       # macOS
# xdg-open index.html   # Linux
```

Press **Enter** (or tap the screen on touch devices) to start.

## Controls

| Action           | Keyboard               | Touch                    |
| ---------------- | ---------------------- | ------------------------ |
| Turn             | `←` / `→` or `A` / `D` | Left / right buttons     |
| Thrust           | `↑` or `W`             | Thrust button            |
| Fire             | `Space`                | Fire button              |
| Hyperspace       | `Shift` or `H`         | Warp button              |
| Pause            | `P`                    | Pause icon (top-right)   |
| Sound            | `M`                    | Speaker icon (top-right) |
| Start / continue | `Enter`                | Tap anywhere             |

Touch controls appear automatically on coarse-pointer devices. The game auto-pauses when the tab loses focus.

## Gameplay

- Clear every rock to advance. Each wave adds more asteroids (up to 11) and increases their speed.
- Large / medium / small asteroids score **20 / 50 / 100** points.
- Large saucers are worth **200**, small saucers **1000**. Small saucers aim their shots and get more accurate each wave.
- Saucers collide with asteroids too — sometimes they do your work for you.
- An **extra ship** is awarded every 10,000 points.
- Hyperspace teleports you to a random safe spot away from rocks and saucers.
- High score and mute preference persist in `localStorage`.

## Features

- Canvas rendering with device-pixel-ratio scaling, twinkling starfield, and subtle scanline/vignette overlay.
- Fully procedural audio via the Web Audio API — thrust rumble, saucer warble, explosions, the classic two-note heartbeat that speeds up as a wave thins out, and jingles for extra ships and game over. No audio assets.
- Attract mode with demo saucers, wave banners, extra-ship toast, and a game-over screen that flags new high scores.
- Responsive layout with `env(safe-area-inset-bottom)` padding for notched phones.

## Tech

Plain HTML, CSS, and vanilla JavaScript (ES2015+). The only external resource is the [Chakra Petch](https://fonts.google.com/specimen/Chakra+Petch) font from Google Fonts; the game falls back to a system monospace font if it isn't available.

## License

No license has been specified yet.
