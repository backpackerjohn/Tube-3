# Packaging Playbook — Titles, Thumbnails, and the Iteration Loop

**Phase 8 deliverable · 2026-07-13.** Memo v2 §4 makes packaging a **first-class system**: "the census attributes breakout separation to title/thumbnail craft." This playbook is that system. It pairs with `PROMPT_LIBRARY.md` prompts 5 (thumbnail) and 6 (title/description/tags) and feeds the dashboard in `CONTENT_ENGINE.md` §e.

## 1. Why packaging gets its own operating manual (the evidence)

- **The natural experiment:** Mode of Horror — same format, 4 years in, 53 videos — plateaued at 22.6k subs, while DisastersUncovered reached 26.6k subs in 18 months with uploads repeatedly clearing 100k views; the census and memo v2 attribute the separation to packaging craft, not topic access (census; memo v2 §3 "quality-with-packaging beats volume").
- **Topic selection alone transfers nothing:** the census's long-tail finding — identical topic classes pull 1–3 orders of magnitude differently by channel (Mount Pelée, 30,000 dead: 2,213 views) — means the impression, not the archive, is the product's front door.
- **The cautionary tail:** Disaster Digest got ~1M lifetime views, then collapsed to 62–820 views/upload (census). Early traction is revocable; sustained CTR/retention performance is the only defense a small channel controls weekly.
- **Discovery mix:** memo correction #4 downgraded search to "adequate, search-assisted; browse/suggested is the primary growth channel." Browse and suggested are *packaging-judged* surfaces — CTR against an impression is the whole game there.

