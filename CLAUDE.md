# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

"Cyprus Mouse Defense" — a single-file browser-based 2D shooter game. A mouse (animal) in the center of the screen defends itself from cats, lions and tigers by shooting water, set against a map of Cyprus.

## Architecture

The entire game lives in `index.html` — a single file with inline CSS and JavaScript. No build system, no dependencies, no frameworks.

**Rendering**: HTML5 Canvas with `requestAnimationFrame` game loop. All graphics are drawn with canvas primitives (no external assets).

**Key systems in the script block:**
- **Game state** (`state` object) — holds all mutable data: entities, timers, score, screen mode
- **Entity types**: Player mouse (stationary center), enemies (cat/lion/tiger with varying HP, size, spawn rates), Zora (black-white friendly cat), WaterProjectile (shot on click)
- **Collision detection**: Circle-vs-circle using squared distances
- **Background**: Cyprus island outline drawn as a polygon from `CYPRUS_OUTLINE` coordinates, cached to offscreen canvas
- **Screen flow**: `title` → `playing` → `gameover`, controlled by `state.screen`

## Development

No build step. Open `index.html` directly in a browser to test. Use any local HTTP server if needed:

```
python3 -m http.server 8000
```
