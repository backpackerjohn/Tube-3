# Production SOP — Mode of Failure

**Phase 10 deliverable · 2026-07-13 · Binding documents upstream:** `content-engine/CONTENT_ENGINE.md` (pipeline + 10.0h budget + kill-switch), `content-engine/PROMPT_LIBRARY.md` (prompts §1–§8), `content-engine/PACKAGING_PLAYBOOK.md` (packaging + Test & Compare), `brand/BRAND_GUIDELINES.md` (voice, palette, diagram rules), `research/SELECTION_MEMO.md` (four hard gates), `research/validation/probe-monetization-policy-status.md` (disclosure-label rulings). Tools named here are specified — with costs — in `production/TOOLCHAIN_AND_TEMPLATES.md`.

**The four hard gates repeat at the top of every SOP because they are the only rules that can never flex:** (1) human narration, no TTS ever · (2) stylized non-photorealistic art only · (3) rights-clean assets with per-video manifest · (4) the day-120 kill-switch. Where any instruction below conflicts with a gate, the gate wins.

---

## 0. Time-budget reconciliation (must sum to 10.0h — it does)

The content engine (`CONTENT_ENGINE.md` §b) fixes the per-video budget at **10.0 hours** as a hard economic gate (memo v2: the documented modal failure is 15–25h/video). Every SOP below carries a minute-level sub-budget that sums exactly to its stage allocation:

| Engine stage | Engine hours | SOP | Sub-budget check |
|---|---|---|---|
| 1. Research & report digest | 2.5 | SOP-1 | 20+40+45+30+15 min = 2h30 ✅ |
| 2. Outline | 0.5 | SOP-2 | 10+15+5 min = 0h30 ✅ |
| 3. Script draft | 2.0 | SOP-3 | 15+60+40+5 min = 2h00 ✅ |
| 4. Fact-check pass | 0.5 | SOP-4 | 20+10 min = 0h30 ✅ |
| 5. Diagrams | 1.5 | SOP-5 | 15+60+15 min = 1h30 ✅ |
| 6. Narration | 1.0 | SOP-6 | 10+25+15+10 min = 1h00 ✅ |
| 7. Edit & assembly | 1.5 | SOP-7 | 10+45+20+15 min = 1h30 ✅ |
| 8. Package & publish | 0.5 | SOP-8 | 15+10+5 min = 0h30 ✅ |
| **Total** | **10.0** | | **10h00** ✅ |

**Overrun rule (engine §b, restated):** a stage overrun comes out of a later stage or the video slips a week. Never fill the weekly slot with an unfinished video; never double cadence to catch up. **Timer rule:** run a timer per stage (any phone timer or the free Toggl Track tier) and log actual hours in dashboard Tab 1 ("Production hours actual") — hours creep is the silent killer of the economics (engine §e).

**Outside the 10h budget (weekly overhead, ~1h05 total):** Monday dashboard update 30 min (engine §e) · Short #2 cut ≤20 min or skipped (engine §f) · community-tab post ~10 min (engine §c) · Friday backup run ~5 min (SOP-10). These are channel-operating costs, not per-video production costs; they are listed so nothing is hidden.

---

## SOP-1 — Report research & digest (2h30)

**Input:** the week's topic (slate order for videos 1–10; rubric-selected from video 11, engine §d). **Output:** the source pack + a started asset manifest.

### 1.1 Where the reports live (20 min: locate & download)

