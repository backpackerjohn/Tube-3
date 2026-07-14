# Brand Guidelines — MODE OF FAILURE

**Deliverable 2a · 2026-07-13 · Binding on all scripts, packaging, and assets (Phases 7–10).**
Everything here is downstream of the four hard gates in `research/SELECTION_MEMO.md` (human narration · stylized non-photorealistic art · archival rights protocol · payback kill-switch). Where a rule below conflicts with anything else, the gates win.

---

## 1. Channel name

### 1.1 Candidates proposed (12) and availability checks

Handle availability was checked on **2026-07-13** via YouTube Data API v3 `channels.list?forHandle=` (an empty `items` array = handle unregistered; a returned channel = taken). Trademark/brand collisions were web-checked for every shortlisted name. Raw results:

| # | Candidate | Handle checked | API result | Web/trademark check | Verdict |
|---|-----------|----------------|------------|---------------------|---------|
| 1 | Mode of Failure | @ModeOfFailure | **0 items — AVAILABLE** | No branded show/podcast/product found in search | **WINNER** |
| 2 | The Accident Report | @TheAccidentReport | **0 items — AVAILABLE** | No branded collision found (adjacent shows exist: "The Crash Report" podcast, "PreAccident Investigation Podcast" — different names) | **RUNNER-UP 1** |
| 3 | The Cause File | @TheCauseFile | **0 items — AVAILABLE** | No direct collision; phonetically near "Casefile" (major true-crime podcast + YouTube channel) — noted risk | **RUNNER-UP 2** |
| 4 | Failure Files | @FailureFiles | 0 items — available | **COLLISION:** "Failure Files™" is a trademark-claimed AI-governance case library (Human Signal / humansignal.io) AND an existing IDR podcast on Spotify | Rejected on trademark |
| 5 | The Failure Report | @TheFailureReport | 0 items — available | **COLLISION:** "The Failure Report Podcast" exists on Apple Podcasts / iHeart / Instagram (@thefailurereport) | Rejected on collision |
| 6 | Failure Mode | @FailureMode | TAKEN (channel "Failure Mode", created 2023) | — | Rejected |
| 7 | Point of Failure | @PointOfFailure | TAKEN ("POINT OF FAILURE", created 2025-12) | — | Rejected |
| 8 | How It Failed | @HowItFailed | TAKEN (created 2023) | — | Rejected |
| 9 | Causal Chain | @CausalChain | TAKEN (created 2025-04) | — | Rejected |
| 10 | Blueprint of Disaster | @BlueprintOfDisaster | TAKEN (created 2013) | Also collides with Discovery-era TV series "Blueprint for Disaster" | Rejected |
| 11 | Fracture Point | @FracturePoint | TAKEN (created 2024) | — | Rejected |
| 12 | Margin of Failure | @MarginOfFailure | TAKEN (created 2021) | — | Rejected |

Additional probes run while mapping the namespace (same API method, same date): @TheFinalReport TAKEN (2010) · @LoadPath TAKEN (590 subs) · @TheFailureFiles TAKEN · @DisasterForensics TAKEN (zero-sub channel created **2026-05-25**) · @FailureForensics TAKEN (zero-sub, created 2025-08) · @FailureMechanics TAKEN (zero-sub, created 2025-10) · @AnatomyOfFailure TAKEN (zero-sub, created **2026-07-09 — four days ago**) · @ChainOfFailure TAKEN (zero-sub, created 2026-04) · @TheEyebarFiles available but too obscure to carry a channel.

> **Urgency finding:** five zero-subscriber channels squatting exact forensic-failure names were registered between Aug 2025 and Jul 2026 — the naming space is being actively claimed, almost certainly by AI-slop operators circling the niche (consistent with the in-lane AI flood documented in `research/validation/census-C09-quiet-catastrophes.json`). **Register @ModeOfFailure the day the Google account is created, before any other launch step.**

### 1.2 The decision

- **WINNER: Mode of Failure** — handle **@ModeOfFailure**
- **Runner-up 1: The Accident Report** — handle **@TheAccidentReport**
- **Runner-up 2: The Cause File** — handle **@TheCauseFile**

If @ModeOfFailure is somehow lost between now and account creation, fall to runner-up 1 without re-litigating.

### 1.3 Naming rationale

