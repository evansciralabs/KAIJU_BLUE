# KAIJU-BLUE // DREAD ORGAN

A single-file kaiju sound-design instrument. A dread organ that lives entirely in one `index.html` — no dependencies, no build step, no network calls. Open it and play.

**Play it. Bounce it. Share it.**

## What it is

KAIJU-BLUE is a browser instrument built on the Web Audio API. Each kaiju plate is a voice: a named preset (ABYSS CALL, HOLLOW CHOIR, IRON DREAD, SUNKEN BELLS, ASH CATHEDRAL, FROZEN MAW, SIREN GRID, RADIANT BURN, …) with its own patch of oscillators, formant/vowel shaping, granular growl, ring modulation, crushing, echo, and reverb. A radar-style scope tracks your signal as you play — range, bearing, tail, and voice count — and goes hot when the patch runs away.

## Features

- **Single file.** The whole app — UI, engine, presets, fonts, favicon — ships in one `index.html`.
- **Four-panel interface.** `PLAY` / `TONE` / `FX` / `OUT` tabs with draggable hex knobs and the full keyboard (octave up/down, HOLD, PANIC).
- **24 kaiju plates.** Named patch presets (`K-01` … `K-24`), each with its own plate art and signal signature.
- **Performance pads.** One-shot hits and a bounce recorder that renders your take to a downloadable audio file.
- **Radar scope HUD.** Live signal analysis — range, bearing, tail length, voice count, RUNAWAY/FLUSH warnings.
- **Zero dependencies.** No CDN, no framework, no assets fetched from the network (plate JPGs are local).
- **It remembers you.** Patch state persists in `localStorage`.
- **Considerate.** Reduced-motion and high-contrast support, ARIA labels, keyboard focus states, safe-area aware layout for phones.

## Run it

### Locally

Double-click `index.html`. That's it. (Any static file server works too: `python3 -m http.server`.)

### GitHub Pages

This repo publishes itself: Settings → Pages → Deploy from branch → `main` / `(root)`.

## Plate art

The app expects `1.jpg` … `24.jpg` (unpadded, lowercase) in the same directory as `index.html`. Missing plates are tolerated — the HUD keeps running — but the organ wants its kaiju.

## Free to use — including commercially

KAIJU-BLUE is MIT-licensed. Sound designers and studios: use it to craft sounds for commercial releases, embed it in your toolchain, modify it, ship it. No permission needed, no fee. The only requirement is that the LICENSE file travels with the code — that's where the credit lives.

**Credits & shout-outs.** If KAIJU-BLUE ends up in something you made, a mention is always appreciated — tag it, star the repo, or drop a link back. Not required. Just good energy.

## Browser support

Modern browsers with Web Audio (Chrome, Edge, Firefox, Safari). Audio starts after your first interaction — browsers require a gesture to unlock sound; the power button in the corner is the ignition.

## License

MIT — © 2026 Evanscira Labs.
