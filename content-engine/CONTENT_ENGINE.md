# Content Engine — The Operating System of the Channel

**Phase 8 deliverable · 2026-07-13 · Binding documents upstream:** `research/SELECTION_MEMO.md` (memo v2 + four hard gates), `research/keywords/LAUNCH_SLATE.md` (slate + keyword map), `brand/POSITIONING.md` (promise, personas, never-list), `research/validation/census-C09-quiet-catastrophes.json` (census), `research/validation/probe-monetization-policy-status.md` (policy probe). Source IDs (S-numbers) refer to `research/sources/SOURCE_LOG.md`.

This document is written so a stranger can run the channel: pick topics, produce a video in ≤10 hours, publish on schedule, and know exactly when to stop.

---

## (a) Content Pillars & Cadence Rules

The pillars are the failure classes proven by the slate's API-verified demand evidence (`research/keywords/LAUNCH_SLATE.md`, class-diversity check). Every video belongs to exactly one pillar.

| # | Pillar (failure class) | Slate videos | Demand proof (from slate) |
|---|---|---|---|
| P1 | **Bridges & structural collapse** | 1 (Silver Bridge), 2 (Champlain Towers), 9 (Key Bridge) | Hottest lane in the genre: Sunshine Skyway 4.59M+2.96M+1.45M across three channels; I-35W 996k/1.34M/667k; Surfside incumbents 1.52M/909k both pre-NIST-findings |
| P2 | **Fire & life-safety systems** | 3 (MGM Grand) | FH's mechanism-light MGM video: 1.94M views, one of its biggest ever, nothing of quality since |
| P3 | **Rail & ground transport** | 4 (Lac-Mégantic) | 2.58M-view sensational leader = "the exactly-beatable shape"; FH 1.37M, 4.5 yrs old; TSB R13D0054's 18 interlocking causes |
| P4 | **Process, industrial & machinery** | 5 (Texas City), 10 (Sayano-Shushenskaya) | CSB's own animations: 1.92M + 2.18M views vs best indie treatment at 3,272 views — a verified vacuum |
| P5 | **Maritime & offshore** | 6 (Ocean Ranger), 8 (Doña Paz) | BI's Ocean Ranger 4.19M then supply withdrawn (BI pivoted away); Doña Paz = zero coverage across all 8 quality channels pulled |
| P6 | **Dams & geotechnical** | 7 (Buffalo Creek) | Practical Engineering Oroville 5.32M, Teton 1.14M (Apr 2026); Buffalo Creek's only treatment is a 5-yr-old 426k video from PD's weakest era |

### Cadence rules (binding)