**Standing constraint over everything below:** never clickbait beyond what the report supports (POSITIONING never-rule #6). The packaging ceiling is the report's own drama — which, in this genre, is high.

---

## 2. Title system

### 2.1 The base formula (slate, cohort packaging analysis)

> **[Concrete mechanism or number] + [human stakes] + [event name]**
> "Numbers and mechanisms outperform adjectives; the event name carries the search keyword; never clickbait beyond what the report supports." — `research/keywords/LAUNCH_SLATE.md`

Non-negotiable mechanics (enforced by prompt 6, checked in the pre-mortem):

- Primary keyword (slate keyword map, per-video bold phrase) or a close variant appears in the title, inside the first 60 characters.
- 45–70 characters preferred.
- Banned vocabulary: "horrifying", "terrifying", "shocking", "nightmare", "you won't believe", "caught on camera".
- Never imply brand affiliation ("Seconds From Disaster" is a NatGeo trademark — slate keyword map).
- Every title claim must survive the fact-check pass (a number in the title is a claim).

### 2.2 The four formulas, with the evidence behind each

| # | Formula | Shape | Evidence on file | When to use |
|---|---|---|---|---|
| F1 | **Mechanism-Number** | `[Number/mechanism], [count/stakes]: [why/event]` | The lane's marquee proof: FH's "One Faulty Weld, 123 Dead: The Alexander Kielland" — 742,398 views, 1.7× FH's era median (slate cohort-proposals). Slate ep 1 is built on it: "Thirteen Seconds, One Eyebar: Why the Silver Bridge Fell". | Default for evergreen bankers with a crisp physical cause. The channel's home formula — it *is* the positioning in one line. |
| F2 | **Report-Reveal** | `What [investigator] actually found / The [agency]'s final answer: [event]` | The freshness-monopoly logic the slate validated twice: Champlain Towers — every big treatment (1.52M, 909k) predates the June 2026 NIST findings; Key Bridge — day-of speculation took 1.2M/795k/336k while the only post-final-report treatments sit at 207k/111k. The title's job is to say *the answer now exists*. | Freshness-window topics (new final report, re-investigation). Slate eps 2 and 9. |
| F3 | **Paradox** | `[True fact]. [Incompatible-seeming true fact]: [event]` | Slate ep 3: "The Fire Was Out in Minutes. The Smoke Killed 85: MGM Grand, 1980" — built against the proven 1.94M-view demand on FH's mechanism-light MGM video. The paradox is the mechanism question stated as tension; it must resolve *in the report* (both halves are report facts). | Topics where the counterintuitive finding IS the story (smoke paths, "the dam that was never a dam"). |
| F4 | **Single-Decision** | `One [person/object/act] + [consequence]: [event]` | Slate ep 4: "One Man, 72 Hand Brakes, and a Town on Fire: Lac-Mégantic" — targeting the 2.58M-view sensational leader's audience with a factual version of the same pull. The census's beatable shape ("Trapped Inside — Kursk", 2.44M, Dark Records) proves the *pull* of person-scale framing; F4 is its non-exploitative twin: the decision, not the victim, is the subject. | Decision-chain-dominant stories. The guardrail: the "one man" is an actor in the causal chain, never a victim inside the event. |

**Honesty note on evidence strength:** F1 has direct in-lane view evidence (FH 742k). F2–F4 are grounded in the slate's demand analysis and cohort comps, not in per-formula A/B data — they are the launch hypotheses. The pattern log (§6.3) exists to replace this table's "evidence" column with the channel's own CTR data by video 15.

### 2.3 Title workflow per video

1. Prompt 6 generates 1 primary + 4 alternates across different formulas, each with its defensibility line.
2. Owner picks primary + 1 backup. The backup is stored in the packaging log — it is the pre-planned repackage title (§6.2), decided while judgment is cold.
3. Fact-check cross-check: every number/claim in both titles has a report citation.
4. Pre-mortem checklist (§5) before upload.

---

## 3. Thumbnail system

### 3.1 Identity

The thumbnail signature is the **hero failure diagram** — the one asset that makes "the forensic layer, drawn" legible in an impression, that no incumbent uses (FH: text-on-screen narrative; PD: 8-bit collage; Dark Records: shock stills — POSITIONING §c), and that AI-slop competitors can't cheaply fake (POSITIONING §d2). Every video's variant set includes at least one hero-diagram thumbnail, permanently.

### 3.2 The three-variant set (from prompt 5)

| Variant | Content | Hypothesis it tests |
|---|---|---|
| A — Hero diagram | The failure diagram simplified to one idea, ≤3 elements | The forensic promise itself is the click |
| B — Archival + overlay | Rights-cleared period photo + one diagram element (ring/arrow/inset) | Authenticity + curiosity hybrid |
| C — Contrast/scale | The tell-tale object made huge vs the scene | Concrete-detail curiosity (the 0.1-inch flaw vs the bridge) |

Fixed craft rules (all variants): readable at 120px; one focal point; ≤4 words of text that never duplicate title words; nothing graphic, no bodies, no victim distress (never-rule #1; the FH 7-year monetization precedent — census Q3); no photorealistic AI imagery (hard gate 2); archival photos unaltered in what they depict (hard gate 3); standing channel palette so the catalog reads as one shelf in browse.

### 3.3 A/B process — YouTube Test & Compare

YouTube Studio's built-in **Test & Compare** runs up to 3 thumbnails on one video and picks the winner by **watch-time share**, not raw CTR — which suits this channel: it automatically penalizes a curiosity-gap thumbnail that wins clicks but loses watch time, i.e., it enforces never-rule #6 by measurement.

Per-video protocol:

1. Upload all 3 variants (A/B/C) at publish. Variant A (hero diagram) is always in the test — the signature must keep earning its slot with data, not sentiment.
2. Let the test run **≥14 days or until Studio reports a confident winner**, whichever is later. Do not touch title or description mid-test — one variable at a time, always.
3. Record in the packaging log: winner, watch-time share split, and *which hypothesis* (§3.2) won.
4. Loser insights are learnings, not trash: a B-variant win on a freshness topic and an A-variant win on a banker is a pattern — check for it monthly (§6.3).
5. First 3 videos are also the calibration set: if Studio's test is unavailable at zero-subscriber scale for any reason, fall back to sequential testing (change thumbnail at day 10 if CTR is below the channel's running median, log before/after CTR at equal impression counts) — inferior but honest.

---

## 4. CTR / AVD reading guide — with decision thresholds

### 4.1 Why channel-relative thresholds, not internet benchmarks

No niche-specific CTR/AVD benchmark exists in the research files, and third-party "good CTR is X%" figures are unverifiable — so this guide deliberately uses **the channel's own trailing medians** as the reference line (computable from video 3 onward, robust from video 6), plus YouTube Studio's own per-video "typical range" display. This is also methodologically stronger: browse-driven channels are graded by the algorithm against their own baseline, and the kill-switch gate (memo v2 gate 4) is likewise median-relative.

**Impression floor:** make no CTR judgment on fewer than ~2,000 impressions, and never compare CTR across videos at different impression scales without noting it — CTR falls mechanically as YouTube widens an audience, so a *rising-impressions, falling-CTR* video may be succeeding. Always read CTR **with** the impressions curve, never alone.

### 4.2 The reading windows

| Window | What to read | What to do |
|---|---|---|
| 72 hours | CTR vs trailing-10 median; views vs trailing-10 72h median; browse/suggested/search split | Nothing irreversible. Flag only. (Census lesson: early signals mislead in both directions — Disaster Digest.) |
| Day 7 | CTR (≥2k impressions), AVD + avg % viewed vs channel median; retention curve shape in Studio | Repackage decision point #1 (§6.2). Intro-fix learnings for next script. |
| Day 28 | Full funnel: impressions → CTR → AVD → end-screen CTR to other videos; traffic-source mix | Dashboard ledger row finalized (`CONTENT_ENGINE.md` §e Tab 1); pattern log updated. |

### 4.3 The 2×2 decision matrix (read at day 7 and day 28)

"High/low" = above/below the channel's trailing-10 median for the same window.

| | **AVD / % viewed HIGH** | **AVD / % viewed LOW** |
|---|---|---|
| **CTR HIGH** | **Scale it.** The packaging pattern and topic class both worked — feed both back: same formula family for the next same-pillar video; topic class gets +evidence in the rubric. | **Overpromise or weak Act 1.** The impression wrote a check the cold open didn't cash. Fix forward: next script's cold open gets the mechanism hook earlier; check whether the title claimed more than the video delivers within 90 seconds. Do NOT repackage this video — its packaging works; its structure is the lesson. |
| **CTR LOW** | **Repackage.** The video keeps whoever finds it — the front door is the problem. Trigger §6.2: swap to the backup title and/or re-run Test & Compare with 2 new variants. Highest-leverage fix on the board. | **Topic/demand miss.** Packaging can't rescue absent demand. Check the topic's rubric score honestly — usually the demand-evidence score was soft (the slate flagged Doña Paz and Sayano as the least search-proven; if either lands here, promote Flixborough/San Bruno per the slate's stated mitigation). Feed back: raise the demand-evidence bar for the next 3 selections. One repackage attempt allowed, then move on. |

### 4.4 Retention-curve reads (Studio's curve, per video)

- **Cliff in the first 30s** → cold-open failure: too slow, or thumbnail/title audience mismatch. Next episode's cold open must place the concrete mechanism hook in the first 15 seconds (prompt 2 already mandates it — tighten enforcement).
- **Slow bleed through Act 1** → history/setup running long: cut Act 1 word budget 15% next script.
- **Spike at diagrams** (expected — they're the signature) → note which diagram type spiked; that type gets thumbnail priority next time. Spikes are also the Shorts cut-list (`CONTENT_ENGINE.md` §f).
- **Dip at diagrams** → diagram is confusing or narration decoupled from visuals: reveal staging (prompt 4 D3) is being violated; audit the brief vs the final asset.
- **Cliff at sponsor/membership mention** (later stage) → move the read or cut it; the calm register is the brand.

---

## 5. The packaging pre-mortem checklist — run before EVERY upload

Printed/scripted as a literal checklist; a video does not upload with an unchecked box. (The pre-mortem question behind every item: *"It's 30 days from now and this video underperformed — which of these did we skip?"*)

**Title**
- [ ] Primary keyword (slate keyword map) or close variant present, within first 60 chars
- [ ] Matches one of F1–F4; formula noted in the packaging log
- [ ] Every number/claim in the title has a report citation (fact-check pass output confirms)
- [ ] No banned vocabulary; no trademark implication; 45–70 chars
- [ ] Backup title selected and logged (the pre-planned repackage)

**Thumbnail**
- [ ] 3 variants (A hero-diagram / B archival+overlay / C contrast) built; Test & Compare configured
- [ ] 120px squint test passed on all 3 (one focal point, readable)
- [ ] Thumb text ≤4 words, zero overlap with title words
- [ ] Nothing graphic; no victims; archival photo unaltered in what it depicts
- [ ] No photorealistic AI imagery anywhere in any variant

**Description / metadata**
- [ ] First 2 lines: mechanism-question hook with primary keyword (the search snippet)
- [ ] Official report linked FIRST in the sources block
- [ ] "Written, narrated, and drawn by a human." statement present (the census-evidenced authenticity defense — DisastersUncovered stamps its equivalent into every title)
- [ ] Chapters timestamped; tags per prompt 6 (primary variants → event terms → cluster terms); max 3 hashtags
- [ ] End screen links: newest same-pillar video + subscribe; pinned comment drafted (the week's diagram teaser or report fact)

**Compliance (the four hard gates, per-upload form)**
- [ ] Suitability review (prompt 8) verdict: SHIP
- [ ] Synthetic-content disclosure toggle: correctly NOT required (stylized-exempt art direction verified — if in doubt, the asset is removed, never disclosed-around)
- [ ] Asset manifest 100% complete with license provenance (gate 3)
- [ ] Narration is the owner's human voice, start to finish (gate 1)

**System**
- [ ] Dashboard ledger row created; production hours logged against the 10h budget
- [ ] Short #1 cut and scheduled (Tue), Short #2 cut or consciously skipped
- [ ] Scheduled: Saturday 09:00 ET

---

## 6. The packaging iteration loop

### 6.1 The loop, end to end

```
pre-mortem (§5) → publish + Test & Compare (§3.3)
   → 72h read (flag only) → day-7 read → 2×2 matrix (§4.3)
      → [repackage / fix-forward / scale / move on]
   → day-28 read → ledger + pattern log (§6.3)
      → learnings applied to the NEXT video's prompt-6/prompt-5 runs
```

One packaging experiment per video maximum beyond the standing thumbnail test — otherwise nothing is attributable.

### 6.2 Repackaging rules (the "CTR LOW / AVD HIGH" cell)

1. **Trigger:** day-7 CTR below trailing-10 median by >20% at ≥2,000 impressions, with AVD at/above median.
2. **Action order:** (a) swap to the backup title; wait 7 days, one change only. (b) If still lagging: new Test & Compare round with 2 fresh thumbnail concepts against the incumbent winner. (c) Both done and still lagging at day 30 → accept, log, move on. Catalog videos get one more repackage look at month 6 (evergreen topics re-enter browse when the algorithm retests them; the catalog-compounding thesis — memo v2 durability row — makes old-video repackaging positive-expectation work).
3. **Never repackage** a video into a claim the report doesn't support, and never A/B *toward* sensationalism: the constraint set (§1 standing constraint) outranks CTR. The channel's bet is that the calm-forensic register wins long-run distribution (7 years of FH evidence); the playbook optimizes *within* the register, never out of it.

### 6.3 The pattern log (monthly, 30 min, feeds everything)

A tab in the dashboard: one row per published video — formula used (F1–F4), thumbnail winner (A/B/C), CTR, AVD, pillar, topic type (banker/freshness). Monthly ritual:

1. Tally CTR by formula and by thumbnail hypothesis. After ~10 videos, retire or rework the weakest formula; promote the strongest to default.
2. Rewrite §2.2's evidence column with own-channel data (the launch table's cohort evidence is the bootstrap, not the destination).
3. Check the register guardrail: if the best-performing packaging is drifting darker (the documented gradient — memo v2 surviving objection: "growth bends toward darker topics"), the never-list wins and the drift is named in the log. This check exists because the drift will be tempting precisely when it works.
4. Feed the two packaging KPIs to the kill-switch dashboard (`CONTENT_ENGINE.md` §e): trailing-10 median CTR trend and the share of videos beating their own pillar's median. Packaging health is the leading indicator; the day-120 gate reads the lagging ones.
