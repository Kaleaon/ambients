# Ambients — a myNoise-style ambient generator

A web ambient generator that works like [myNoise.net](https://mynoise.net): every soundscape is built from **10 separate layers**, each on its own vertical fader, so you shape the mix yourself instead of playing a fixed loop.

Live site: **https://kaleaon.github.io/ambients/** (served from `docs/` via GitHub Pages). The app is also built as a Muse web artifact (slug: `ambient-generator`). This repo is the saved source: a single self-contained `index.html` plus photo assets under `assets/`. Open `index.html` in a browser — no build step, no server needed.

## What's in v3 — 670 generators, 20 categories

A procedural generator factory expands the original 13 hand-built scenes into **670 generators across myNoise's 20 categories** — Natural, Landscapes, Ambiences, Synthesizers, Tonal Drones, Transports, Urban, Industrial, Experimental, Magic, and more — grouped by use case (Sleep, Focus, Relaxation, Meditation, Tinnitus…). Every generator has 10 channels, 5+ presets (including spectral curves: Brown / Pink / White / Grey / Speech Blocker, plus Surprise!), keyword search, star **Favorites** with a Your Favorites view, and Recently Added / Site Favorites shelves.

Highlights of the hand-built scenes, all still here: Rain on Leaves, Ocean Waves, Forest & Birds, Crackling Fire, Mountain Stream, Summer Night, Thunderstorm, Japanese Garden (working shishi-odoshi), Train Journey, Rainy Day Café, Blizzard Cabin, Drone & Tones — plus designer-led additions like Industrial Drone, Desert / Dunes, Near Silence, and a Binaural Beats lab with Delta→Gamma quick-picks.

## How it works

- All sound is synthesized live with the **Web Audio API** — no audio files, no loops.
  - Pink / brown noise beds with wandering bandpass voices (a stream that babbles, not hisses), granular rain, generated-impulse convolution reverb per scene
  - Thunder is an *event*, never a layer: randomized strikes with sub-bass drops; beds duck under hero events (sidechain)
  - Randomly-timed synthesized events: birdsong, crickets, fire crackles, droplets, frogs, owls, gulls, shishi-odoshi — so no scene ever repeats exactly
- **Calibration** — a real 10-band (31 Hz–16 kHz) personal hearing calibration with threshold and equal-loudness variants; your curve is saved locally and applied via iEQ None / Balanced / Full. Control Panel holds global defaults (level, stereo width, iEQ, theme).
- **Animate mode** — faders drift on their own: Soft / Hard, Solo / Duo / Trio / Quad grouping, speeds ÷8–×8, adjustable Low / High range.
- **Collect → Composite** — collect individual sliders across generators (up to 10) and render your own composite generator, alongside whole-scene stacking.
- **Sharing** — mixes encode into the URL (auto-loads on open), Save in Browser (named local mixes), JSON export / import, Mini-Player mode, and a **free Render & Download WAV** (~60 s render) — no credits, no paywall.
- **Timers** — sleep timer with fade, Meditation Timer, Pomodoro, and a meditation bell.
- **Player extras** — Stereo Width (Mono / Narrow / Normal / Wide), Tape Speed, tonal transpose + Remix, 432 Hz toggle, spectrum analyzer with frequency cursor, and a full keyboard-shortcut set with a Help overlay.

## Files

- `index.html` — the whole app (HTML/CSS/JS, Web Audio engine)
- `assets/*.jpg` — hero photos for the hand-built soundscapes
- `docs/` — an exact copy of the app, served by GitHub Pages

## License

See `LICENSE` in this repo.