1. **One long-form video per week, never more.** Memo v2 §3 sets 1/week as a design requirement; the census natural experiment is the reason — Forgotten Disasters ground every-2-days for 10 months and went dark (18 days silent as of 2026-07-13, memo correction #2), while quality-with-packaging (DisastersUncovered) is the lane's only thriving indie. POSITIONING never-rule #7 makes this a standing prohibition, not a target.
2. **≤2 videos per pillar in any rolling 10** (the slate's own selection rule, extended forward). Prevents the channel drifting into a single-domain channel (Brick Immortar's trap — one domain, then burnout/pivot).
3. **Alternate freshness hooks and evergreen bankers** (slate episode-order logic): never run two freshness-window topics back-to-back; a freshness miss then costs only one slot.
4. **One "diagram showcase" episode per ~5 videos** (slate: eps 5 and 10) — an episode chosen because the mechanism is the star (turbine cross-sections, blowdown-drum flow paths). These build the visual signature that is the channel's thumbnail-visible differentiator (POSITIONING §d2).
5. **The darkness rule:** no massacre-class topics ever, even though they outperform (Bath School: 177k on a 7k-sub channel — traffic deliberately refused; memo v2 surviving objection + POSITIONING never-rule #5). Pillar list above is the complete allowed universe: engineering, process, and systems failures only.

---

## (b) Weekly Production Pipeline — ≤10 hours/video

Memo v2 §3 makes ≤10h/video a **hard economic gate**: the documented modal failure is 15–25h/video at 1/week AdSense-only (bear-case skeptic, accepted as design requirement). The budget below sums to exactly 10.0h. If a stage overruns, the overrun comes out of a later stage or the video slips a week — the weekly slot is never filled with an unfinished video, and cadence is never doubled to catch up.

Every stage has a **quality gate**: a pass/fail check derived from the channel promise (`brand/POSITIONING.md` §a) and the four hard gates (memo v2). A video that fails a gate does not advance.

| Stage | Hours | What happens | Quality gate (pass/fail) |
|---|---|---|---|
| 1. Research & report digest | 2.5 | Pull the named official report (NTSB/CSB/TSB/NIST/inquiry). Run the **report-digest prompt** (`PROMPT_LIBRARY.md` §1) to build the source pack: mechanism chain, decision chain, system findings, key figures/quotes with section citations. Start the per-video asset manifest (hard gate 3). | Source pack maps all three layers (mechanism / decisions / system) to numbered report sections. Every archival asset candidate has license provenance logged. No report of substance = topic killed (promise clause: "if the report doesn't say it, we don't say it"). |
| 2. Outline | 0.5 | Run the **outline prompt** (§2): cold open, three-act structure, diagram list (3–5), report-quote placements. | Three-layer test passes (POSITIONING §a table); ≥1 original diagram is load-bearing to the explanation, not decoration; cold open contains the mechanism hook, not a body count. |
| 3. Script draft | 2.0 | Run the **script-draft prompt** (§3) with voice rules inlined; owner edits to final. Target 1,800–2,600 words ≈ 12–20 min at documentary pace. | Every causal sentence carries an inline report citation `[HAR-71-1 §X]`. Zero speculation beyond the report (never-rule #3). Calm register — no "trapped inside!" framing (never-rule #2). |
| 4. Fact-check pass | 0.5 | Run the **fact-check prompt** (§7) — the script is verified claim-by-claim against the source pack and report. | Zero unresolved claims. Any claim the report doesn't support is deleted or explicitly flagged in-script as outside the findings. This gate is what makes Persona 3 ("they read the actual TSB report") shareable credibility real. |
| 5. Diagrams | 1.5 | Build 3–5 custom failure diagrams from report figures: cross-sections, causal maps, sequence panels. Run the **diagram-brief prompt** (§4) per diagram; assemble in the diagram template kit (reused every week — the kit is why this fits in 1.5h). | Stylized, non-photorealistic only (hard gate 2 — keeps the synthetic-media disclosure label legally unnecessary, probe Task 4 ruling #4). One diagram must be thumbnail-grade (the "hero frame"). Self-made or report-figure derived only — zero rights exposure (hard gate 3). |
| 6. Narration | 1.0 | Owner records the script (hard gate 1: human narration, no TTS ever). One take-through + pickups; noise-clean and level. | Human voice, calm read, correct pronunciations verified during fact-check (PD's mispronunciations are a documented beatable weakness — slate Estonia note). Listen-back at 1× of the full track. |
| 7. Edit & assembly | 1.5 | Assemble narration + diagrams + licensed/PD archival stills in the standing edit template (lower-thirds, map style, quote cards, music bed from a licensed library). Chapter markers added. | No photorealistic AI imagery anywhere (gate 2). No altered/animated archival photos that change what the real event appears to be (gate 3). Asset manifest 100% complete with license provenance before export. |
| 8. Package & publish | 0.5 | Run title/description/tags generator (§6) + thumbnail-concept prompt (§5); run the **packaging pre-mortem checklist** (`PACKAGING_PLAYBOOK.md` §5); upload with 2–3 thumbnail variants for Test & Compare; cut one 60-second mechanism Short from the hero diagram segment (see §f). | Pre-mortem checklist 100% green — it includes the suitability self-certification (§8 prompt) and the synthetic-content disclosure check (answer must be "not required" because the art direction is stylized-exempt; if it isn't, the video violated gate 2 upstream). |
| **Total** | **10.0** | | |

**Weekly rhythm for a solo operator** (one video in flight at a time, one week ahead of publish): Mon = stages 1–2 · Tue = stage 3 · Wed = stages 4–5 · Thu = stages 6–7 · Fri = stage 8 + scheduling · publish Saturday (below). Banking rule: enter launch with episodes 1–3 fully finished (three weeks of pre-launch production), so the buffer absorbs a sick week without breaking cadence.

---

## (c) Publishing Schedule & First-90-Days Calendar

### Day and time — with the honest evidentiary basis

**Default: Saturday, 09:00 ET / 14:00 UK, one long-form per week.** Reasoning from evidence on file:

- The audience is primarily US/UK/CA/AU (decision D-004, `logs/DECISION_LOG.md`). A Saturday-morning ET slot is live before peak weekend viewing in every one of those time zones on the same calendar day.
- 12–20 min documentaries are lean-back content, and lean-back viewing concentrates on TVs and evenings/weekends: YouTube holds a record ~13% share of all US TV viewing (Nielsen Gauge, S053–S056) with 1B+ daily watch-hours on TVs (S058). Publishing a few hours ahead of the weekend couch window lets early engagement accumulate before the highest-appetite session of the week.
- The proven incumbent cadence at the quality end is weekly (Fascinating Horror — weekly cadence, no main upload below ~170k in its last 100; census reference row), and the lane's thriving indie runs ~2×/week max (census). Weekly Saturday matches the audience's trained consumption habit for this format.
- **Stated honestly:** no niche-specific day-of-week performance data exists in the research files (per-slot analytics aren't observable via the API). So the day/time is a *held-constant default, not a validated optimum*: keep it fixed for the first 10 uploads so it never confounds packaging experiments, then test Thursday-evening vs Saturday-morning as a single controlled change in month 4, judged on first-72h views and CTR (see `PACKAGING_PLAYBOOK.md` §6).

### First 90 days — Aug 1 to Oct 30, 2026 (all publishes Saturday 09:00 ET)

Slate order is preserved exactly as argued in `research/keywords/LAUNCH_SLATE.md` (ep 1 = evergreen best-lane banker; ep 2 rides the live post-June-2026 NIST-findings window; ep 3 = the proven-1.94M single-treatment topic; then freshness/evergreen alternation, diagram showcases at 5 and 10).

| Week | Publish date | Long-form (pillar) | Shorts (Tue + Thu, see §f) | Community-tab beat |
|---|---|---|---|---|
| 0 (pre-launch, Jul) | — | Bank eps 1–3 finished; channel art, handle, trailer-free launch (the videos are the trailer) | — | — |
| 1 | Sat Aug 1 | **#1 Silver Bridge** (P1) | S1: eyebar-chain vs wire-cable in 60s · S2: the 0.1-inch flaw | Wed: hero-diagram teaser image + "first video Saturday" |
| 2 | Sat Aug 8 | **#2 Champlain Towers / NIST findings** (P1) | S1: what NIST found in 60s · S2: pool-deck slab detail | Wed: one striking NIST finding as an image card; Sun: "which report should we open next?" poll (options from backlog) |
| 3 | Sat Aug 15 | **#3 MGM Grand fire** (P2) | S1: smoke-path diagram walk · S2: why the sprinklers weren't there | Wed: 1980 fire-code fact card |
| 4 | Sat Aug 22 | **#4 Lac-Mégantic** (P3) | S1: the hand-brake test done wrong · S2: 18 causes in 60 seconds | Wed: TSB causal-web teaser (the 18-cause diagram, cropped) |
| 5 | Sat Aug 29 | **#5 Texas City** (P4 — diagram showcase) | S1: blowdown drum vs flare · S2: the level indicator that lied | Wed: diagram-showcase teaser; Sun: month-1 thank-you + sources thread |
| 6 | Sat Sep 5 | **#6 Ocean Ranger** (P5) | S1: the broken portlight chain · S2: ballast panel logic | Wed: Royal Commission quote card |
| 7 | Sat Sep 12 | **#7 Buffalo Creek** (P6) | S1: three impoundments, one cascade · S2: "flagrant disregard" | Wed: impoundment-cascade diagram teaser |
| 8 | Sat Sep 19 | **#8 Doña Paz** (P5) | S1: why 4,386 couldn't escape (manifest math) · S2: the Vector's paperwork | Wed: poll — pick video 12 from three scored backlog topics (audience sees the rubric working) |
| 9 | Sat Sep 26 | **#9 Key Bridge / NTSB final** (P1) | S1: the loose wire in 60s · S2: what every 2024 video got wrong (calmly) | Wed: NTSB-final-report fact card |
| 10 | Sat Oct 3 | **#10 Sayano-Shushenskaya** (P4 — diagram showcase) | S1: the turbine that jumped (cross-section) · S2: stud-fatigue progression | Wed: turbine cross-section teaser; Sun: slate-complete recap post linking all 10 |
| 11 | Sat Oct 10 | **#11 — first rubric-selected topic** (see §d; leading candidate: Flixborough, P4-adjacent process) | 2 mechanism Shorts | Wed: "how we pick topics" post (publish the rubric — authenticity signal) |
| 12 | Sat Oct 17 | **#12 — rubric-selected** (San Bruno or Estonia, class-rotation dependent) | 2 mechanism Shorts | Wed: diagram teaser |
| 13 | Sat Oct 24 | **#13 — rubric-selected** | 2 mechanism Shorts | Wed: diagram teaser; Sun: day-90 transparency post (views/subs, what's working) |

Community-tab beats begin the moment YouTube enables posts for the channel; until then the same teaser images go into each video's pinned comment. Every long-form description links the named report (the "we read it so you didn't have to" proof) and carries the sources block — the census shows the authenticity-signaling pattern (DisastersUncovered's "No AI. Human Narrated." in every title) is live market defense; ours is the visible report citation plus "Written, narrated, and drawn by a human" in the standing description block.

Day-120 from launch = **Sun Nov 29, 2026**, by which point the schedule above yields 17 published, fully packaged videos — comfortably clearing the kill-switch precondition of ≥15 (memo v2 gate 4). The checkpoint is pre-scheduled in §e.

---

## (d) Topic Selection System for Video 11+

Run this system in week N−3 for the video publishing in week N. It exists so topic choice never regresses to taste. Feed it candidates from: the validated backlog (`research/keywords/LAUNCH_SLATE.md`, next 14), new official-report releases (NTSB/CSB/TSB/NIST RSS — a fresh final report on a known event is the strongest hook the slate found, cf. eps 2 and 9), and audience comments requesting events.

### Step 1 — Suitability gate (pass/fail, before any scoring)

All six must pass. Any fail = topic rejected permanently or deferred, logged with reason.

| Gate | Test |
|---|---|
| G1 Failure-class | Engineering / process / systems failure. **Never** massacre-class: no school attacks, shootings, terrorism, deliberate killings (POSITIONING never-rule #5 — binding even though these outperform). |
| G2 Report exists | A named official investigation of substance (NTSB, CSB, TSB, NIST, MAIB, Royal Commission, court of inquiry). No report → no video (promise clause a). |
| G3 Non-graphic treatable | The story can be told to the channel's standard with zero graphic imagery and zero victim sensationalism (never-rules #1–2; the ad-suitability mitigation that keeps FH-class channels monetized for 7 years — census Q3). |
| G4 Rights-clean assets | Public-domain / openly licensed archival + report figures + self-made diagrams cover the visual needs (hard gate 3). Agency press imagery dependence = fail. |
| G5 Class rotation | Does not create a 3rd video in one pillar within the rolling last 10 (§a rule 2). |
| G6 No live litigation/raw grief | Event is either historical or has reached its official-findings stage (the slate's recent entries — Surfside, Key Bridge — are eligible *because* final findings exist; framing is strictly the engineering record). |

### Step 2 — Scoring rubric (100 points; greenlight ≥70, backlog 50–69, drop <50)

| Criterion | Pts | How to score it (evidence required, not vibes) |
|---|---|---|
| **Search/demand evidence** | 30 | API-verified views on the exact topic or a tight class comp. 25–30: ≥1M views on existing treatments or proven class breakouts (e.g., Sunshine Skyway 4.59M/2.96M/1.45M). 15–24: 300k–1M. 5–14: 100k–300k or strong comp only. 0–4: unproven demand. *Method: yt-dlp / Data API videos.list on the top existing treatments; log the numbers.* |
| **Coverage gap** | 20 | 16–20: verified vacuum (best indie treatment <10k views, like Texas City's 3,272) or every big treatment factually obsolete (post-report freshness gap, like Champlain/Key Bridge). 8–15: single dated or mechanism-light treatment (MGM shape). 0–7: ≥2 recent quality treatments (saturated — the census shows marquee topics absorb 2–3, so 2 recent = marginal). |
| **Report richness** | 25 | 20–25: multi-layer report with mechanism + decision chain + systemic findings (TSB R13D0054's 18 causes = the benchmark). 10–19: solid mechanism, thinner decision chain. 0–9: findings summary only — weak moat. |
| **Diagram potential** | 10 | 8–10: the mechanism is inherently visual (turbine cross-section, smoke path, eyebar fracture). 4–7: diagrammable with effort. 0–3: abstract (the signature asset has nothing to show). |
| **Class rotation bonus** | 10 | 10: opens a pillar not covered in the last 5 videos. 5: last covered 3–4 back. 0: covered within last 2. |
| **Freshness hook** | 5 | 5: report released/updated in the last 12 months or a dated anniversary/news peg. 0: pure evergreen (fine — bankers score their points elsewhere). |

**Tie-breaks:** (1) higher demand-evidence score wins; (2) evergreen banker wins if the last video was a freshness play (cadence rule 3); (3) the topic whose report the operator can digest fastest (protects the 10h budget).

### Worked example — scoring Flixborough 1974 (backlog) for slot #11

Evidence from `research/keywords/slate-proposals-report-vault.json`: PD's single treatment has 998,882 views (Jul 2022); era/geography comps Ronan Point FH 2.73M + PD 1.75M; Court of Inquiry report (HMSO 1975) with the famous "chalk sketch on the workshop floor" decision chain; bellows/bypass-pipe mechanism is a perfect diagram set piece.

| Criterion | Score | Why |
|---|---|---|
| Suitability gate | PASS | Industrial explosion, 52 yrs old, rich official report, PD-only imagery needs, process class last used at slot 10 → G5 check: Sayano is machinery (P4)… Flixborough is also P4, but slots 5 & 10 are the only P4 in the rolling 10 and slot 5 rolls out at video 15 — passes with a note to rotate P4 out afterward |
| Demand evidence | 24/30 | 998,882 on one dated treatment + 1.7–2.7M class comps; just under the ≥1M-on-topic bar |
| Coverage gap | 16/20 | Single 4-year-old fast-collage treatment, mechanism-light — "softest target on this list" per the proposal file |
| Report richness | 22/25 | Court of Inquiry: mechanism (bellows failure) + decision chain (no engineer on site, chalk-sketch design) + system layer (birth of UK process-safety regulation) |
| Diagram potential | 9/10 | Dog-leg bypass assembly + vapour-cloud propagation — signature material |
| Class rotation | 5/10 | P4 covered at slot 10 (3 back by publish) |
| Freshness | 0/5 | Pure evergreen |
| **Total** | **76/100** | **Greenlight** — schedule as video 11 |

Log every scored topic (including rejects) in `content-engine/topic-log` rows: date, topic, gate results, scores, decision. The rejects list is the audit trail that keeps the darkness rule honest.

---

## (e) Kill-Switch Metrics Dashboard (memo v2, hard gate 4)

Gate 4 verbatim: *at day 120 with ≥15 published, fully-packaged videos: if the trailing-10 median is under ~8k views or projected annualized revenue is under a defined floor, execute the C23 pivot playbook rather than zombie-grinding.* This section makes that executable.

### The revenue floor, defined

**Floor: projected annualized gross channel revenue < $7,200/yr (≈$600/mo run-rate, all legs combined).** Basis: memo v2 documents the modal failure as "1–5k views/upload ≈ $200–600/mo gross — economic failure" (bear-case skeptic, accepted). $600/mo is the *top* of the documented failure band; projecting at or below it at day 120 means the channel is living inside the failure mode. The Phase-10 monetization model (`monetization/`) may **raise** this floor; it may never lower it. Projection method: (trailing-8-week actual revenue across AdSense + memberships/Patreon + any sponsor income) ÷ 8 × 52.

### Dashboard spec (one spreadsheet, `content-engine/dashboard` — Google Sheets or CSV, updated every Monday, 30 min)

**Tab 1 — Per-video ledger** (one row per long-form, from YouTube Studio):

| Column | Source | Why it's on the dashboard |
|---|---|---|
| Publish date, title, pillar | — | Class-rotation audit |
| Views: 72h / 7d / 28d / cumulative | Studio | Feeds trailing-10 median |
| Impressions + CTR (7d, 28d) | Studio | Packaging health (playbook thresholds) |
| Avg view duration + avg % viewed | Studio | Retention health (playbook thresholds) |
| Browse / Suggested / Search % of traffic | Studio → Reach | Memo correction #4: browse/suggested is the primary growth channel; search is assist. A collapse in browse share is the Disaster Digest early-warning pattern (census: early traction revoked) |
| Production hours actual | timer log | ≤10h gate audit — hours creep is the silent killer of the economics |
| Test & Compare winner + CTR lift | Studio | Packaging iteration record |

**Tab 2 — Channel health (weekly row):**

| Metric | Definition | Amber | Red (feeds the gate) |
|---|---|---|---|
| **Trailing-10 median views** | Median 28d-normalized views of the last 10 long-forms (use current views for videos <28d old, flagged) | <8k at day 60 | **<8k at day 120 → GATE FIRES** |
| Trailing-10 median trend | This week vs 4 weeks ago | Declining 4 weeks straight | — |
| Projected annualized revenue | Formula above | <$7,200 at day 90 | **<$7,200 at day 120 → GATE FIRES** |
| Subs, watch hours (trailing 365d) | Studio | — | YPP progress tracker (1,000 subs + 4,000 hrs, or the 500-sub/3,000-hr lower tier — S078/S079) |
| Shorts→long-form conversion | Views on long-form attributed to Shorts end-screens/related | — | Informational (see §f) |
| Median outlier check | Best/worst video vs median | — | A single breakout must not mask a dead median — the gate runs on the **median**, not the mean, precisely so one Aberfan-style spike (478k, census) can't hide nine 1k-view videos |

**Tab 3 — Checkpoint log** (pre-scheduled, written up even if all green):

- **Day 30 (Aug 31):** baseline snapshot. No decisions — the census shows early traction is uninformative in both directions (Disaster Digest had ~1M views before collapsing to sub-500/upload).
- **Day 60 (Sep 30):** amber review. If trailing-10 median <4k AND browse share falling, pull the two worst performers into the repackaging loop (`PACKAGING_PLAYBOOK.md` §6) and re-score the next 3 topics for demand-evidence weight. No pivot decision — packaging fixes get 60 days to work, because the census attributes breakout separation to packaging craft (memo v2 §4).
- **Day 90 (Oct 30):** revenue-floor pre-read. Compute the projection for the first time with 8 weeks of data. If below floor, spend weeks 14–17 on the strongest-demand backlog topics only (no experiments).
- **Day 120 (Nov 29) — THE GATE.** Preconditions verified: ≥15 published fully-packaged videos (schedule delivers 17). Test: trailing-10 median <8k **OR** projected annualized revenue <$7,200. Either true → **execute the C23 pivot playbook** (memo v2 fallback: C23 Relocation Report with shown-methodology defense from video 1). Neither true → write the continuation memo with next-90-day targets and proceed.

### Pivot-playbook trigger protocol (so firing the gate is mechanical, not a mood)

1. The day-120 review is a calendar appointment created at launch (not movable; the memo's critique of v1 was a kill-switch that could never fire).
2. The two gate numbers are computed from the dashboard by formula — no judgment inputs.
3. If fired: no new disaster videos enter production. The catalog stays up (evergreen AdSense continues — the memo's worst-case logic: a living channel that can iterate). Week 1 post-fire: C23 channel setup + methodology video script. The disaster channel becomes a maintenance asset, not a grind.
4. If the gate *almost* fires (median 8–10k or revenue within 15% of floor): continuation is allowed only with a written diagnosis naming which pipeline stage or packaging pattern will change, and a hard re-check at day 180.

---

## (f) Shorts & Derivative Strategy — 60-Second Mechanism Clips

**Role: discovery surface and YPP accelerant, never a revenue line.** Per D-003 (`logs/DECISION_LOG.md`): long-form first; Shorts are derivative promotion — long-form carries ~10× the watch-time RPM, and Shorts RPM is $0.01–0.06 (S051). The reach case: Shorts average 200B daily views platform-wide (S058/S059) — it is the cheapest cold-audience surface available to a zero-subscriber channel.

**Format — the mechanism clip:** 45–60 seconds, vertical reframe of the week's hero diagram segment. Structure: (1) 0–3s: the diagram already moving + one-line mechanism hook ("This half-inch flaw dropped a 700-meter bridge"); (2) 3–45s: the single failure mechanism explained on the diagram — one mechanism only, never the whole story; (3) 45–60s: the unresolved layer as the pull — "*why* nobody inspected it is the real story — full breakdown on the channel." Human narration re-used from the long-form track or re-recorded in one pass (gate 1 applies to Shorts identically; all four hard gates do).

**Cadence: 2 per long-form, published Tue + Thu** (between Saturday long-forms, keeping the channel surfaced midweek). Production cost: Short #1 is cut inside stage 8 of the pipeline (budgeted); Short #2 is cut from the same timeline in ≤20 min or skipped — Shorts are never allowed to breach the 10h budget or delay a long-form (cadence rule 1 protects long-form; this rule protects it from Shorts).

**Why mechanism clips and not story clips:** the diagram is the only asset that makes the channel's positioning visible in 3 seconds (POSITIONING §d2), it is the asset AI-slop competitors can't cheaply fake (census: the slop flood is the lane's live threat), and a story-fragment Short would compete on the sensational register we've sworn off (never-rule #2) — a mechanism Short *cannot* be sensational.

**Measurement:** Shorts are judged only on (a) Shorts views counting toward the YPP lower-tier threshold (3M Shorts views/90 days alternative path — S079) and (b) long-form traffic attributed to Shorts viewers (dashboard Tab 2). If after 90 days Shorts drive <2% of long-form views and negligible YPP progress, cut to 1/week and reinvest the time in diagrams — the dashboard decides, not sentiment.

**Other derivatives (deferred, revisit at day 120 if the gate doesn't fire):** community-tab diagram cards (already scheduled, §c); a "sources & further reading" standing block in every description (zero marginal cost, feeds Persona 3); podcast/audio re-use is explicitly out — the narration without diagrams breaks the promise ("drawn so you can see it") and adds a platform for no evidenced demand.
