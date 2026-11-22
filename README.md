# HOLOMAP — Commander / Recon

A sci-fi holographic terrain projector you can play in the browser. Plan routes, mark hostiles, and sneak a figure into a hostile outpost. In v3 the map is much larger, you can switch between orbit, third person, first person, and a 2D tactical map, and two people can share a live session so one of you can command while the other walks the ground.

**Play it:** [https://deli6767.github.io/holo-map/](https://deli6767.github.io/holo-map/)

## Play together (Commander + Recon)

This is built for a guide and a field agent on two devices — a laptop or tablet for the commander, a phone for the recon. You need an internet connection so the free PeerJS broker can introduce the two browsers; after that the drawing and movement sync peer-to-peer.

**Delon (Commander) — host the room**

1. Open [https://deli6767.github.io/holo-map/](https://deli6767.github.io/holo-map/).
2. Tap **Host (Commander)**. A short room code appears (for example `K7M3P`).
3. Tap **Copy code** or **Copy link** and send it to your brother. The link looks like `https://deli6767.github.io/holo-map/?join=K7M3P`.
4. Draw paths, drop enemy beacons, and ping spots. He sees those appear live on his device.

**Brother (Recon) — join**

1. Open the share link, **or** open the same site, tap **Join (Recon)**, type the code, and tap **Join**.
2. When the status says **LINKED**, you are in. Switch to **2D map**, **3rd**, or **1st** with the buttons on the right (or press **V** / **C**).
3. Walk with the on-screen joystick (phone) or WASD. You will see Delon’s gold figure, and he will see yours (cyan-green).

Either of you can draw (commander paths are **gold**, recon paths are **cyan-green**) and move your own figure. Only the commander can generate **New terrain** — both of you then load the same map (the terrain seed is synced).

**Solo** is the default: skip Host/Join and use the map by yourself.

If the link fails, you will get a clear message. Check that both devices are online, try another network (some VPNs and locked-down networks block WebRTC), or stay in Solo.

## Camera / view modes

Toggle with the **Orbit / 3rd / 1st / 2D map** buttons, or press **V** or **C** to cycle.

| View | What it is | Move / look |
| --- | --- | --- |
| **Orbit** | Tabletop hologram, current default | Left-drag to spin, scroll/pinch to zoom |
| **3rd** | Chase camera behind your figure | WASD or joystick to move; drag (or mouse-look) to turn |
| **1st** | Eye-level, with a reticle | Desktop: click the view to lock the pointer, mouse-look, WASD. Phone: drag the right side of the screen to look, joystick to move |
| **2D map** | Orthographic, north-up tactical map | Drag to pan, scroll to zoom. Shows paths, enemy markers, both figures, and the base |

In every view the world keeps the hologram look: glowing contour terrain, drawn paths as lit lines on the ground, and enemy markers as red beacons you can pick out from far away.

## Mission

Infiltrate the red enemy base, grab all four intel/crates, and get back to the green **extraction** pad without being seen.

- Patrolling guards have **vision cones** on the ground. Stay in a cone for a moment and you are **DETECTED** — you lose a life and reset to extraction.
- You have **3 lives**. Walk over loot (or press **E**) to pick it up. The HUD tracks `LOOT X/4`.
- Walls block movement; use the **gate**.
- Extract with all loot for **MISSION COMPLETE**.
- **Restart mission** starts the run over on the same terrain. **New terrain** (or **R**) builds a fresh mountain and relocates the base (commander only in a linked session).

The world is several times larger than before, with the original infiltration base plus a few extra landmarks. Fog hides the far edge.

## Controls

| Input | Action |
| --- | --- |
| V / C | Cycle view mode |
| Left-drag (Orbit) | Orbit the table |
| Scroll / pinch | Zoom (orbit or 2D map) |
| Right-drag | Draw a planning path (arrow on release) |
| Double-click / long-press / P | Ping a spot (pulse + sound). In 1st/3rd, P pings where you are looking |
| WASD / arrows / joystick | Move your figure |
| Mouse-look / drag | Turn in 1st and 3rd |
| Click in **Move** mode | Walk to that point (not in 1st person) |
| Shift | Sprint |
| E | Pick up nearby loot |
| 1–4 | View / Draw / Place enemy / Move |
| Z | Undo last path |
| R | New terrain (commander) |

On a phone, the view-mode buttons stay large, the joystick sits in the lower left, and you can play in portrait or landscape. Turn on **Draw** to trace a path with one finger. **Place enemy** drops a red beacon; tap a beacon to remove it.

## Status

The top bar shows **SOLO**, **HOSTING** + the room code, **CONNECTING…**, **LINKED**, **RECONNECTING…**, or **LINK FAILED**. Use **Leave** to drop back to solo.
