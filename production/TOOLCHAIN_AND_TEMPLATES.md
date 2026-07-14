# Toolchain & Templates — Mode of Failure

**Phase 10 deliverable · 2026-07-13 · Pairs with `production/PRODUCTION_SOP.md`.** Constraint: owner budget **≤$100/mo tooling** (`logs/DECISION_LOG.md` D-005). Design principle: **free-first** — every pipeline stage runs at $0/mo on the launch stack; paid upgrades are listed with the specific problem each one buys out of, and even the everything-on stack stays under the cap.

**Pricing honesty note:** vendor pricing pages could not be fetched from this environment (403 via proxy — same limitation logged in `research/validation/probe-monetization-policy-status.md`, method caveats). All prices below are **estimates from general market knowledge as of early 2026, labeled [est.] — verify each at purchase**. The budget math therefore includes a safety margin: even if every [est.] runs 25% high, the recommended stack stays under $75/mo.

---

## 1. The tool stack + monthly cost table

### 1.1 Recurring monthly costs

| Function | Launch choice (free-first) | $/mo | Paid upgrade (what it buys) | Upgrade $/mo [est.] |
|---|---|---:|---|---:|
| Video editing | **DaVinci Resolve (free version)** — full NLE, Fairlight audio, loudness metering, 1080p+ export | 0 | DaVinci Resolve Studio — **$295 one-time** [est.], not monthly; buys noise-reduction FX and GPU encode speed. Not needed at launch | 0 |
| Diagrams / brand graphics | **Inkscape** (free, open-source SVG) — the diagram template kit lives here | 0 | Affinity Designer 2 — ~$70 **one-time** [est.]; snappier canvas on big files. Optional forever | 0 |
| Photo prep (archival stills) | **GIMP** (free) — crop/level/restore within gate-3 limits | 0 | — | 0 |
| Thumbnails | Same Inkscape template (§3.6) | 0 | Figma free tier as alternative; paid tier unnecessary for 1 user | 0 |
| Audio record/edit | **Audacity** (free) — full SOP-6 chain (NR, EQ, compressor, LUFS normalize) | 0 | REAPER — $60 **one-time** discounted license [est.]; punch-and-roll recording, faster comping | 0 |
| Music & SFX bed | **YouTube Audio Library** (free, license terms per-track, downloadable license receipt) + Pixabay Audio (free, license per-track) | 0 | **Epidemic Sound Personal** ~$18/mo [est.] or Artlist ~$15/mo [est.] — one library, one blanket license row in every manifest, better bed consistency. Recommended from first revenue, not before | 18 |
| Captions/transcription | YouTube auto-captions corrected against script; or local **Whisper** (free, open-source) | 0 | — | 0 |
| AI assistance (prompt library §1–§8) | **Claude Pro** ~$20/mo [est.] — runs the report-digest/outline/draft/fact-check/diagram-brief prompts. This is the one paid tool in the launch stack: the ≤10h budget depends on the prompt library (engine §b), so it is load-bearing, not optional | 20 | Higher API/Max tiers unnecessary at 1 video/week | 20 |
| Project management + dashboard | **Google Sheets** (free) — the kill-switch dashboard is specced as a sheet (engine §e); one tab doubles as the topic log | 0 | Notion free tier if preferred; $0 either way | 0 |
| Timer (hours audit) | Phone timer or **Toggl Track free tier** | 0 | — | 0 |
| Offsite backup (SOP-10 copy 3) | **Google Drive free 15 GB** — covers scripts, source packs, manifests, license evidence, diagram SVGs (the irreplaceable small files). Video masters ride Copy 2 (local drive) at launch | 0 | **Backblaze Personal Backup** ~$9/mo [est.] (unlimited, incl. video masters + external drive) or Google One 2 TB ~$10/mo [est.]. Recommended from month 2–3 as masters accumulate | 9 |
| File sync (copy 2) | **FreeFileSync** (free) | 0 | — | 0 |
| Screen/PDF tools | Any free PDF reader with highlight (e.g., PDF-XChange free / Preview) | 0 | — | 0 |

**Totals:**

| Scenario | Recurring $/mo | vs $100 cap |
|---|---:|---|
| **Launch stack (months 0–2)** | **$20** (Claude Pro only) | 20% of cap |
| **Recommended steady state (month 3+)** | **$47** = $20 AI + $18 music + $9 offsite backup | 47% of cap |
| Everything-on worst case (all upgrades, +25% price-drift margin) | ~$59; with margin **~$74** | still <75% of cap ✅ |

