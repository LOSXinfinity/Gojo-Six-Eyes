# Gojo Satoru — Six Eyes Tribute

Cinematic, scroll-free tribute to **Gojo Satoru** from *Jujutsu Kaisen*. Five scenes driven by button navigation — no scrolling required.

## Scenes

| # | Scene | Interaction |
|---|-------|-------------|
| 0 | **Hero** — Eyes closed, title reveal | Auto-entry |
| 1 | **Six Eyes Awakening** — Video: eyes opening, lightning strikes at thresholds | Click ▶ |
| 2 | **Domain Expansion** — Hand-seal video → detonation → Unlimited Void splash | Click ▶ |
| 3 | **Infinity Barrier** — Hover to reveal Six Eyes through the mask | Mouse move |
| 4 | **Outro** — "Throughout heaven and earth, I alone am the honored one" | Click ▶ |

## Features

- **Zero framework** — Single `index.html` (~90 KB), only external dep is GSAP via CDN
- **Custom cursed-energy lightning** — Fractal midpoint-displacement channels, 4-layer stroke (violet corona → indigo haze → cyan sheath → white-hot core), restrikes reuse the same path
- **Web Audio synths** — Awakening hum, domain boom, infinity *shing*; gated by first user gesture
- **Fluid cursor** — Screen-space trails, look-at nearest interactive element, hot-state expansion
- **Mouse/gyro tilt parallax** — `data-tilt` elements respond to cursor or device orientation
- **Film grain** — SVG turbulence overlay, stepped animation
- **Preloader** — Kanji iris bloom + progress bar + audio cue
- **HUD** — Live clock + cursed-energy/domain status per scene
- **Reduced motion** — Respects `prefers-reduced-motion`

## Quick Start

```bash
# Serve locally (required for video + ES modules)
npx serve .
# or
python -m http.server 8000
```

Open `http://localhost:3000` (or `:8000`).

## Assets

Place these in the project root (already included):

```
├── index.html
├── eyes opening.mp4          # Scene 1 video
├── hand-sign.mp4             # Scene 2 video
├── img/
│   ├── gojo_unmasked.png     # Scene 3 under layer
│   ├── gojo_masked.png       # Scene 3 top layer (mask)
│   ├── gojo_portrait.png     # Outro background
│   └── domain_splash.png     # Domain Expansion splash (optional)
├── eyes_opening_frames/      # 101 frames (fallback/poster)
└── hand-sign_frames/         # 61 frames (fallback/poster)
```

## Controls

| Key / Action | Result |
|--------------|--------|
| `→` / `Space` / Click **Next** | Next scene |
| `←` / Click **Prev** | Previous scene |
| Dot indicators | Jump to scene |
| Mouse move (Scene 3) | Reveal Six Eyes through mask |

## Customization

Edit CSS custom properties in `:root` (lines 12–26) to recolor:

```css
--cyan:#4fd8ff;       /* Six Eyes */
--indigo:#5b6cff;     /* Infinity */
--violet:#b46bff;     /* Hollow Purple */
--violet-blue:#3a6bff;
```

## License

Fan tribute. Jujutsu Kaisen © Gege Akutami / MAPPA. Not for commercial use.
