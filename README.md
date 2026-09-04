# Portfolio — Animated Edition

A dark, motion-forward developer portfolio. Plain HTML/CSS/JS — no build tools, no dependencies, no frameworks.

## What's different from a static template

- **Live particle network** in the background (canvas), lines connect nearby dots and react to your mouse
- **Custom cursor** — a dot + trailing ring that expands over links
- **Typing effect** in the hero (cycles through a few lines like a terminal)
- **Scroll reveals** — content fades/slides in as you scroll (IntersectionObserver, not scroll-jank)
- **Tilt-on-hover project cards** with unique generated SVG art per project (no stock photos needed)
- **Magnetic buttons** that nudge toward your cursor
- **Animated stat counters** that count up when scrolled into view
- Respects `prefers-reduced-motion` — all of the above turns off automatically for people who've asked their OS for less motion, and the custom cursor is disabled on touch devices

## Files

- `index.html` — structure and content
- `style.css` — all styling and animation keyframes
- `script.js` — canvas network, cursor, typing effect, reveals, counters, tilt/magnetic effects

## How to run it

**Just open it:** double-click `index.html`.

**Local server (recommended):**
```
cd portfolio-v2
python3 -m http.server 8000
```
Open http://localhost:8000

**In VS Code:** open the folder, install the "Live Server" extension, right-click `index.html` → "Open with Live Server".

## How to customize it

- Replace "Your Name", the email, and placeholder project/about copy in `index.html`.
- The four project "images" are generated SVGs (no real photos needed) — swap the `<svg>` blocks inside each `.project-media` for your own abstract art, or replace with a real `<img>` if you have screenshots.
- The typing-effect lines are the `typedStrings` array near the top of `script.js`.
- The stat counters (`7`, `42`, `99%`, `12`) are set via `data-count` / `data-suffix` attributes on the `.stat-num` spans in `index.html`.
- Colors, fonts, and spacing are CSS variables at the top of `style.css` under `:root`.
- Particle count and connection distance are tunable in `script.js` (`LINK_DIST`, `MOUSE_DIST`, and the density formula in `initParticles`).

## Deploying it for free

GitHub Pages, Netlify, or Vercel — drag-and-drop the folder or push to a repo, no backend needed.
