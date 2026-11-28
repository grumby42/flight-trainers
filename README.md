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
- Worlds: Zephyr Valley (Air Work drills + scenic soaring), straight-in, power-off 180 (0 to +200 ft), mountain spiral at 6,800 ft density altitude, short field over pines (0 to +100 ft), lava caldera, Rainbow Tunnel (thread a warp tunnel, break out through clouds), Crosswind County (real runway, random gusty crosswind, power-off 180, scored on drift and nose alignment), 3-island hop, Engine Out! (random failure from cruise) and Cloud Kingdom (Zen free flight).
- Lessons: each world has a mastery ladder; stages pass on repetition (3 in a row or 3 of last 4), and the checkride needs 2 in a row. Air Work (best-glide hold, trim, slow flight, approach & flare at altitude) unlocks Mallard Meadow, which unlocks the rest.
- Fix-it drills: recurring errors (too fast, hard, long/short, drift, crab, off the trail...) are logged across flights; when one repeats in at least half of your recent flights, a drill isolates it — the autopilot flies the controls you have down and leaves you only the one to fix (pitch only, pitch below 30 ft, bank + rudder, or flaps + slip). Pass 3 in a row.
- "Is it you or the level?": every debrief checks the error against the level's demands — energy budget vs what the duck can burn, float distance, where you crossed 20 ft, gusts, and crosswind vs the airplane's maximum demonstrated value. Bread trails end at an aim point about one float-distance short of the spot.
- Instructor mode: build a scenario (world, duck, wind, failure height and cause, note) and share it as a link that opens straight into the briefing.
- Instruments: G1000-style speed and altitude tapes, CFI-duck wingman with spoken callouts, chase / duck-eye / tower cameras, and an approach-plate profile view (tap the minimap).
- Ducks: Mallard 172 (Cessna 172S numbers: Vg 68, about 9:1), Pintail Archer (Piper PA-28-181 numbers: Vg 76, about 10:1), Teal Cub (no flaps, so slip), Glider Goose (sailplane, airbrakes).
- Point-mass lift/drag physics with stall, ISA density, ground effect, flaps/slip drag, gusts, thermals and ridge lift.
- Model limits (read before using it with students): Mallard numbers match the Cessna 172S POH at 2,550 lb (Vg 68, Vs1 48, Vs0 40 KIAS, about 9:1, approach speeds 65 / 63 / 61 KIAS). Speeds are shown as KIAS with no instrument or position error. The stall horn sounds about 5–6 kt above stall. There are no pitch dynamics or flap balloon. Rudder creates real sideslip (side force and drag), so crab and wing-low crosswind technique works, but there is no yaw/roll coupling or gear cornering. Water stands in for a runway (not seaplane technique). Auto-trim is a game aid and is off for checkrides. The engine-out restart checklist follows the C172S POH order (airspeed 68, fuel shutoff ON, selector BOTH, aux pump ON, mixture RICH, ignition BOTH/START); failure causes are simplified. Tolerances follow the Commercial ACS (power-off 180: 0 to +200 ft; short field: 0 to +100 ft; slow flight just above the stall warning). The game supplements dual instruction and the POH; it doesn't replace them.
- Build `DUCK-YYYYMMDD-HHMMZ` is stamped in the menu, pause and results screens and in the page's meta tags.

## Self-hosted libraries (`vendor/`)
No page loads code or fonts from a CDN. `vendor/` holds three.js r128 (MIT), Leaflet 1.9.4 (BSD-2-Clause), and the Oswald and Share Tech Mono fonts (SIL OFL), taken from their npm packages with licences alongside. The panel trainer still fetches map tiles and METARs at run time.

## Review status
All trainers had a CFI / DPE / FAA-style content review on 2026-11-23 (build 2026-11-23T18:54:31Z for the four smaller tools). They are concept demonstrators with tuned magnitudes: use the POH/AFM and the ACS for numbers.