Headroom (~$26–80/mo depending on scenario) is deliberately reserved for the monetization phase's needs (e.g., a paid thumbnail-test tool or a second music seat) — it is not pre-committed here.

### 1.2 One-time hardware (not monthly; listed for completeness)

| Item | Choice | One-time cost [est.] | Why |
|---|---|---:|---|
| Microphone | **Samson Q2U** (~$70) or **Audio-Technica ATR2100x-USB** (~$99) | $70–99 | Dynamic USB/XLR hybrid: rejects untreated-room reverb (SOP-6 rationale); XLR path future-proofs an interface upgrade without a new mic |
| Pop filter + boom/desk arm | generic | $25–35 | Plosive control + consistent mic position |
| Backup drive ×1 (Copy 2) | 1 TB+ USB HDD/SSD | $50–70 | SOP-10; holds ~2 years of pruned episode archives |
| **Hardware total** | | **~$145–205 one-time** | Amortized over 12 months ≈ $12–17/mo equivalent — even counting it against the cap, every scenario above stays ≤$100/mo |

Everything else assumes an existing computer that can run Resolve (any recent laptop with 16 GB RAM; if the owner's machine can't, the fallback editor is **Shotcut** or **Kdenlive** — both free, both lighter — with the same template logic; this fallback is an inference, untested against the 1.5h edit budget).

---

## 2. Why this stack (grounding)

- **≤10h/video is the binding constraint** (engine §b, memo v2 economic gate) — so every choice optimizes for *templated repetition*, not power: standing Resolve project, standing Inkscape kit, standing prompts. Tools you rebuild in weekly cost hours; templates cost minutes.
- **$0 video/design/audio tier is fully sufficient** for a 1080p, diagram-led, narration-driven format — nothing in the brand spec (`BRAND_GUIDELINES.md` §3) requires 3D, motion-capture, or stock-footage subscriptions. The visual signature is self-drawn linework (gate 2/3), which is exactly the asset class free vector tools are best at.
- **The one paid launch tool is the AI assistant** because the prompt library (`PROMPT_LIBRARY.md`) is what compresses research+draft+fact-check from the documented 15–25h failure mode into the 10h design (memo v2 §3). Cutting it would cost hours, which cost more than $20 [inference — labeled].
- **No vidIQ/TubeBuddy-class subscription at launch:** keyword validation was completed in Phase 5 with existing credits (`LAUNCH_SLATE.md` keyword map); ongoing topic selection runs on API-verified view evidence per the engine §d rubric, which needs the free YouTube Data API, not a paid SEO tool. Re-evaluate only if the day-60 amber review (engine §e) blames discovery.

---

## 3. Editing template spec (build once in week 0; reuse every week)

All values from `brand/BRAND_GUIDELINES.md` §3 — palette: Report Navy `#0D1B2A` · Blueprint Blue `#1B4965` · Drafting Cyan `#5FA8D3` · Paper White `#E8EDF2` · Signal Red `#C1494B` · Caution Amber `#E0A458` · Gauge Green `#6A994E`. Fonts: **Archivo** (display) + **IBM Plex Mono** (technical), both free/SIL-OFL. No third font.

### 3.1 Intro stinger (≤5 s — hard cap)

- **Concept:** a blueprint sheet draws itself. Report Navy field; the 50 px grid fades in at 15% opacity (0.0–0.8 s); a 3 px Drafting Cyan line traces a schematic fragment of this episode's subject class (a truss, a valve, a hull section — 3 interchangeable class variants built once) (0.8–2.8 s); one Signal Red mark stamps on the failure point with a single low "thunk" (2.8–3.2 s); wordmark **MODE OF FAILURE** in Archivo Black, Paper White, letter-spaced, rises 12 px with a 200 ms fade (3.2–4.5 s). Out by 5.0 s.
- **Audio:** pencil-scratch + paper texture under the trace; the thunk is the only hit. No whoosh, no riser — calm register extends to sound design.
- **Placement:** *after* the cold open (SOP-7 timeline), never at 0:00 — the hook owns frame one.
- Built in Resolve (Fusion page or plain keyframes); saved in the template project. Total build ≈ one-time 2–3 h in week 0, zero weekly cost.

### 3.2 Lower-thirds (two presets, saved as Resolve Text+ templates)

Per brand §3.6 — anchored bottom-left, inside 10% title-safe, in/out = 200 ms slide+fade, no bounces:

- **Citation lower-third** (every quoted finding): 1 line, IBM Plex Mono Regular 24 pt Paper White, on Blueprint Blue bar @85% opacity, **8 px Signal Red left edge**. Text pattern: `NTSB HAR-71-1 · p.34 · "probable cause"`.
- **Context lower-third** (dates/places/people): line 1 Archivo Semibold 30 pt; line 2 IBM Plex Mono 22 pt; same bar, **Drafting Cyan edge**.

