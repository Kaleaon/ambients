# Ambients — a myNoise-style ambient generator

A web ambient generator that works like [myNoise.net](https://mynoise.net): every soundscape is built from **10 separate layers**, each on its own vertical fader, so you shape the mix yourself instead of playing a fixed loop.

Live version is built as a Muse web artifact (slug: `ambient-generator`). This repo is the saved source: a single self-contained `index.html` plus photo assets under `assets/`. Open `index.html` in a browser — no build step, no server needed.

## Soundscapes (v2 — 13 total)

- Rain on Leaves
- Ocean Waves
- Forest & Birds
- Crackling Fire
- Mountain Stream
- Summer Night
- Thunderstorm
- Pure Noise (spectrum mixer)
- Japanese Garden — with shishi-odoshi
- Train Journey
- Rainy Day Café
- Blizzard Cabin
- Drone & Tones — with a binaural pair

Each soundscape has 10 channels and 5 presets, and its fader settings are remembered while you switch between scenes.

## How it works

- All sound is synthesized live with the **Web Audio API** — no audio files, no loops.
  - Filtered white / pink / brown noise for the continuous layers
  - LFO swells for surf, wandering bandpass filters for wind
  - Randomly-timed synthesized events: thunder, birdsong, crickets, fire crackles, droplets, frogs, owls, gulls, shishi-odoshi — so no scene ever repeats exactly
- **10 vertical faders per scene** — tap a channel name to mute just that layer, double-click a channel to solo it
- **Stacking** — stack a second generator on top of the first, with its own level control
- **Calibration EQ** — a global 6-band calibration EQ with presets: small speakers, highs lift, warm & dark, and tinnitus notch
- **Animate mode** — faders drift on their own, now with 3 modes: Drift, Wave, and Breathe
- **Presets, Flat / Random Mix / Mute All**, master volume with smooth fades
- **Sleep timer** that fades out at the end, plus a meditation bell every 5 min
- **Category filters + Surprise Me** to browse and discover soundscapes
- **Live spectrum visualizer**
- **Save Mix / Copy Mix** settings for the session — and load a mix back by pasting Copy Mix text

## Files

- `index.html` — the whole app (HTML/CSS/JS, Web Audio engine)
- `assets/*.jpg` — hero photos for each soundscape

## License

See `LICENSE` in this repo.