1. **It is the thesis in three words.** The selection memo's differentiator is the forensic/engineering spine — the *why-it-happened* layer incumbents keep light (`SELECTION_MEMO.md` §"The confirmed thesis", point 2). "Failure mode" is the literal engineering term for how a component or system fails (as in FMEA — failure mode and effects analysis). Inverting it to *Mode of Failure* makes the term ownable and brandable while keeping the engineering register intact. Every episode delivers, concretely, the mode of failure.
2. **It targets the channel's home keyword cluster.** The keyword map (`research/keywords/LAUNCH_SLATE.md`) identifies *engineering failure* as the best-economics cluster measured (engineering disasters 58.6k/mo, competition 42.5). The name signals engineering-failure content to both viewers and the recommendation system's topic modeling without squatting a generic search phrase (the census shows keyword-squatting names earn nothing: two "Disaster Documentaries" channels sat on the exact niche phrase for 6+ years at 835 and 234 subs — `census-C09-quiet-catastrophes.json`).
3. **It is calm by construction.** No "horror", "dark", "terrifying", "doomed" — the sensational register the house style must resist (memo: growth gradient bends toward darker topics; the name is a standing brake on that pull). It reads like a report chapter heading, which is the brand promise.
4. **It works spoken.** The narration sign-off writes itself: *"…and that was the mode of failure."* A verbal brand stamp at zero cost, in the owner's human voice (gate 1).
5. **Accepted risk, documented:** the census cohort contains "Mode of Horror" (22.6k subs, industrial-disaster docs, plateaued 2021 entrant). The shared "Mode of—" construction is a mild confusability risk. Accepted because (a) the overlap word is the generic one, (b) the registers diverge completely (Horror vs Failure — our name is the anti-sensational statement), and (c) every distinctive alternative in the namespace is either taken or trademark-encumbered. If viewer-comment confusion actually materializes in the first 90 days, the fallback is runner-up 1.

Why the runners-up rank where they do: *The Accident Report* is the strongest pure authority signal (the moat **is** official accident reports) but is generic, weakly protectable, and near-invisible in a subscription feed. *The Cause File* is distinctive but phonetically shadows Casefile, a much larger true-crime brand — a discoverability leak we don't need.

---

## 2. Voice & tone guide

**The register in one sentence:** a good accident investigator briefing an intelligent lay audience — calm, precise, mechanism-first, respectful of the dead, and never more certain than the report is.

**Evidence base for this register:** the niche's one thriving young indie (DisastersUncovered) and the marquee incumbent (Fascinating Horror) both run calm narration and a no-graphic-imagery house style — FH's stated approach, per the census — and FH monetizes for 7+ years on it; meanwhile the census's sensationalist entries are exactly what we out-flank (Lac-Mégantic's 2.58M-view leader is "a sensationalist non-forensic video (the exactly-beatable shape)" — `LAUNCH_SLATE.md` row 4). The memo also binds us: house-style rules must resist the pull toward darker framing to protect ad suitability (`SELECTION_MEMO.md`, surviving objections). Tragedy content sits in limited-ads territory under YouTube's advertiser guidelines (census Q3; support.google.com/youtube/answer/6162278) — this voice guide is the mitigation.

### The 10 rules, each with a before → after

1. **Lead with the mechanism, not the body count.** Deaths are stated once, precisely, with sourcing — never as the hook.
   - ✗ *"85 people never stood a chance in the deadliest hotel inferno in Vegas history."*
   - ✓ *"The fire itself was out in minutes. What traveled through the building for the next half hour was smoke — and the building had been designed, legally, with no way to stop it."*

2. **Attribute every causal claim to the investigation.** The report is the narrator's authority; borrow it explicitly, at least once per act.
   - ✗ *"Investigators would later be stunned by what they found."*
   - ✓ *"The NTSB's metallurgists sectioned eyebar 330. Inside the eye, they found a crack twelve one-hundredths of an inch deep — Highway Accident Report 71-1, page 34."*

3. **Numbers over adjectives.** Delete intensifiers; replace each with a measurement, a time, or a count. (This is also the packaging finding: "numbers and mechanisms outperform adjectives" — `LAUNCH_SLATE.md`, title formula.)
   - ✗ *"The tank was massively, dangerously overfilled."*
   - ✓ *"The tower was designed to hold 6.5 feet of liquid. By 1:04 p.m. it held 158 feet."*

4. **Respect for the dead: named people act, they are never props.** Individuals appear when their decisions or testimony matter to the mechanism; suffering is never described graphically or lingered on.
   - ✗ *"Passengers clawed at the locked gates as the water rose, their screams echoing…"*
   - ✓ *"The manifest said 1,583 people were aboard. The court record would eventually establish more than 4,000. Most were asleep when the tanker struck."*