### 3.3 Diagram-reveal pattern (the signature move)

1. Diagram enters as **grid + secondary linework only** (the 0.75/1.5 px layers) — 1 beat.
2. **Primary subject** (3 px cyan) fades/wipes in as narration names it — 1 beat.
3. **Numbered tags** pop in sequence (100 ms apart) as each part is named.
4. **The Signal Red element lands last**, always synced to the exact narration beat that names the failure — red is never on screen before the voice earns it.
5. Sequence diagrams: hard cut or 300 ms wipe between `STATE` frames (exported as separate PNGs in SOP-5 — no animation software involved).

Implementation at $0: export the diagram from Inkscape as **layered stages** (grid / subject / tags / red) and stack them as timeline layers with fade-ins — 4 PNGs per diagram, cross-dissolved. Budgeted inside SOP-5/SOP-7 timings.

### 3.4 Chapter card style

Full-frame, 1.5–2.0 s, used at act boundaries only (3 per episode): Report Navy + grid; top-left in IBM Plex Mono Medium, Drafting Cyan: `PART 02 //`; below in Archivo Black 64 pt Paper White, ≤4 words: `THE MECHANISM`; bottom-right in Plex Mono Italic 20 pt: the episode's report ID. The card titles match the YouTube chapter names exactly (SOP-7.4) so the video's internal navigation and the platform's agree.

### 3.5 End-card layout (final 20 s — per brand §3.5, restated as build spec)

- 1280×720 design space scaled to frame; Report Navy; 50 px grid @15%.
- Left 55%: two stacked end-screen slots (410×230 boxes, 1.5 px Drafting Cyan border, 4 px corner radius), each labeled above in Plex Mono: `RELATED FAILURE //`.
- Right 40%: channel avatar subscribe element (196×196) above the line *"Researched, written, and narrated by a human."* — Archivo Semibold 28 pt.
- Bottom: class-color strip (cyan structural / amber fire-process / green transport-machinery, brand §3.4) carrying `Primary source: [report ID]` reversed out in Plex Mono.
- Audio: music bed only; narration's sign-off (*"…and that was the mode of failure."*) lands exactly as the card cuts in.

### 3.6 Thumbnail template (Inkscape, 1280×720)

Per brand §3.4, pre-built with locked guides: vertical-thirds grid · right ⅔ image zone (hero diagram or gate-3-clean archival) · left ⅓ text block, Archivo Black, Paper White, **≤4 words, ≤2 lines, one word may be Signal Red** · one red mark (circle/arrow/crack-path) on the failure location — exactly one · bottom 8% class-color strip with the `T+` timestamp or key number in Plex Mono. Hard bans baked into the template as a checklist layer: no shock faces, no MAYDAY gradients, no fake flames, no photorealistic-AI renders (gate 2), thumbnail text never repeats the title verbatim.

### 3.7 Diagram template kit (Inkscape, 1920×1080)

Pre-built: Report Navy artboard · 50 px grid layer @25% line 0.75 px · swatch palette (the 7 brand hexes, nothing else) · three stroke styles saved (3 px cyan / 1.5 px @60% / 0.75 px @25%) · numbered-tag symbol (1.5 px cyan circle + Plex Mono Medium numeral) · legend strip group (bottom edge) · citation text object bottom-right (Plex Mono Italic): `Source: ______ (redrawn)` · locked reference-layer slot at 30% opacity (SOP-5 redraw protocol) · humans-as-scale silhouette symbol (solid Blueprint Blue, no face). Sequence-frame labels saved as text presets: `STATE 1 — AS DESIGNED` / `STATE 2 — AS BUILT` / `STATE 3 — AT FAILURE`.

---

## 4. File & folder naming conventions

**Episode ID:** `MOF-E###` (E001 = Silver Bridge, per slate order). Slugs: lowercase, hyphens, ≤3 words. Dates: `YYYY-MM-DD`. Versions: `_v1`, `_v2`; the word `master` is reserved for final deliverables. **Never** rename a file after it appears in the asset manifest — the manifest is an audit document (SOP-9).

