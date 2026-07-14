# Channel Assets — MODE OF FAILURE

**Deliverable 2b · 2026-07-13.** Execution specs for the banner, avatar, and the three thumbnail templates. All colors, fonts, and rules inherit from `brand/BRAND_GUIDELINES.md` (§3). All imagery obeys the hard gates in `research/SELECTION_MEMO.md`: stylized/non-photorealistic only (gate 2 — also the disclosure-label-exempt register per `research/validation/probe-monetization-policy-status.md` Task 4), rights-clean sources only (gate 3). Each spec includes a prompt block usable in an AI image tool; AI-generated *stylized diagram/illustration* assets are permitted and label-exempt, AI-photorealistic assets are banned.

Palette shorthand used throughout: NAVY `#0D1B2A` · BLUE `#1B4965` · CYAN `#5FA8D3` · PAPER `#E8EDF2` · RED `#C1494B` · AMBER `#E0A458` · GREEN `#6A994E`. Fonts: Archivo (display), IBM Plex Mono (technical).

---

## 1. Channel banner (channel art)

### 1.1 Canvas and safe-area math

- Full canvas: **2560×1440** (TV rendering).
- Desktop crop: 2560×423 horizontal band, vertically centered (y = 508 to y = 931).
- **Minimum safe area (all devices, incl. mobile): 1546×423, centered** — x = 507 to x = 2053, y = 508 to y = 931. **Every letter and every critical mark must live inside this box.**
- Export: PNG, ≤6 MB (YouTube limit).

### 1.2 Layout (measurements relative to full 2560×1440 canvas)

| Element | Position / size | Spec |
|---|---|---|
| Background field | full 2560×1440 | NAVY, with a left→right linear gradient into BLUE at 20% strength; blueprint grid overlay (50 px module, CYAN at 12% opacity) covering the full canvas |
| Signature diagram (decor, may bleed outside safe area) | right half, x ≈ 1500–2560, full height | A large stylized eyebar-chain cross-section (episode-1 motif) in 3 px CYAN linework at 40% opacity, with the single eyebar-eye crack drawn 3 px RED at 100% — positioned so the red crack detail falls INSIDE the safe area at approx x = 1850, y = 640 |
| Wordmark | inside safe area, left-aligned at x = 560, baseline y = 700 | `MODE OF FAILURE` — Archivo Black, ~110 px cap height, PAPER, -2% tracking; the word `FAILURE` may carry a 6 px RED underline (drafting-style, slightly overshooting each end) |
| Tagline | x = 563, baseline y = 775 | `How it actually failed — from the official report.` IBM Plex Mono Regular, ~34 px, CYAN |
| Statement line | x = 563, baseline y = 855 | `Researched, written, and narrated by a human.` IBM Plex Mono Medium, ~30 px, PAPER on a BLUE bar with 8 px RED left edge (the citation lower-third style — brand continuity, and the always-on human-narrated placement per BRAND_GUIDELINES §4.2) |
| Upload cue | right edge of safe area, x ≈ 1900–2050, y = 855 | `NEW REPORT WEEKLY` — Plex Mono, 26 px, PAPER at 70% |
| Class-color strip | y = 916 to y = 931 (bottom 15 px of safe band), x = 507–2053 | Three equal segments: CYAN / AMBER / GREEN — the failure-class coding legend rendered as pure design |

### 1.3 Designer / AI-tool prompt (banner background plate only — type is set manually, never AI-rendered)