5. **No false suspense about settled facts.** Tension comes from the decision chain, not from withholding what the report established decades ago.
   - ✗ *"What happened next would shock the world… but to understand it, we have to go back."*
   - ✓ *"The bridge fell in thirteen seconds. The reason it fell took the NTSB three years to isolate — and it was smaller than a fingernail."*

6. **Blame systems precisely, people carefully.** Individual error is reported in the report's own language; the narrative weight lands on the system that made the error fatal.
   - ✗ *"One careless engineer's stupidity killed 47 people."*
   - ✓ *"The engineer set seven hand brakes. The rule book said the number needed was 'sufficient' — a word the TSB found had no agreed meaning anywhere in the company."*

7. **Plain grammar, short sentences at load-bearing moments.** The sentence rhythm slows and simplifies exactly where the failure happens.
   - ✗ *"Owing to the confluence of residual stresses and the pre-existing flaw, catastrophic fracture propagation ensued."*
   - ✓ *"The crack had been growing for forty years. That night, it finished."*

8. **Mark uncertainty honestly.** Where the report says "probable" or dissents exist, the narration says so — certainty-laundering is the sensationalist tell.
   - ✗ *"This is what happened in those final seconds."*
   - ✓ *"No one survived the compartment, so the sequence here is the Commission's reconstruction — its probable cause, not a recording."*

9. **The present tense is for the timeline; the past tense is for the record.** Reconstruction sequences run in present tense ("the relief valve opens"); findings and aftermath in past tense ("the Board found"). Never dramatized dialogue that isn't in a transcript.
   - ✗ *"'We're not going to make it!' the foreman screamed."*
   - ✓ *"At 11:57 the foreman radios the office. The transcript records four words: 'the water's coming over.'"*

10. **End on the fix, not the wound.** Every episode's final act is what changed — the code, the regulation, the design practice — because that is the genre's payoff and its ad-suitability armor (historical, educational, non-graphic treatment is explicitly the monetizable register — census Q3).
    - ✗ *"…a tragedy that haunts Point Pleasant to this day."*
    - ✓ *"Within four years, Congress had ordered the inspection of every bridge in America. The National Bridge Inspection Standards exist because eyebar 330 cracked — and because, for forty years, no one could see it."*