```
MOF-E001_silver-bridge/
├── 01_source/            # report PDF(s), figures/ (page-numbered screenshots)
│   └── figures/HAR-71-1_p34_fig12.png
├── 02_research/          # source-pack.md, pronunciation list, prompt outputs
├── 03_script/            # MOF-E001_script_v1.md … _final.md, _readcopy.md
├── 04_diagrams/          # MOF-E001_D1_eyebar.svg + staged exports _D1_s1..s4.png
├── 05_assets/            # archival stills, music
│   └── licenses/         # license-evidence screenshots/PDFs (SOP-9)
├── 06_audio/             # MOF-E001_narration_raw.wav, _narration_master.wav
├── 07_edit/              # Resolve project export/backup, captions MOF-E001.srt
├── 08_publish/           # MOF-E001_master.mp4, _thumb_A/B/C.png, metadata.md,
│                         #   MOF-E001_manifest.md, shorts/MOF-E001_S1.mp4
└── MOF-E001_manifest.md  # (or lives in 08_publish — one canonical location, pick once)
```

Channel-level (outside episode folders): `_templates/` (Resolve template project, Inkscape kits, stinger, this checklist) · `_dashboard/` (the Sheets exports, SOP-10) · `_brand/` (fonts, wordmark, palette file). The underscore prefix keeps them sorted above episodes.

---

## 5. Per-video checklist (printable one-pager)

> Print this page; one sheet per episode, pinned above the edit bay next to the brand card. A box left unchecked = the video does not advance. Full detail lives in `PRODUCTION_SOP.md` (gate index at the end).

```
MODE OF FAILURE — EPISODE CHECKLIST          MOF-E___  ·  topic: ______________
Publish target (Sat 09:00 ET): ____-__-__    Timer log target: ≤10.0h  actual: ____

MON — RESEARCH & OUTLINE (3.0h)
[ ] Final official report downloaded; ID/date/URL in source pack header
[ ] Source pack: mechanism / decisions / system — all section-cited
[ ] Figures screenshotted with page numbers; hero-diagram candidate flagged
[ ] Asset manifest STARTED; license evidence captured for every candidate
[ ] No agency press imagery anywhere (Getty/AP/Mirrorpix/Alamy = banned)
[ ] Outline: mechanism cold open (not body count); 3–5 diagrams; hero named

TUE — SCRIPT (2.0h)
[ ] Draft via prompt §3; owner rewrite done; 1,800–2,600 words
[ ] Every causal sentence carries [REPORT §X] citation
[ ] Read-aloud pass done; stumbles rewritten
[ ] Banned-vocab sweep: 0 hits (or report-quoted + cited)

WED — FACT-CHECK & DIAGRAMS (2.0h)
[ ] Fact-check prompt §7: ZERO unresolved claims
[ ] Pronunciations verified; phonetics in read copy
[ ] 3–5 diagrams built in template; reference layers DELETED before export
[ ] "(redrawn)" citation on every diagram; Signal Red once per composition
[ ] Stylized only — nothing photorealistic (gate 2)

THU — NARRATION & EDIT (2.5h)
[ ] 48kHz/24-bit mono WAV; peaks −12 to −6 dBFS; room noise < −60 dBFS
[ ] ~150 wpm read; clap-marked retakes; full sentences only
[ ] Edit chain: cut → NR → 80Hz HPF → breaths −8dB → comp → −16 LUFS
[ ] Full 1× listen-back against script — done
[ ] Timeline per template; visual change every 8–15s; max hold 20s
[ ] No archival photo altered/animated to change event appearance (gate 3)
[ ] Citation lower-third on every quoted finding
[ ] Mix −14 LUFS / −1 dBTP; music ducked −18 to −24 dB under voice
[ ] Captions corrected vs script; chapters at act boundaries
[ ] ASSET MANIFEST 100% COMPLETE — then, and only then, export

FRI — PACKAGE & PUBLISH (0.5h + schedule)
[ ] Final watch-through at 1× — full length, no skips
[ ] Title (keyword per slate map) + 3 thumbnail variants built
[ ] Packaging pre-mortem (playbook §5): 100% green
[ ] Description line 1: "Researched, written, and narrated by a human."
[ ] Report link + sources block + chapters in description; SRT uploaded
[ ] Disclosure tree: Q1 No / Q2 No / Q3 No → toggle "No"
      (ANY yes = STOP — upstream gate violation, fix before upload)
[ ] Test & Compare armed with all 3 thumbnails
[ ] Short #1 cut & scheduled (Tue); Short #2 ≤20 min or skipped
[ ] Scheduled Sat 09:00 ET; end-screen slots set; pinned comment drafted
[ ] Friday backup run: episode folder → Copy 2 (+ offsite for keep-set)
[ ] Dashboard Tab 1 row created; hours actual logged

SIGN-OFF: all 8 QC gates (SOP index G-A…G-H) green  →  PUBLISH
```