All primary sources are official investigation bodies — public domain or openly licensed government works, which is why gate 3 is satisfiable at $0. Portals (all grade **A — primary/official**; URLs are the agencies' public report databases):

| Body | What it covers | Where to search |
|---|---|---|
| **NTSB** (US) | Highway/bridge, rail, marine, pipeline, aviation | ntsb.gov → Investigations; full-text search via the CAROL query tool at data.ntsb.gov/carol-main-public. Historical reports (e.g., Silver Bridge HAR-71-1) are digitized PDFs — if CAROL misses a pre-1990 report, search the report number + "ntsb.gov" or pull from ROSA P (rosap.ntl.bts.gov, the DOT national transportation library). |
| **CSB** (US) | Chemical/process/refinery incidents | csb.gov → Investigations. Each investigation page carries the final report PDF **and** the CSB's own animation video — watch it once; it is the demand evidence (slate #5) *and* the mechanism storyboard you must out-explain, not copy. |
| **NIST / NCST** (US) | Structural collapses, building fires | nist.gov → Disaster and Failure Studies (National Construction Safety Team). Champlain Towers South findings (June 2026) live here. Reports are US-government works: public domain, figures included. |
| **MAIB** (UK) | Marine accidents | gov.uk/maib-reports (searchable by vessel/year). UK reports are Crown copyright under the Open Government Licence — attribution required; log OGL v3 in the manifest. |
| **TSB** (Canada) | Rail, marine, pipeline, air | tsb.gc.ca → Investigation reports (e.g., R13D0054, Lac-Mégantic). Terms permit non-commercial reproduction with attribution; for our use, quote + redraw and cite — log the terms page in the manifest. |
| **Other bodies used by the slate/backlog** | — | MSHA (msha.gov — US mining, e.g., Upper Big Branch); USCG marine casualty reports (via dco.uscg.mil or NTSB joint reports); UK HSE (hse.gov.uk, e.g., Flixborough successor material); Royal Commission reports (national archives of Canada/Australia; Ocean Ranger via Memorial University's Digital Archives); court-of-inquiry PDFs surfaced via Google Scholar or archive.org when the originating agency predates the web. |

Rules: download the **final** report (not the preliminary), record report ID + release date + URL in the source pack header, save the PDF into the episode folder (`01_source/`). If no report of substance exists, the topic dies here — "no report → no video" (engine gate G2; promise clause).

### 1.2 First skim (40 min: read like an investigator, not a completist)

Reports run 100–500+ pages; the 10h budget survives because you never read linearly. Read in this order:

1. **Synopsis / Executive summary / Probable cause statement** (every agency front-loads it).
2. **Findings + Recommendations sections** (the numbered lists — this is the system layer and the "end on the fix" material, voice rule 10).
3. **The analysis chapter** for the failure mechanism only (skip the boilerplate on agency methodology).
4. **Figure flip-through:** page through every figure/diagram/photo, screenshotting candidates into `01_source/figures/` with page numbers in the filename (`HAR-71-1_p34_fig12.png`). These seed SOP-5.

Mark up the PDF (any free PDF reader) with three highlight colors: mechanism = cyan, decisions = amber, system = green — mirroring the three-layer structure the source pack needs.

### 1.3 Digest with the prompt library (45 min)

Run the **report-digest prompt** (`PROMPT_LIBRARY.md` §1) on the report (feed it the summary, findings, and analysis chapters — not all 400 pages). The prompt returns the **source pack**: mechanism chain, decision chain, system findings, key figures/quotes — each item with a numbered report-section citation. Then do the human pass the prompt cannot: verify each source-pack line against your highlighted PDF; anything the model produced that you cannot find in the report is deleted now (cheaper here than in SOP-4).

**Note-taking format (the source pack is the only note file — one file, `02_research/source-pack.md`):**

```
# SOURCE PACK — [Event] · [Report ID] · [Report date] · [Report URL]
## LAYER 1 — MECHANISM CHAIN (what physically failed, in sequence)
M1. [claim] — [§/page cite]
M2. ...
## LAYER 2 — DECISION CHAIN (who decided what, when, and why it seemed reasonable)
D1. [claim] — [§/page cite]
## LAYER 3 — SYSTEM FINDINGS (regulation/design practice/organizational findings + what changed after)
S1. [claim] — [§/page cite]
## QUOTES (verbatim, ≤25 words each, page-cited — these become citation lower-thirds)
Q1. "..." — [§/page]
## FIGURES (candidates for redraw — file, page, what it shows)
F1. HAR-71-1_p34_fig12.png — eyebar 330 fracture face
## NUMBERS TABLE (every load-bearing number: value · unit · page)
## OPEN QUESTIONS / UNCERTAINTY the report itself flags (feeds voice rule 8)
```

### 1.4 Start the asset manifest (30 min)

Open the manifest template (SOP-9) and log every asset candidate found so far: report figures (public domain / licence noted), archival photo candidates from **NARA catalog (catalog.archives.gov), Library of Congress (loc.gov/pictures), Wikimedia Commons (license checked per-image — Commons hosts non-free images too; read the license box, not the site name)**. For each: capture the license evidence NOW (screenshot or PDF-print of the rights page into `05_assets/licenses/`) — license pages change; your evidence file is the defense. Agency press imagery (Getty/Mirrorpix/AP/Alamy watermarks or credits) is off-limits even when the photo looks old (gate 3, memo verbatim).

### 1.5 Gate check (15 min)

**Stage-1 quality gate (engine §b):** source pack maps all three layers to numbered report sections · every archival candidate has provenance logged · report is substantive. Fail → kill or defer the topic, log it in the topic log with the reason, pull the next backlog topic.

---

## SOP-2 — Outline (0h30)

1. **(10 min)** Run the **outline prompt** (`PROMPT_LIBRARY.md` §2) with the source pack pasted in. It returns: cold open, three-act structure, diagram list (3–5), quote placements.
2. **(15 min)** Human edit: reorder for the decision-chain tension (voice rule 5 — no false suspense about settled facts), confirm the cold open is a **mechanism hook, not a body count** (voice rule 1), and mark which diagram is the **hero** (thumbnail-grade, engine stage-5 gate).
3. **(5 min)** Gate check: three-layer test passes · ≥1 diagram is load-bearing to the explanation · cold open passes rule 1. Fail → fix now; outlining is the cheapest place to fix structure.

---

## SOP-3 — Script draft (2h00)

Target **1,800–2,600 words** (engine stage 3). At the SOP-6 pacing standard of ~150 wpm that is 12:00–17:20 of narration, landing the finished video in the 12–20 min documentary band once diagram holds and the end card are added.

1. **(15 min)** Run the **script-draft prompt** (`PROMPT_LIBRARY.md` §3 — voice rules are inlined in the prompt) with source pack + approved outline.
2. **(60 min)** Owner rewrite pass — the draft is raw material, not a script. Work paragraph by paragraph: replace every adjective with a number where the report has one (voice rule 3), shorten sentences at load-bearing moments (rule 7), set reconstruction in present tense / findings in past (rule 9), and keep every causal sentence's inline citation tag `[HAR-71-1 §X]` (these tags become citation lower-thirds in SOP-7 and are deleted from the read copy in SOP-6).
3. **(40 min)** **Read the entire script aloud once, standing, at speaking pace.** Mark every stumble — a sentence you trip on at the desk will cost three retakes at the mic. Rewrite the stumbles. This single pass is the highest-ROI hour-fraction in the pipeline for a non-professional narrator.
4. **(5 min)** Banned-vocabulary sweep: search the script for each word on the brand list (*horrifying, terrifying, nightmare, doomed, deathtrap, shocking, insane, unbelievable, chilling, gruesome, haunting*, second-person dares). Zero hits, or each hit is a cited report quote (Buffalo Creek's "flagrant disregard" pattern).

Gate check (engine stage 3): every causal sentence cited · zero speculation beyond the report · calm register throughout.

---

## SOP-4 — Fact-check pass (0h30)

1. **(20 min)** Run the **fact-check prompt** (`PROMPT_LIBRARY.md` §7): script verified claim-by-claim against the source pack and the report PDF. It returns a claims table with verdicts.
2. **(10 min)** Resolve every flagged claim: fix the number, add the citation, or delete the sentence. A claim the report doesn't support is deleted or explicitly framed in-script as outside the findings (voice rule 8). **Zero unresolved claims** is the gate — this is what makes "they read the actual TSB report" (Persona 3 credibility) literally true.

Also verified here: **pronunciations.** List every proper noun and technical term; check each (Forvo, agency b-roll, local news clips). Write phonetic respellings inline in the read copy — mispronunciation is a documented beatable incumbent weakness (engine stage 6 gate; slate Estonia note).

---

## SOP-5 — Diagram production (1h30)

**Tool: Inkscape (free, SVG) with the standing brand template file** (`TOOLCHAIN_AND_TEMPLATES.md` §3 — canvas, grid, swatches, line-weight styles, tag symbols pre-built). The template kit is why 3–5 diagrams fit in 1.5h: you never rebuild the frame, you only draw the subject.

### 5.1 Brief (15 min)
Run the **diagram-brief prompt** (`PROMPT_LIBRARY.md` §4) per diagram (batch all 3–5 in one session). Each brief names: the report figure(s) it derives from, the one Signal Red element, labels, and the state-sequence if it's a progression diagram.

### 5.2 Build (60 min, ~12–20 min per diagram)

**The redraw protocol — how to derive from report figures without copying 1:1 (gate 3 + brand §3.3.6):**

1. Import the report figure screenshot onto a **locked reference layer at 30% opacity**.
2. On the working layer, draw the subject in brand linework — but **recompose**: choose your own crop, viewing angle or schematic simplification, your own label set and callout numbering, and add information the figure lacks (timestamps, the failure-path in Signal Red, dimension callouts from the report text). The output is a new explanatory drawing *informed by* the figure, not a traced restyle of it.
3. **Delete the reference layer before export.** The deliverable contains only your linework.
4. Citation line bottom-right, IBM Plex Mono Italic: `Source: NTSB HAR-71-1, Fig. 12 (redrawn)` — "redrawn" is literal and load-bearing (brand §3.3.3). (US federal report figures are public domain, so even closer derivation is rights-safe for NTSB/CSB/NIST material — but the redraw protocol applies to ALL figures uniformly because Crown-copyright/foreign-inquiry figures are not PD, and one uniform habit can't be misapplied. This uniformity rule is an inference/design choice, not a legal requirement for US-government figures.)

Brand rules enforced by the template: three line weights only (3 px cyan subject / 1.5 px 60% secondary / 0.75 px 25% grid+dimensions) · Signal Red exactly once per composition · numbered circular tags + bottom legend strip · leader lines 45°/90° only · humans only as neutral Blueprint Blue scale silhouettes · no distress, bodies, blood, or victims' effects (brand §3.3.5).

**Sequence diagrams** (the money shot): duplicate the finished frame 3–5 times, advance the state per frame (`STATE 1 — AS DESIGNED` → `STATE 3 — AT FAILURE`), red element propagating. Export each state as its own PNG — the "diagram reveal" in the edit is a cut/wipe between states, so no animation software is needed.

**Export:** PNG at 1920×1080 (diagrams are composed on the 1080p artboard; the 50 px grid module and px line weights in brand §3.3 are defined at this size). Hero diagram additionally exported at 1280×720 crop for the thumbnail build.

### 5.3 Gate check (15 min)
Stylized/non-photorealistic only (gate 2 — this is what keeps the synthetic-media disclosure toggle legally "No", probe Task 4 ruling #4) · one thumbnail-grade hero frame exists · every diagram self-made/report-derived with citation line · manifest updated with each diagram + its source figure lineage.

---

## SOP-6 — Narration recording (1h00) — for a non-professional

Gate 1 verbatim: the owner records, or a hired **human** narrator does. No TTS, no AI voice, ever — including Shorts.

### 6.1 Setup (10 min, converges to 3 min once routined)

- **Mic:** a **dynamic USB/XLR mic** (Samson Q2U or Audio-Technica ATR2100x class — see toolchain §1 for cost). Dynamic, not condenser, is the specific choice for a non-professional: dynamics reject untreated-room reverb and household noise that a condenser faithfully records. Add the foam windscreen + a pop filter.
- **Room treatment hacks ($0–20):** record inside a **clothes closet** (hanging clothes = broadband absorption), or build a **duvet fort** (duvet over two chairs around the mic), or drape a moving blanket behind and in front of you. Kill the noise sources you can: fridge in another room off... no; realistically: HVAC off, fan off, phone on airplane, hard-drive/laptop fan pointed away, record when the street is quiet. Test: record 10 s of silence — the meter should sit below **−60 dBFS**; if not, hunt the hum before recording.
- **Mic technique:** 5–10 cm from the grille, speaking **slightly off-axis** (45°, past the mic, not into it — kills plosives), gain set so normal-read peaks hit **−12 to −6 dBFS** (never touching 0). Same position every week: tape an X on the desk.
- **Recording settings (Audacity or any DAW):** **48 kHz / 24-bit / mono WAV.** One project per episode: `MOF-E001_narration_raw`.

### 6.2 The read (25 min for a 12–17 min script)

- **Pacing: ~150 wpm** — the documentary standard this channel targets (12:00–17:20 for 1,800–2,600 words). Calibrate once: read a known 300-word passage against a 2:00 timer; adjust until it lands. Most nervous readers rush — aim to feel "slightly too slow"; that is correct on playback.
- **One take-through + pickups** (engine stage 6). Do not stop for small flubs mid-flow. **Retake protocol:** on a flub, pause 2 s, **clap once** (a visible spike to cut by), then re-read from the *start of the sentence*, matching your original pitch. Never restart mid-sentence — splices inside sentences are audible.
- Stand or sit upright; keep water (room temp) in reach; re-read rule-7 "load-bearing" sentences deliberately slower — the script marks them.
- Read from the **read copy** (citation tags stripped, phonetics inline), on a silent screen (no paper rustle).

### 6.3 Edit the take (15 min)

In Audacity (free) — the chain, in order:

1. **Cut retakes:** find the clap spikes, keep the last read of each sentence, delete the rest.
2. **Noise reduction:** capture 3–5 s of room-tone noise profile → Effect ▸ Noise Reduction: **12 dB reduction, sensitivity 6.0, frequency smoothing 3** (start values; ears over numbers — artifacts mean you've gone too far, back off to 8 dB).
3. **High-pass filter** at **80 Hz** (Filter Curve EQ low-cut) — removes rumble/desk thumps below the voice.
4. **Breaths: attenuate, don't delete.** Select each audible intake and drop it **−8 to −10 dB** (Amplify effect). Deleting breaths entirely makes a human read sound like TTS — exactly the wrong signal for this channel's human-narrated brand defense.
5. **Compression:** Audacity Compressor — threshold **−18 dB, ratio 3:1, attack 0.1 s, release 1.0 s** — evens the nervous-reader volume drift.
6. **Loudness Normalization to −16 LUFS** (mono voice track headroom; the final video mix hits **−14 LUFS integrated, −1 dBTP true peak** in SOP-7 — YouTube's playback normalization target, so louder buys nothing).
7. Export `MOF-E001_narration_master.wav` (48/24 WAV — never hand the editor an MP3).

### 6.4 Gate check (10 min)
**Listen back to the full track at 1×** while following the script (this is the engine's stage-6 gate — do it against the read copy, marking any mismatch). Human voice ✅ calm read ✅ pronunciations as verified in SOP-4 ✅ no clipped words at splice points ✅.

*(Listen-back overlaps the tail of the edit pass in practice; the 10 min line item is the attention, and a 15-min residual of listening runs while SOP-7 setup begins — the Thursday block schedules stages 6 and 7 back-to-back for exactly this reason.)*

---

## SOP-7 — Edit & assembly (1h30)

**Tool: DaVinci Resolve (free)** with the standing episode template project (`TOOLCHAIN_AND_TEMPLATES.md` §3): tracks, stinger, lower-third presets, end-card, music bed slots pre-placed. Editing is assembly into a template, not design from scratch — that is the only way 12–20 min cuts fit in 1.5h.

### 7.1 Timeline structure (the standing skeleton)

| Block | Content | Timing |
|---|---|---|
| Cold open | Mechanism hook over the hero diagram or a PD archival still. No stinger first — the hook is frame one. | 0:00–0:40 |
| Intro stinger | Brand stinger (≤5 s, toolchain §3.1) + episode title card | ~0:40–0:45 |
| Act I — context | The system as designed. Context lower-thirds for dates/places/people. | ~25% of runtime |
| Act II — mechanism | The failure, diagram-led. Sequence-diagram reveals; citation lower-third every time a finding is quoted. | ~45% |
| Act III — system & fix | Decision chain consequences → what changed (rule 10: end on the fix). | ~25% |
| Sign-off + end card | "…and that was the mode of failure." lands as the card appears; narration ends before the card; music only under the final 20 s (brand §3.5). | final 20 s |

### 7.2 Assembly pass (45 min)
Drop narration master on A1; lay visuals to the script's scene markers. **Pacing rules:** a visible change (new image, diagram state, zoom move, lower-third) every **8–15 s**; maximum hold on a static frame **20 s** and only on a diagram the narration is actively walking; slow push-in (2–4% scale over the hold) on archival stills — **but never animate/alter an archival photo in a way that changes what the event appears to be** (gate 3; probe Task 4 format-2 tripwire (a) — a Ken-Burns move on an authentic photo is fine; compositing, colorizing-to-imply-footage, or AI-animating it is not). Diagram reveals: cut or 300 ms wipe between exported states, synced to the narration beat that explains the change.

### 7.3 Sound + music (20 min)
Music bed from the licensed library (toolchain §1; log track + license in the manifest) on A2, ducked **−18 to −24 dB under voice** (sidechain or manual: music should be felt, not heard); no music under the cold open's key sentence or the probable-cause quote — silence is the emphasis tool of the calm register. Final mix loudness: **−14 LUFS integrated, −1 dBTP** (Resolve's loudness meter on the master bus).

### 7.4 Captions, chapters, export + final QC (15 min)
- **Captions:** generate the transcript (Resolve free-tier audio transcription, or YouTube auto-captions post-upload), then **correct it against the script** — technical terms and proper nouns are exactly what auto-captioning botches, and captions are an accessibility + retention surface. Upload as SRT in SOP-8.
- **Chapter markers** at the act boundaries + each named diagram ("The eyebar, up close") — chapters double as browse hooks.
- **Export:** 1080p, H.264/MP4, high bitrate preset (`MOF-E###_master.mp4`).
- **Final QC gate (watch-through at 1×, full length — non-negotiable):** ☐ no photorealistic-AI imagery anywhere (gate 2) ☐ no altered archival meaning (gate 3) ☐ every quoted finding has its citation lower-third ☐ Signal Red once per composition ☐ audio: no splice artifacts, music ducked, −14 LUFS ☐ end card + sign-off land correctly ☐ **asset manifest 100% complete** — every visual and audio asset on the timeline appears in the manifest with license provenance (gate 3; export is forbidden until this is true).

*(The 1× watch-through of a 12–20 min video runs during the export render + Friday morning buffer; the 15-min line covers setup and the fix-list, and the watch itself is the first item of Friday's stage-8 block. Total Thursday+Friday wall-clock still fits the engine's weekly rhythm.)*

---

## SOP-8 — Package, upload & publish (0h30)

### 8.1 Package (15 min)
Run the **title/description/tags prompt** (`PROMPT_LIBRARY.md` §6) and the **thumbnail-concept prompt** (§5); build the 3 thumbnail variants in the thumbnail template (A hero-diagram / B archival+overlay / C contrast — playbook §3.2); run the **packaging pre-mortem checklist** (`PACKAGING_PLAYBOOK.md` §5) — 100% green or no upload. Cut Short #1 (vertical reframe of the hero-diagram segment, engine §f) inside this block.

### 8.2 Upload SOP (10 min) — metadata order + the disclosure decision tree

**Metadata, in order:**
1. Title: the winning title (playbook §2 formula; primary keyword from the slate keyword map).
2. Description line 1 (above the fold, verbatim): **"Researched, written, and narrated by a human."** (brand §4.2).
3. Description body: 2-sentence summary → **Primary source block** (report ID + link — the "we read it so you didn't have to" proof, engine §c) → chapters list → sources & further reading → the standing channel boilerplate.
4. Tags from prompt §6; playlist by pillar; end screen: two related-failure slots + subscribe (brand §3.5 layout).
5. Captions: upload the corrected SRT.
6. Schedule: **Saturday 09:00 ET** (engine §c — held-constant default; do not improvise the slot).

**Altered/synthetic-content disclosure toggle — decision tree** (grounded in probe Task 4, official policy blog.youtube Mar 18 2024 / support.google.com/youtube/answer/14328491, source grades [A]):

```
Q1. Does the video contain AI/synthetically generated imagery that a viewer
    could mistake for a REAL person, place, scene, or event?
      → Our house style is blueprint-stylized, clearly-illustrated diagrams:
        EXEMPT by design (probe Task 4, format 4: "clearly unrealistic,
        animated, special effects" exemption).
    If YES anywhere → STOP. Do not toggle-and-ship. The video violated
    hard gate 2 upstream; the asset is replaced before upload.
Q2. Were any authentic archival photos/footage altered or animated so the
    real event/place appears different from reality?
      → Must be NO (gate 3; format-2 tripwire (a)). If YES → STOP, fix.
Q3. Was any real person's voice synthesized, or any real person depicted
    saying/doing something they didn't?
      → Must be NO (gate 1: owner-recorded narration). If YES → STOP.
ALL THREE NO → answer the Studio disclosure questions "No" (no label).
```

The tree's purpose is asymmetric by design: the correct answer is always "No" **because the production system makes it true**, and any "Yes" is a production defect, not a disclosure decision. (AI production assistance — scripts, outlines, prompts, thumbnail drafting — is explicitly exempt from disclosure and does not falsify the human-narrated statement: probe Task 4 + brand §4.4.)

**Test & Compare setup** (playbook §3.3): attach all 3 thumbnail variants at upload; YouTube picks the winner by **watch-time share** (which auto-penalizes curiosity-gap bait — it enforces never-rule #6 by measurement). Let the test run to Studio's confidence call — do not end it early on day-2 CTR; log the winner + lift in dashboard Tab 1.

### 8.3 Publish-day checks (5 min)
Pin the owner-voice comment (accountable-faceless posture, brand §4.5) · verify chapters render · verify end-screen slots point at the two designated related failures · Short #1 scheduled for Tuesday.

---

## SOP-9 — Asset manifest & license provenance (hard gate 3) — the template

One manifest per episode, `MOF-E###_manifest.md` (or a sheet tab), started in SOP-1, completed before export (SOP-7 gate). **Every** visual and audio asset on the timeline gets a row — including our own diagrams (lineage) and the music bed.

```
# ASSET MANIFEST — MOF-E001 · Silver Bridge · export date: YYYY-MM-DD
Status: ☐ COMPLETE (all rows verified) — export forbidden until checked.

| ID | File | Type | Description | Source (exact URL) | Creator/Agency | License | Evidence file (in 05_assets/licenses/) | Verified date | Used at (timestamps) | Notes |
|----|------|------|-------------|--------------------|----------------|---------|-----------------------------------------|---------------|----------------------|-------|
| A01 | HAR-71-1_p34_fig12.png | report figure (shown as document) | NTSB fracture diagram | [report URL] | NTSB | US Gov work — public domain | ntsb_pd_terms.pdf | 2026-07-28 | 07:12–07:31 | shown as-is, as a document |
| A02 | MOF-E001_D1_eyebar.png | own diagram | eyebar cross-section, redrawn | derived from A01 | Mode of Failure | own work | — | — | 03:05–03:40, thumb | citation line: "(redrawn)" |
| A03 | wiki_silverbridge_1928.jpg | archival photo | bridge, 1928 | [Commons file URL] | [photographer] | PD-US (pre-1930 pub.) | commons_A03_license.png | 2026-07-28 | 01:10–01:25 | license box screenshotted |
| A04 | bed_track.mp3 | music | Act I–III bed | [library track URL] | [artist/library] | [library license + acct ID] | musiclib_A04.png | 2026-07-28 | full | — |
```

**Rules:** no row, no timeline — an asset without a completed row never enters the edit. License evidence is captured at acquisition (SOP-1.4), not at export. Allowed license classes: US-government work (PD) · Crown copyright under OGL v3 (attribute) · Wikimedia Commons with a verified PD/CC tag (attribute per tag; **CC "NC" and "ND" tags are treated as unusable** — monetized videos are commercial use [inference from license terms; conservative by design]) · our own work · the paid/free music library under its account license. **Banned regardless of apparent age:** Getty, Mirrorpix, AP, Alamy, Reuters, or any watermarked/credited agency image (gate 3 verbatim). Manifests are retained permanently (SOP-10) — they are the audit trail if a claim ever arrives.

---

## SOP-10 — Archive & backup (outside the 10h; ~5 min Friday + 15 min monthly)

**Standard: 3-2-1** — 3 copies, 2 different media, 1 offsite.

- **Copy 1 (working):** the editing machine, episode folder per the naming convention (toolchain §4).
- **Copy 2 (local archive):** external USB drive; Friday after upload, sync the finished episode folder (free tool: FreeFileSync mirror job — one double-click).
- **Copy 3 (offsite):** cloud backup or cloud drive (toolchain §1 — free tier at launch covers scripts/manifests/diagrams; the paid tier adds video masters).

**What is kept forever (the "keep set"):** final script + read copy · source pack · asset manifest + `licenses/` evidence folder · all diagram SVGs + exports · narration master WAV · final master MP4 · thumbnail sources + 3 variants · the report PDF. **What is pruned after 60 days:** Resolve render cache, raw narration WAV (the edited master survives), unused asset candidates. Prune keeps the per-episode archive under ~10 GB [inference: typical 1080p master + WAV sizes], so a 1 TB drive holds 2 years of channel.

**Restore drill (monthly, 15 min):** open one random archived episode from Copy 2, confirm the project relinks and the manifest opens. A backup that has never been restored is a hope, not a backup. Also monthly: export the dashboard sheet to CSV into the archive (the kill-switch gate at day 120 runs on this data — losing it means the gate can't fire mechanically, engine §e).

---

## QC gate index (single view — a video must pass all eight to publish)

| # | Gate (owner: SOP) | Pass condition |
|---|---|---|
| G-A | Source pack (SOP-1) | 3 layers, all section-cited; report substantive; manifest started |
| G-B | Outline (SOP-2) | Mechanism cold open; load-bearing diagram; three-layer test |
| G-C | Script (SOP-3) | Citations inline; zero speculation; banned-vocab sweep clean |
| G-D | Fact-check (SOP-4) | Zero unresolved claims; pronunciations verified |
| G-E | Diagrams (SOP-5) | Stylized only; hero frame; "(redrawn)" citations; manifest rows |
| G-F | Narration (SOP-6) | Human voice; 1× listen-back done; levels/loudness met |
| G-G | Edit (SOP-7) | Final watch-through; manifest 100%; −14 LUFS; gates 2+3 visual checks |
| G-H | Package (SOP-8) | Pre-mortem 100% green; disclosure tree = three No's; Test & Compare armed |

A failed gate never advances the video; it either gets fixed inside the remaining weekly hours or the video slips a week (engine §b overrun rule). The printable one-page version of this checklist is `TOOLCHAIN_AND_TEMPLATES.md` §5.