**Banned vocabulary list** (use in QA pass on every script): *horrifying, terrifying, nightmare, doomed, deathtrap, shocking, insane, unbelievable, chilling, gruesome, haunting* — plus any second-person dare ("you won't believe"). Permitted strong words when the report itself uses them (e.g., Buffalo Creek's commission wrote "flagrant disregard" — quote it, cite it).

---

## 3. Visual identity

**Design concept: the investigation drawing.** Every surface of the brand looks like a figure lifted from a beautifully drafted accident report — blueprint linework on dark paper, one element marked in red. This is the compliance-optimal art direction, not just an aesthetic choice: stylized/illustrated imagery is exempt from YouTube's synthetic-media disclosure label, while photorealistic AI scene generation would require it (`probe-monetization-policy-status.md`, Task 4, formats 3 vs 4; gate 2 of the memo).

### 3.1 Palette (hex)

| Role | Name | Hex | Usage |
|------|------|-----|-------|
| Primary background | **Report Navy** | `#0D1B2A` | All diagrams, thumbnails, end cards, banner base |
| Secondary surface | **Blueprint Blue** | `#1B4965` | Panels, callout boxes, banner gradient, hover states |
| Primary linework | **Drafting Cyan** | `#5FA8D3` | Diagram lines, grids, structural outlines |
| Text / paper | **Paper White** | `#E8EDF2` | All body text, labels, dimension lines |
| Failure mark | **Signal Red** | `#C1494B` | ONE element per composition: the failing component, crack path, or breach point. Never used decoratively. |
| Class accent A | **Caution Amber** | `#E0A458` | Fire / explosion / process class coding (see 3.4) |
| Class accent B | **Gauge Green** | `#6A994E` | Transport / machinery / maritime class coding |

Rules: Signal Red appears exactly once per thumbnail/diagram — scarcity is what makes the eye find the failure. Never place Drafting Cyan text on Blueprint Blue (contrast fails); text is always Paper White or Report Navy. No pure black, no pure white anywhere — the drawing-on-paper illusion depends on it.

### 3.2 Typography (2 free fonts)

- **Display / titles / thumbnails: Archivo** (SIL Open Font License, Google Fonts). Weights: Black for thumbnail text and episode titles, Semibold for section cards. Set tight (-2% tracking), always Paper White or Signal Red.
- **Technical / annotations / everything inside diagrams: IBM Plex Mono** (SIL OFL, Google Fonts). Regular for labels and dimensions, Medium for callout numbers, Italic for report citations. The mono font *is* the forensic voice in visual form — every number on screen is set in it.

No third font, ever. Narration subtitles use Archivo Regular.

### 3.3 Failure-diagram style rules (the visual signature)

The custom failure diagram is the channel's signature asset (memo thesis). Every diagram obeys:

1. **Line weights, three and only three:** 3 px Drafting Cyan for the primary subject outline · 1.5 px at 60% opacity for secondary structure/context · 0.75 px at 25% opacity for the background grid (50 px module) and dimension lines. The failure element is redrawn in 3 px Signal Red.
2. **Labeling:** every labeled part gets a numbered circular tag (IBM Plex Mono Medium, Paper White numeral in a 1.5 px cyan circle), with a legend strip along the bottom edge. Leader lines run at 45° or 90° only, never curved, never crossing each other.
3. **Annotation conventions:** dimensions in the unit the report uses (with metric/imperial conversion in parentheses); timestamps as `T+0:00:13` relative to initiation; forces/pressures/temperatures always sourced — each diagram carries a citation line bottom-right in Plex Mono Italic: `Source: NTSB HAR-71-1, Fig. 12 (redrawn)`.
4. **Sequence diagrams** (the "how it progressed" money shot): 3–5 stacked frames of the same drawing, state advancing left→right or top→bottom, red element growing/propagating frame to frame; frame labels `STATE 1 — AS DESIGNED`, `STATE 2 — AS BUILT`, `STATE 3 — AT FAILURE`.
5. **Never depicted:** human figures in distress, bodies, blood, personal effects of victims. Humans appear only as neutral scale silhouettes (solid Blueprint Blue, no faces) when scale matters.
6. **Provenance:** diagrams are self-drawn (rights-clean by construction, gate 3), *based on* report figures — "redrawn" in the citation is literal and load-bearing. Original report figures may appear on screen as documents (see lower-thirds), but the signature diagrams are ours.

### 3.4 Thumbnail system

Evidence anchors: the census attributes breakout separation in this cohort to title/thumbnail craft (memo, thesis point 4 — DisastersUncovered vs Mode of Horror natural experiment), and the cohort's winning packaging is calm-forensic, not shock-face — the thriving channels here are faceless diagram/photo-led (`census-C09-quiet-catastrophes.json`); the title formula work in `LAUNCH_SLATE.md` found numbers/mechanisms outperform adjectives. The system:

- **Canvas:** 1280×720. **Composition grid:** vertical thirds. Right two-thirds = the image (one failure diagram OR one treated archival photo per gate 3). Left third = text block. Bottom 8% = class-color strip (see coding below) with the episode's `T+` timestamp or key number reversed out in Plex Mono.
- **Text: 4 words maximum,** Archivo Black, Paper White, max 2 lines, one word may be Signal Red (the mechanism word: ONE EYEBAR · THE SMOKE · 72 BRAKES). Never repeat the title verbatim; the thumbnail says the mechanism, the title carries the searchable event name (keyword map rule).
- **One red mark per thumbnail:** a Signal Red circle, arrow, or crack-path on the failure location. This is the brand's recurring visual hook — over a browse page of our catalog, the red mark is the identity.
- **Color coding by failure class** (the bottom strip + diagram accent): **Drafting Cyan** = structural/civil (bridges, dams, buildings — slate #1, 2, 7, 9) · **Caution Amber** = fire/explosion/process (slate #3, 5) · **Gauge Green** = transport/machinery/maritime (slate #4, 6, 8, 10).
- **Hard bans:** NO shock faces, no open-mouth reaction insets, no red-yellow "MAYDAY" gradient text, no fake flames, no arrows pointing at nothing, no AI-photorealistic disaster renders (disclosure-label trigger, gate 2). Archival photos in thumbnails must pass the gate-3 rights protocol and must not be altered in ways that change what the event appears to be (probe Task 4, format 2 tripwire (a)).

### 3.5 End-card spec

- Final 20 seconds of every video, 1280×720 design space. Background: Report Navy with the 50 px blueprint grid at 15% opacity.
- Layout: left 55% — two stacked video end-screen slots (each 410×230 export, 1.5 px Drafting Cyan border, 4 px corner radius), labeled above in Plex Mono: `RELATED FAILURE //`. Right 40% — channel avatar (subscribe element, 196×196) over the line *"Researched, written, and narrated by a human."* in Archivo Semibold 28 pt, and the class-color strip along the bottom carrying the episode's citation: `Primary source: [report ID]`.
- Audio: narration ends before the card; music bed only. The verbal sign-off (*"…and that was the mode of failure."*) lands as the card appears.

### 3.6 Lower-third spec

Two variants, both anchored bottom-left, safe within 10% title-safe margins, in-out animation = 200 ms slide+fade (no bounces):

- **Citation lower-third** (the credibility signature — used every time a report finding is quoted): single line, Plex Mono Regular 24 pt Paper White on a Blueprint Blue bar at 85% opacity, 8 px Signal Red left edge. Text pattern: `NTSB HAR-71-1 · p.34 · "probable cause"`.
- **Context lower-third** (dates/places/people): two lines — line 1 Archivo Semibold 30 pt (name/place), line 2 Plex Mono 22 pt (role/date). Same bar, Drafting Cyan edge instead of red.

---

## 4. "Human narrated" statement policy

**The policy exists because the market already proved it matters:** the lane's one thriving young indie, DisastersUncovered, stamps "No AI. Human Narrated." into every single title as a survival defense against the in-lane AI flood and the 2025–26 demonetization wave (census, cohort row 1 + Q3; memo gate 1). Faceless human creators are documented collateral damage of that wave (Hollywood Reporter / TheNextWeb, cited in census sources; Doctor NOS and French Whisperer cases in `probe-monetization-policy-status.md` Task 3). The statement is therefore a **standing brand asset**, deployed as follows:

1. **The canonical statement (use verbatim everywhere):**
   > **Researched, written, and narrated by a human.**
   Short form where space is tight: `Human narrated. No AI voice.`
2. **Always-on placements:** line 1 of every video description (above the fold, before the summary) · the About page (§ opening, see `ABOUT_AND_TRAILER.md`) · the banner tagline area · the end-card of every video (§3.5) · spoken once in the channel trailer.
3. **Titles stay clean — with a defined escalation trigger.** Unlike DisastersUncovered we do NOT spend title characters on the stamp by default: our title formula needs every character for mechanism + event keyword (`LAUNCH_SLATE.md` title formula), and the stamp's job is done by description line 1, which YouTube surfaces in search snippets. **Escalation trigger:** if (a) a synthetic-media/AI flag or limited-ads decision ever hits the channel, or (b) two consecutive months of comment/community evidence show viewers mistaking the channel for AI, append the suffix ` | Human Narrated` to all future titles until resolved. Decision logged here so it isn't relitigated under stress.
4. **Truthfulness boundary (this is a compliance statement, so it must be exactly true):** the claim covers narration (owner-recorded, gate 1), writing, and research. AI assistance for research organization, drafting support, or diagram tooling is permitted under YouTube's rules ("production assistance" is explicitly exempt from disclosure — probe Task 4) and does **not** falsify the statement, but the statement must never expand to "no AI used" — it says exactly what is human: the research judgment, the words as delivered, and the voice. If narration is ever outsourced, it goes to a named human narrator and the statement stays true; it never goes to TTS (gate 1, hard).
5. **On-video proof-of-human:** the narrator sign-off formula (*"I read the full [N]-page report so you don't have to — sources below. And that was the mode of failure."*) plus owner-voice replies pinned in comments on each premiere. The census/probe evidence (Dr. Jonathan Tam case, probe Task 2) shows an accountable human presence is what converts faceless format into "authentic" under the 2026 enforcement climate — we adopt the accountable-faceless posture: real voice, consistent sign-off, no on-camera requirement.

---

## 5. One-page brand card (pin this above the edit bay)

- **Name:** Mode of Failure · **@ModeOfFailure** · register the handle FIRST.
- **Promise:** *How it actually failed — from the official report.*
- **Voice:** investigator, not storyteller of horrors. Numbers over adjectives. End on the fix.
- **Look:** blueprint linework on Report Navy `#0D1B2A`; one Signal Red `#C1494B` mark per frame; Archivo + IBM Plex Mono; class colors cyan/amber/green.
- **Never:** shock faces · TTS narration · photorealistic AI scenes · unlicensed agency photos · body-count hooks · certainty the report doesn't have.
- **Always:** citation lower-thirds · human-narrated statement in description line 1 · red mark on the failure · the sign-off.
