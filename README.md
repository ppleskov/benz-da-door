# Cyprus Mouse Defense

Browser-based 2D shooter game. A mouse defends itself from evil cats, lions and tigers on the island of Cyprus by shooting water at them.

## How to Play

Open `index.html` in a browser.

- **Click** to shoot water from the mouse toward your cursor
- **Cats** (orange) — 1 hit to scare, -1 life if they reach you
- **Lions** (golden, with mane) — 3 hits to scare, -2 lives. Appear after 60s
- **Tigers** (orange with black stripes, large) — 5 hits to scare, -3 lives. Appear after 120s
- **Zora** (black & white cat) is friendly — if she reaches the mouse, you gain a life. Don't accidentally scare her!
- **Water is limited** — watch the supply bar, it regenerates over time
- Chain hits for **combo multipliers**

## Features

- Satellite map of Cyprus (ESA) as the game background
- Progressive difficulty — cats spawn faster, lions and tigers join over time
- Multi-hit enemies with HP bars and knockback
- Combo scoring system with milestones
- Particle effects, screen shake, floating text
- High score saved in localStorage

## Tech

Single-file game (`index.html`) — HTML5 Canvas, vanilla JS, no dependencies.
