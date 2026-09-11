# Website3D — Crystal Worlds

A single-file, self-contained Three.js scene: an infinite scroll journey through four
worlds — Star → Moon → Sun → Earth — each rendered with its own procedural shader and
revealed by real page scroll (no library beyond Three.js r134 from a CDN).

## Run it

Just open `index.html` in a browser, or serve the folder and visit it — no build step,
no dependencies to install.

## Controls

- **Scroll** — travel deeper into the next world (loops forever: after Earth it returns
  to the Star).
- **Drag** — rotate the current world.
- **‹ › buttons / arrow keys** — jump to the previous/next world.
- **♪ sound** — optional synthesized ambient drone (Web Audio API).

## Tech

- Three.js (WebGLRenderer, custom `ShaderMaterial`s — no external textures, everything
  is procedural noise/fbm in GLSL).
- Real, native page scroll drives a continuous "world position," smoothed and
  rate-limited so the reveal paces itself regardless of scroll speed.
- No build tooling — it's one HTML file.
