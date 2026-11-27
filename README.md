# flight-trainers

Single-file, offline-capable HTML flight-training tools. GitHub Pages serves them over HTTPS, which phone motion sensors require.

| File | Tool |
|---|---|
| `index.html` | Landing page |
| `archer-trainer.html` | Archer control-surface trainer (CFI) |
| `twin-trainer.html` | Twin: Vmc and critical engine (MEI) |
| `panel-trainer.html` | Six-pack and compass errors (phone sensors) |
| `compass-errors.html` | Whiskey compass errors (standalone) |
| `pc-pocket-trainer.html` | P/C Pocket Trainer: commercial ASEL checkride prep for the PA-28-181 (FAA-S-ACS-7B, POH VB-2960) |
| `duck-glide.html` | Duck Glide: 3-D engine-out glide and accuracy-landing game, phone tilt controlled (8 worlds, replay) |

**P/C Pocket Trainer notes**
- Add `?selftest` to the URL to run the built-in invariant checks on-device.
- Free flight: Settings → TILT YOKE turns the phone into a yoke. Turn it like a wheel to roll; tilt the top away from or toward you for pitch. The d-pad left/right buttons become rudder pedals.
- This is a ground-based cognitive training aid. It does not replace flight instruction, the POH, or the ACS.

**Duck Glide notes**
- Worlds: straight-in, power-off 180 (0 to +200 ft), mountain spiral at 6,800 ft density altitude, short field over pines (0 to +100 ft), lava caldera, 3-island hop, Engine Out! (random failure from cruise) and Cloud Kingdom (Zen free flight).
- Ducks: Mallard 172 (C172-like glide, about 9:1, Vg 63 KIAS), Teal Cub (no flaps, so slip), Glider Goose (sailplane, airbrakes).
- Point-mass lift/drag physics with stall, ISA density, ground effect, flaps/slip drag, gusts, thermals and ridge lift. Tuned to be realistic, but it's a game: use the POH for numbers.
- Build `DUCK-YYYYMMDD-HHMMZ` is stamped in the menu, pause and results screens and in the page's meta tags.

## Self-hosted libraries (`vendor/`)
No page loads code or fonts from a CDN. `vendor/` holds three.js r128 (MIT), Leaflet 1.9.4 (BSD-2-Clause), and the Oswald and Share Tech Mono fonts (SIL OFL), taken from their npm packages with licences alongside. The panel trainer still fetches map tiles and METARs at run time.

## Review status
All trainers had a CFI / DPE / FAA-style content review on 2026-11-23 (build 2026-11-23T18:54:31Z for the four smaller tools). They are concept demonstrators with tuned magnitudes: use the POH/AFM and the ACS for numbers.
