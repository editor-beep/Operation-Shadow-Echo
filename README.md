# Operation: Shadow Echo — Spatial Ops Map

A living, draggable constellation of black ops, sanity-draining nodes, and mythic
layers. The terminal log evolved into a spatial ThoughtMap — a leaked CIA black
site you can pan, zoom, and unravel. Retro CRT / VT323 aesthetic, scanlines,
glitch, and creeping paranoia.

> **ALL OF IT IS REAL.**

## Features

- **Infinite canvas** — pan (drag), zoom (scroll / pinch), fit-to-view.
- **Draggable ops nodes** — MKULTRA, Monarch, Blue Beam, St. Louis, Chemtrails,
  Presidential Models, and more. Positions persist in `localStorage`.
- **Custom retro nodes** — glitch on hover, per-node sanity-drain bars, color-coded
  by type (op / doc / handler / recover / terminal).
- **Signal-line edges** — animated dashed "redacted" connections with classified labels.
- **Sanity meter** — global drain/recovery. Each node you open costs sanity;
  the **Safehouse** restores it. Passive bleed over time. Hit zero and the CRT bleeds red.
- **The Handler** — open an encrypted chat channel and transmit queries for answers.
- **Paranoia events** — random environmental dread triggered by interaction.
- **Document viewer** — classified memos pulled from the lore, with redaction styling.
- **Layer toggle** — `SURFACE → DEEP STATE → MYTHIC`. Filter the constellation by reality layer.
- **TRANSMIT** — export the current map state + connections as a JSON field report.
- **Signal audio** — toggleable procedural Web Audio bed (low detuned drone +
  band-passed static hiss) with teletype clicks on node open, handler-channel
  beeps, and static stings on paranoia events. The bed reacts to sanity: as it
  falls the hiss swells, the drone muddies and detunes, and a waveshaper bites
  in — hitting zero triggers a panic collapse. Autoplay-safe (nothing sounds
  until you enable it); the on/off preference persists in `localStorage`.

## Tech

Zero-dependency, single-file `index.html`. Pure JS + SVG. No build step, no
`node_modules` — deploys to Vercel as a static site exactly as before.

## Run / Deploy

```bash
# locally — just open it
open index.html        # (or serve the folder with any static server)

# Vercel — static deploy, see vercel.json
vercel
```

## Lore

Narrative seed data lives in `messages.json` and inline in `index.html` (the
`NODES` / `EDGES` arrays). Add nodes by pushing to those arrays — `layer`,
`type`, `x`, `y`, `drain`, `title`, `sub`, and a `doc` (or `chat`) payload.

## Roadmap

- Custom node typewriter reveal + per-node scanline overlays
- Add-node-on-the-fly authoring ("unhoused words" publishing)
- ~~Audio: teletype + static bed~~ ✓ shipped
- Audio next: `AnalyserNode`-driven glitch sync, WaveShaper escalation tuning
- Next.js + React Flow migration for shared "leaks" via Supabase
