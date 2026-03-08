# mediaLab2 — VR Point Cloud Explorer

A-Frame based Virtual Reality application with an interactive HUD control panel.

---

## Browser Compatibility

Tested and working on:

| Browser | Version | Result |
|---|---|---|
| Google Chrome | 123.0.6312.86 | Full support |
| Mozilla Firefox | 124.0.1 | Full support |

> **Note:** Requires a local web server to load `.ply` assets due to CORS restrictions.
> Recommended: VS Code **Live Server** extension, or `python3 -m http.server 8080`.

---

## Features Implemented

### 1. Rotation Control Panel
- Rotate the point cloud on X, Y, Z axes (15 deg steps)
- **Auto-rotate** toggle: smoothly spins the model on the Y axis

### 2. Move / Shift Controls
- Arrow pad to shift the model left, right, up, down, forward, backward
- Home button resets position

### 3. Scale / Zoom Controls
- Zoom In / Zoom Out buttons (20% per step)
- **Point Size slider** – adjusts point cloud point size in real time
- **Light Intensity slider** – adjusts the main light in real time

### 4. Object Controls
- **Hide / Show toggle** – toggles model visibility
- **Color Cycle** – cycles through 6 accent colors
- **Grid toggle** – turns the wireframe floor on/off
- **Reset All** – restores all transforms to defaults

### 5. HUD Status Panel
- Semi-transparent cyberpunk-styled overlay
- Status bar shows last action
- **[ HUD ]** button hides/shows the entire panel

---

## A-Frame Version

Updated from **0.6.0 to 1.5.0**:

```html
<script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
```

---

## Models Used

Only **Sphere.ply** is used (sculpt.ply removed). Background is a custom deep-space environment:
- Dark navy sky
- Procedural star field (emissive spheres)
- Nebula backdrop plane
- Wireframe grid floor
- Blue + magenta point lights

---

## Running Locally

```bash
# Python (built-in)
cd aframe/
python3 -m http.server 8080
# Open http://localhost:8080

# VS Code: right-click index.html -> "Open with Live Server"
```

---

## Controls (In-Scene)

| Action | Input |
|---|---|
| Look around | Mouse drag |
| Walk | W / A / S / D |
| Rotate model | Control panel |
| Move model | Arrow pad |
| Zoom | +/- buttons |
| Auto-rotate | AUTO button |
