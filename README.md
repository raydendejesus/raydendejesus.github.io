# Web Projects — a collection of 205 self-contained apps

A growing portfolio of small, focused web applications — games, developer tools, and
interactive visualizations. Every project is built with **vanilla HTML, CSS, and JavaScript**:
no frameworks, no build step, no dependencies, and no network calls. Each one is a single
`index.html` that runs by opening it in a browser.

**🔗 Live: https://raydendejesus.github.io/**

---

## Why it's built this way

Every app is intentionally **zero-dependency and self-contained**. That constraint means:

- **It just works** — no `npm install`, no bundler, no server. Open the file, it runs.
- **It's auditable** — each app is one readable file you can view end to end.
- **It's durable** — nothing breaks when a package updates or a CDN goes down.
- **It's fast** — no framework overhead; everything is hand-written.

Anything that would normally pull in a library is implemented from scratch instead (see
[Notable engineering](#notable-engineering) below).

## What's inside

| Category | Count | Examples |
|---|---|---|
| 🎮 **Games** | 59 | Tetris, Minesweeper, Snake, 2048, Asteroids, Sudoku, Chess-style AI opponents |
| 🧑‍💻 **Developer tools** | 104 | JSON/YAML/CSV converters, regex tester, JWT decoder, CSS generators, subnet calculator |
| 🛠️ **Utilities** | ~28 | Unit/timezone converters, calculators, password & QR generators, Markdown preview |
| ✨ **Visual toys** | ~14 | Particle systems, flow fields, Mandelbrot explorer, plasma & ripple effects |

The full, searchable index is the [live site](https://raydendejesus.github.io/).

## Notable engineering

A few things implemented **without any libraries**, just standard browser APIs:

- **QR code generator** — a from-scratch Reed–Solomon error-correction encoder.
- **Parsers written by hand** — Markdown, YAML, TOML, and JSON-path resolvers.
- **Game AI** — minimax (with difficulty levels) for tic-tac-toe; heuristic AIs for
  Connect Four, Checkers, Reversi, Gomoku, and Battleship.
- **Graphics & math** — a Mandelbrot set explorer, metaball/“lava-lamp” rendering,
  boids flocking, and Perlin-noise flow fields, all on `<canvas>`.
- **Crypto** — text encryption via the Web Crypto API (AES-GCM + PBKDF2); SHA hashing
  via `SubtleCrypto`.
- **Audio** — synthesized sound (drum machine, metronome, playable piano) using the
  Web Audio API — no audio files.

## Project structure

```
/                       → portfolio landing page (this site's index.html)
/<project-name>/        → one folder per app, each a single self-contained index.html
```

## Running locally

```bash
git clone https://github.com/raydendejesus/raydendejesus.github.io.git
```

Then open `index.html` (or any `<project-name>/index.html`) in a browser. That's the whole setup.

## License

Released under the [MIT License](LICENSE).