> Wide technical-blueprint illustration, dark navy background (#0D1B2A) with a subtle drafting grid in desaturated cyan, large engineering line drawing of a steel eyebar chain link cross-section on the right side, thin precise cyan linework (#5FA8D3) like a vintage accident-investigation report figure, one small crack detail highlighted in muted red (#C1494B), flat 2D vector style, no photorealism, no people, no text, generous empty space on the left half, clean, austere, technical drawing aesthetic, 2560×1440.

---

## 2. Avatar

### 2.1 Concept

**"The red-circled flaw."** A single circular mark from the diagrams — the brand's recurring red failure mark — containing a minimal eyebar-eye cross-section with a hairline crack. Reads at 98 px (comment size) as: navy disc, cyan ring, red tick. It is deliberately NOT a wordmark (illegible at small sizes) and not a skull/flame/warning-triangle (sensational register, banned).

### 2.2 Spec

- Canvas 800×800, design on a circle (YouTube crops circular).
- Background: NAVY disc, full bleed; faint 50 px grid at 8% opacity.
- Ring: 12 px CYAN circle at 78% of canvas diameter (624 px), a drafting "detail callout" circle.
- Inside: simplified eyebar eye (a cyan annulus, 16 px line) occupying ~55% of the inner area, with a RED crack path (14 px, jagged 3-segment polyline) breaking the annulus at the 4 o'clock position.
- Callout tab: small RED-filled circle (56 px) sitting ON the big cyan ring at 10 o'clock, containing `1` in Plex Mono Medium, PAPER — the diagram label motif.
- No letters otherwise. Test render at 98 px and 48 px before accepting.

### 2.3 AI-tool prompt

> Minimal flat vector logo on a dark navy circle (#0D1B2A), a thin cyan (#5FA8D3) engineering callout circle containing a simple cross-section of a steel eyebar eye drawn as a cyan ring, broken by a small jagged red (#C1494B) crack line at the lower right, one tiny red circular tag with the number 1 on the outer ring, blueprint schematic style, extremely clean and minimal, no gradients, no text besides the numeral, no photorealism, centered, 800×800.

---

## 3. Thumbnail templates (one per failure-class family)

Shared frame for all three (from BRAND_GUIDELINES §3.4): 1280×720 · NAVY field + 12%-opacity grid · right two-thirds image / left third text · Archivo Black text, ≤4 words, ≤2 lines, one word may be RED · exactly one RED mark on the image · bottom 8% (58 px) class-color strip with a Plex Mono data callout reversed out · NO shock faces, no fake flames, no photorealistic AI renders. Title carries the search keyword; thumbnail carries the mechanism (`research/keywords/LAUNCH_SLATE.md` title formula + keyword map).

Export: 1280×720 PNG < 2 MB. Legibility test: 10% zoom (mobile browse size) — if the red mark or any word disappears, iterate.

### 3.1 Template A — STRUCTURAL / CIVIL (strip: CYAN) — slate #1, 2, 7, 9

- **Image zone (x = 427–1280):** a single self-drawn structure elevation or cross-section (bridge span, building section, dam profile) in CYAN 3 px linework, tilted 4° for energy, occupying ≥70% of the zone height. The failing member is redrawn RED with a crack-path or separation gap, circled by a 6 px RED detail-callout circle (the avatar motif at work).
- **Text zone (x = 0–427):** 2 lines max, e.g. `ONE EYEBAR` / (RED) `13 SECONDS` — Archivo Black ~120 px cap height, left-aligned at x = 48.
- **Strip:** CYAN, callout in NAVY Plex Mono: the load-bearing number (`T+0:00:13` or `40-YEAR CRACK`).
- **Example execution (Ep. 1, Silver Bridge):** full eyebar-chain suspension elevation, red circle on the lower-chord eyebar joint, crack detail exploded in a callout box top-right; text `ONE EYEBAR` / `13 SECONDS`.
- **AI prompt (image plate):** *Technical blueprint side-elevation drawing of a 1920s eyebar-chain suspension bridge, thin cyan (#5FA8D3) precise linework on dark navy (#0D1B2A) with faint drafting grid, one chain link near the tower highlighted in red (#C1494B) with a red engineering callout circle around it and a magnified crack detail in a small inset box, flat 2D vintage accident-report figure style, no text, no people, no photorealism, dramatic but austere, 1280×720, subject weighted to the right two thirds of the frame.*

### 3.2 Template B — FIRE / EXPLOSION / PROCESS (strip: AMBER) — slate #3, 5

- **Image zone:** a cutaway section (hotel floors, distillation tower, pipe run) in CYAN linework; the propagation path — smoke route, vapor cloud, overpressure front — rendered as an AMBER flow arrow system (3 px lines with arrowheads, 30% fill regions), NOT as illustrated flames. Origin point gets the single RED mark. Stylized flow-arrows keep this class calm, diagrammatic, and disclosure-exempt where photoreal fire would be none of those.
- **Text zone:** e.g. `THE SMOKE` / (RED) `NOT THE FIRE` — note: mechanism subversion is this class's hook (fire was out in minutes — `LAUNCH_SLATE.md` #3).
- **Strip:** AMBER, callout in NAVY: `85 DEAD · FIRE OUT IN MIN 10` style fact, or report ID.
- **Example execution (Ep. 3, MGM Grand):** 26-story tower section, amber arrows climbing seismic joints and elevator shafts from a red-marked deli fire origin on floor 1; text `THE SMOKE` / `NOT THE FIRE`.
- **AI prompt (image plate):** *Architectural cutaway section of a 1980s high-rise hotel tower drawn as a technical blueprint, thin cyan (#5FA8D3) linework on dark navy (#0D1B2A), amber (#E0A458) arrows flowing upward through elevator shafts and stairwells across many floors, one small red (#C1494B) circle at the ground-floor origin point, flat 2D accident-report diagram style, no flames, no smoke clouds, no people, no text, no photorealism, clean and precise, 1280×720, composition weighted right.*

### 3.3 Template C — TRANSPORT / MACHINERY / MARITIME (strip: GREEN) — slate #4, 6, 8, 10

- **Image zone:** the machine or vessel in profile/cross-section (locomotive + tank-car consist, semi-submersible rig, ferry hull, hydro turbine) in CYAN linework; motion/physics vectors (grade arrows, list angle, flooding sequence, thrust) in GREEN 3 px; the failed component (hand brake set, ballast-control panel, cargo door, turbine studs) carries the single RED mark. Water, where needed, is a GREEN 30%-opacity horizontal band with a drafted waterline — never rendered waves.
- **Text zone:** e.g. `72 HAND BRAKES` / (RED) `SET: 7` — the number pair is this class's hook.
- **Strip:** GREEN, callout in NAVY: gradient/angle/pressure figure (`1.2% GRADE · 63 MPH`).
- **Example execution (Ep. 4, Lac-Mégantic):** train consist profile on an exaggerated 4° grade line, green descent vector toward a town plan-view dot, red circle on the lead locomotive's brake group; text `72 BRAKES` / `SET: 7`. *(Numbers per TSB report as scripted in Phase 9 — thumbnail numbers must match the script's verified figures before export.)*
- **AI prompt (image plate):** *Technical blueprint profile drawing of a long freight train of tank cars on a descending grade, thin cyan (#5FA8D3) linework on dark navy (#0D1B2A) with faint grid, a green (#6A994E) arrow indicating downhill motion toward a small town drawn as a map footprint, one red (#C1494B) engineering callout circle on the lead locomotive, flat 2D accident-investigation report figure style, no fire, no people, no text, no photorealism, austere and precise, 1280×720, subject weighted to the right two thirds.*

### 3.4 Template governance

- One template per video, chosen by failure class — never mixed. Class → strip color is a hard mapping (catalog-level legibility: a subscriber browsing the channel page should be able to read the catalog by color).
- Archival-photo thumbnails are the *exception* path (allowed only when a public-domain photo is objectively stronger than the diagram — e.g., the iconic PD wreckage aerials): photo occupies the image zone desaturated toward NAVY (duotone NAVY/PAPER), red mark + text rules unchanged, license provenance logged in the per-video asset manifest first (gate 3).
- A/B iteration (Phase 8 packaging loop) may vary text and red-mark placement freely, but never the grid, fonts, strip mapping, or the one-red-mark rule.
