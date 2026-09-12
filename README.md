# Contagion Corridor

A browser-based, first-person 3D survival horror prototype built with [Three.js](https://threejs.org/). A rat-borne outbreak turns a school into a maze of infected students — fight or flee through procedurally generated corridors across 100 escalating levels.

No installs, no build step, no external assets. It's a single self-contained HTML file that runs directly in any modern browser, desktop or mobile.

> ⚠️ **Educational / prototype project.** Built to explore game-dev concepts in Three.js (3D rendering, procedural generation, real-time audio synthesis). Not a commercial release, and not affiliated with or a copy of any existing commercial game.

---

## Play it

Just open [`zombie-school-prototype.html`](./zombie-school-prototype.html) in a browser — no server, no dependencies, no build process required.

- **Desktop:** double-click the file, or drag it into a Chrome/Edge/Firefox tab.
- **Mobile:** open the file directly in your phone's browser. On-screen touch controls appear automatically.

> Note: some in-app browsers / embedded preview panes block WebGL and mouse-lock. If the game doesn't seem to respond, open the file in a full standalone browser tab.

## Controls

| Action | Desktop | Mobile |
|---|---|---|
| Move forward | `W` / `↑` | ▲ button |
| Move back | `S` / `↓` | ▼ button |
| Turn left | `A` / `←` | ◀ button |
| Turn right | `D` / `→` | ▶ button |
| Shoot | `Space` or mouse click | FIRE button |
| Sprint | `Shift` | — |
| Look around (optional) | Mouse (if pointer-lock works) | — |

## Story

A rat bit one student in Biology. It didn't stay contained. Every other student in the school is turning. Move through the classroom, reach the lab, arm yourself, and get out through the exit before they catch you — 100 times, each level tighter and faster than the last.

## Features

- First-person 3D movement and combat, no plugins or installs
- Procedurally generated levels — layout, zombie count, zombie speed, and ammo all scale with level number via a seeded generator (same level always generates the same layout)
- 5 rotating environment themes that cycle every 20 levels: Classroom Wing, Gymnasium, Cafeteria, Science Labs, Auditorium
- Three zombie types (fast / slow / normal) with distinct speed, size, and color tinting
- Jointed low-poly humanoid zombie rigs (hips, knees, shoulders, elbows) with walk-cycle animation
- Real-time shadows, dynamic point lighting, and procedurally generated (canvas-based) floor/wall textures — no external image or model assets
- Fully synthesized audio via the Web Audio API — ambient drone, footsteps, gunshots, growls, heartbeat — no external sound files
- On-screen touch controls that auto-appear on mobile/tablet devices
- Level-clear / game-over flow with retry and level progression

## Tech

- [Three.js r128](https://threejs.org/) (loaded via CDN)
- Vanilla JavaScript, no build tooling or frameworks
- Web Audio API for all sound (synthesized, not sampled)
- Everything — geometry, textures, audio — is generated procedurally at runtime; there are no binary/image/audio asset files in this repo

## Known limitations

This is a solo prototype, not a polished game:
- Characters are built from primitive geometry (cylinders/spheres/boxes), not sculpted or rigged character models
- No save system — progress resets when you close the tab
- Balance (zombie speed/damage/ammo curves) is a first pass, not extensively playtested
- Level layouts are algorithmically generated corridors, not hand-designed rooms

## Contributing / license

Feel free to fork and experiment. This project doesn't currently specify a license — add one (e.g. MIT) if you intend to reuse or distribute the code.
