# Buckling Branch Jukebox

A static offline toy sandbox demonstrating post-bifurcation branch diversity in a slender 3D beam under load. Based on the Bi-FORK paper (arXiv:2610.12449).

## Run Instructions

Open `demo/index.html` directly in a browser (file:// protocol works). No build step, no server, no network required.

```bash
# Option 1: Open directly in browser
open demo/index.html        # macOS
xdg-open demo/index.html    # Linux
start demo/index.html       # Windows

# Option 2: Serve locally (optional)
python3 -m http.server 8000  # then visit http://localhost:8000/demo/index.html
```

## Controls

- **Normalized load** (0–1): Raise above 0.55 to split the beam
- **Initial imperfection** (−0.15 to 0.15): Favors positive or negative buckle branch
- **Camera orbit** (−180° to 180°): Rotates view only; does not change the stored branch
- **Physical branch** (+/−): Select which post-critical branch to display in the left pane
- **Clustered / Spread**: Toggle ensemble display mode (right pane)
- **Play / Pause / Step / Reset**: Control playback through 49 fixed frames
- **Drag on beam**: Rotates camera orbit (touch/mouse)
- **Keyboard**: All controls are focusable and operable by keyboard

## Provenance

- **Paper**: [Bi-FORK](https://arxiv.org/html/2610.12449) by Anna Zimmel, Fleur Hendriks, Markus Holzleitner, Florian Sestak, Martin Weichselbaumer, Vlado Menkovski and Johannes Brandstetter (CC BY 4.0)
- **Implementation**: Locally generated toy trajectories using a declared sine-mode beam rule with 33 material points, 49 frames, and 9 fixed seeds
- **Notice**: Equations and values are illustrative; this is not Bi-FORK output, validated mechanics, or evidence about real branch likelihoods
- **License**: This independent toy is released under MIT License. Third-party code: none.

## Accessibility

- Respects `prefers-reduced-motion`: auto-play pauses by default for reduced-motion users
- Full keyboard navigation with visible focus indicators
- ARIA labels and live regions for screen readers
- System fonts, capped device pixel ratio (2×), no sound, no runtime network, no personal data