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

**P/C Pocket Trainer notes**
- Add `?selftest` to the URL to run the built-in invariant checks on-device.
- Free flight: Settings → TILT YOKE turns the phone into a yoke. Turn it like a wheel to roll; tilt the top away from or toward you for pitch. The d-pad left/right buttons become rudder pedals.
- This is a ground-based cognitive training aid. It does not replace flight instruction, the POH, or the ACS.
