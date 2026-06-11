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
- **FOIA trail** — every dossier carries a *filed-requests* footer linking the real,
  public record. Programs that genuinely declassified (MKULTRA, the St. Louis zinc
  cadmium sulfide tests) link straight to the CIA Reading Room, the 1977 Senate
  hearing, and the National Academies review with a `DECLASSIFIED` badge. The
  purely-mythic nodes (Monarch, Blue Beam) instead show a `REQUEST DENIED` dead-end —
  honest about where the paper trail actually stops, and on-theme about the silence.
  A dedicated **FOIA VAULT** node hubs the real archives (CIA Reading Room, National
  Security Archive, The Black Vault, the JFK records, FOIA.gov).
- **Clearance progression** — a single-player ARG loop layered over the map.
  Recovering documents raises your **CLEARANCE** (`Lv.1 SURFACE → Lv.2 DEEP STATE →
  Lv.3 MYTHIC`). The MYTHIC nodes stay `▓▓ ENCRYPTED ▓▓` until you earn Lv.2 —
  reach it and the arcana overlay decrypts live.
- **Leaked-files counter** — a persistent `DOCUMENTS X/Y RECOVERED` HUD tracking
  every dossier you've opened.
- **Fuse signals (player-made connections)** — arm `⊕ FUSE`, pick a source node's
  `⊕` handle, then a target, to draw your own edge. Hitting a **real pattern**
  (MKULTRA→MONARCH, BLUE BEAM→TAROT, …) reveals hidden lore and restores sanity;
  forcing a meaningless link is a paranoia gamble that can spike or drain you.
  Fused edges render as cyan dashed signal-lines distinct from the canon edges.
- **Handler Directives** — a live mission panel (top-left). Recover N documents,
  fuse specific patterns, reach the Safehouse, open the FINAL TRANSMISSION. Each
  completion pays out sanity and/or progression.
- **Branching endgame** — opening the FINAL TRANSMISSION (or hitting zero sanity)
  ends the run with one of four outcomes — `ABSORBED`, `THE ARCHIVIST`,
  `THE WHISTLEBLOWER`, `THE FORGOTTEN` — chosen from documents recovered,
  patterns fused, and final sanity, with a full stat readout. `REBOOT` to replay.
- **Paranoia decision events** — timed forced choices ("a black SUV idles
  outside…") where each option is a sanity gamble. More frequent as sanity falls.
- **Escalating dread** — a sanity-reactive canvas overlay layers static grain, a
  red haze, and shadowy figures creeping in at the edges as you slip. The audio
  bed gains low-sanity *whispers* (band-passed, LFO-wobbled "voice" oscillators).
- **INTEL economy (v6.0)** — a score currency layered over everything. First-time
  recoveries, decrypted intercepts, verified records, locked fusion patterns and
  signal chains all bank INTEL; a persistent HUD counter tracks it, and your best
  haul survives reboots.
- **Signal chains (v6.0)** — recover two *connected* dossiers back-to-back
  (within 25s) and a `SIGNAL CHAIN ×N` multiplier fires: escalating intel bonuses
  and a sanity kickback for following the thread instead of clicking at random.
- **Encrypted intercepts (v6.0)** — periodic captured transmissions arrive as
  Caesar/ROT cipher puzzles. Dial the rotation until the traffic reads clean and
  lock it for intel + sanity; every plaintext is a *true* line from the record
  (Helms's 1973 burn order, the 1994 St. Louis confirmation, the FOIA clock…)
  with a follow-up note — plus a footnote on why ROT-N falls to patience and why
  real tradecraft moved to one-time pads. Wrong locks and burned intercepts cost.
- **Field verification (v6.0)** — dossiers with a real public record carry a
  `▸ VERIFY THE RECORD` check: one factual multiple-choice question (When did the
  Army confirm St. Louis? How did the MKULTRA pages survive? Where does Blue Beam
  actually come from?). Right or wrong, you get the sourced answer — the
  educational layer pays intel for actually reading.
- **The Handler answers back (v6.0)** — the encrypted channel now has a typed
  query line. A keyword brain responds in character about MKULTRA, Monarch,
  Blue Beam, St. Louis, FOIA, your progress, your sanity — with live state woven
  into hints. Off-record questions get static.
- **Typewriter dossiers (v6.0)** — documents teletype in line-by-line (click to
  skip), synced to the audio clicks.
- **Run meta-progression (v6.0)** — runs, best intel, and endings seen persist
  *across* reboots. The endgame readout shows your career: `RUN #3 · BEST INTEL
  240 · ENDINGS SEEN 2/4`.
- **Corrupted dossiers (v6.0)** — from run 2 onward, one undiscovered file comes
  back wrong: magenta flicker, double sanity drain, double intel. Replay tension.
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

A node may also carry a `sources` array — its FOIA trail. Each entry is one of:

```js
{ s:'open',    label, url, note? }  // real, declassified, links out with a DECLASSIFIED badge
{ s:'partial', label, url?, note? } // released but redacted / fragmentary
{ s:'denied',  label }              // no responsive records (or never existed) — REQUEST DENIED
```

Keep the `open`/`partial` links honest: only point real declassified URLs at nodes
that actually have a public record. Fictional programs get `denied`.

## Roadmap

- Add-node-on-the-fly authoring ("unhoused words" publishing)
- ~~Audio: teletype + static bed~~ ✓ shipped
- ~~FOIA trail: real declassified-document links per node~~ ✓ shipped
- ~~Game loop: clearance progression, fuse-signal connections, handler
  directives, branching endgame, paranoia decisions, dread overlay~~ ✓ shipped (v5.0)
- ~~Typewriter dossier reveal~~ ✓ shipped (v6.0)
- ~~Multi-run "corrupted node" replay tension~~ ✓ shipped (v6.0)
- ~~More fusion patterns~~ ✓ shipped (v6.0 — 16 total)
- ~~Sticky loop: INTEL economy, signal chains, cipher intercepts, field
  verification quizzes, conversational Handler, career meta-progression~~ ✓ shipped (v6.0)
- Audio next: `AnalyserNode`-driven glitch sync, WaveShaper escalation tuning
- FOIA next: in-modal document preview pane, per-node request-status timeline
- Game next: procedurally-generated nodes from chains, PNG export of field
  reports, daily intercept rotation, leaderboard via Supabase
- Next.js + React Flow migration for shared "leaks" via Supabase
