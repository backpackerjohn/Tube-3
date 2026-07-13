# Phase 4 — Winner Selection Memo (v2)

**Date:** 2026-07-13 · **Decision:** **C09 — reframed as "disaster engineering forensics" — is confirmed as the channel to build**, on corrected facts and with four hard execution gates.
**Revision history:** v1 (2026-07-13) selected C09 and was then attacked by a 3-skeptic adversarial panel (`research/validation/skeptic-panel.md`). Two skeptics refuted **the memo as written** — catching five real evidence errors — and one upheld the pick conditionally. This v2 is the mandatory re-adjudication on corrected facts. The v1 errors are preserved in the corrections table below rather than silently fixed, per guardrail 3.

## Corrections table — what v1 got wrong (all skeptic-caught, API-verified)

| # | v1 claim | Corrected fact |
|---|----------|----------------|
| 1 | Two channels' near-identical Tenerife documentaries were both "absorbed" (248k + 108k views) → demand exceeds supply | The two videos have identical 87m19s durations; the second channel is part of the Little Dot Studios network. This was **one syndicated documentary counted twice** — a licensing artifact, not duplicate-supply absorption. Claim struck. |
| 2 | "Multiple genuinely independent young channels thriving right now" | The census grades exactly **one** young indie "thriving" (DisastersUncovered) and one "modest" (Forgotten Disasters — which, as of 2026-07-13, had not uploaded in 18 days after 10 months of every-2-day cadence). Corrected to n=1 thriving + 1 modest-and-possibly-burned-out. |
| 3 | "DisastersUncovered's uploads out-view its sub count 4–10×" | That describes the top quartile. Last-20 pull: median ≈35k views on 26.6k subs (~1.3×), floor 2.3k; 5 of 20 uploads clear 100k. Still genuinely strong for an 18-month indie — but stated honestly now. |
| 4 | "Best keyword ratio in any lane" via "history documentary" (981k/mo, competition 49) | That term is generic to the whole history lane, not C09-specific. The niche term "disaster documentary" has **3,461 US searches/month** (41.5k global). "Seconds from disaster" is a National Geographic brand title. Money-lane related terms include low-competition entries too (financial survival 25.5). Keyword pillar downgraded from "best ratio measured" to "adequate, search-assisted discovery; browse/suggested is the primary growth channel." |
| 5 | "VPN/audiobook sponsors are standard in the format" | Census: sponsor reads in ~3 of 100 Fascinating Horror videos, no VPN/audiobook reads observed; the NordVPN evidence belonged to a C10-lane channel. Corrected: sponsors are **sparse at the marquee tier**; Forgotten Disasters' sponsor reads at 7k subs remain a real but modest positive signal. |
| 6 | "The only finalist with zero policy gate flags" | False as stated — C13/C10/C16 also carried zero tournament flags (only C23 had a WARN). And C09's lane has its own live policy exposure: the AI-slop flood has arrived in-lane (the thriving indie brands every title "No AI. Human Narrated." as a defense), and faceless channels face documented algorithmic deprioritization field-wide. Reframed below as severity-weighted policy comparison, not "zero flags." |

## Re-adjudication: C09 vs C23 on corrected facts

The censuses left two OPEN lanes. On corrected facts, the honest comparison is:

| Axis | C09 (disaster forensics) | C23 (relocation rankings) |
|---|---|---|
| Distribution proof | Incumbents show **zero decay** (Fascinating Horror's Mar–Jul 2026 uploads run 169k–795k views — policy-hawk verified 2026-07-13); one thriving 18-month indie; no 2026-launch evidence either way | Bigger, more recent winner (MrState: 0→137k subs / 22.4M views in 13 months from June 2025) but **violent boom-bust cycles** and a real failure floor |
| Expected revenue velocity | Lower: RPM ~$4–12 (C/D-grade), field-lowest monetization score 5.7, sparse sponsors at scale | Higher: cheapest production (8.0), monetization 7.0, purchase-intent audience (moving/real-estate/insurance) |
| Worst-case policy outcome | **Per-video limited-ads haircut** (tragedy adjacency) — survivable; historical non-graphic treatment is explicitly monetizable under the advertiser guidelines; incumbents monetize for 7+ years | **Channel-level inauthentic-content demonetization** (standing WARN; listicle + stock b-roll + AI VO is the enforcement wave's named shape; Jan 2026 purge precedent) — fatal if it fires |
| 3-year durability | Evergreen catalog compounds; research/narrative moat is hard to copy; sustainability 8.0 | Listicle fatigue, most AI-sloppable format on the platform, clickbait pressure; sustainability 5.7 |
| Median-case economics | Documented modal outcome 1–5k views/upload ≈ $200–600/mo gross at 1/week — **economic failure if AdSense-only and effort stays at 15–25h/video** (bear-case skeptic, accepted) | Better revenue per view, but boom-bust means the median entrant may get one cycle then collapse |

**Decision rule:** for a solo, faceless, launch-this-month operator, worst-case severity dominates expected velocity — a limited-ads haircut leaves a living channel that can iterate and add revenue legs; a demonetization strike or slop-purge ends the project. C09 also dominates on durability. C23's velocity advantage is real and is why it remains the designated pivot. **C09 confirmed.**

The bear-case skeptic's fatal economic objection is accepted as a **design requirement**, not a kill: v1 had no payback model, and the modal outcome at v1's implied design (1/week, 15–25h/video, AdSense-only) is failure. The channel design therefore changes, below.

## The confirmed thesis (v2, corrected)

**Channel: faceless forensic documentaries on how disasters actually happened** — the engineering, the decisions, and the systems that failed — built from official accident-investigation reports (CSB, NTSB, MAIB, TSB, mining/rail/structural inquiries), with custom failure-mechanism diagrams as the visual signature.

What changed from the C09 pitch, driven by the corrected evidence:

1. **Topic strategy inverts.** The census proved long-tail demand is authority-gated (Mount Pelée, 30,000 dead: 2,213 views; Matawan: 752) while marquee-adjacent topics pull views for young channels (Aberfan: 478k on a 26.6k-sub channel; Bath School: 177k on a 7k-sub channel). Launch slate therefore targets **famous-enough-to-be-searched, under-served-in-quality** disasters; the obscure long tail is a later-stage asset unlocked by earned authority, not the launch wedge.
2. **The forensic/engineering spine is the differentiator** vs Fascinating Horror's narrative register — it serves the same audience a *why-it-happened* layer the incumbent deliberately keeps light, pulls the content toward the engineering/education audience (higher ad tier than pure tragedy narration), and widens the sponsor surface toward the proven engineering-channel sponsor set (Brilliant/CuriosityStream/Nebula class) rather than the unproven VPN/audiobook claim struck in correction #5.
3. **Economics are now designed, not assumed** (full model in `monetization/`): target ≤10h/video via the production system, cadence 1/week sustained (the every-2-day grinders burn out — Forgotten Disasters went dark; quality-with-packaging beats volume per the DisastersUncovered vs Mode of Horror natural experiment), revenue legs staged (AdSense → memberships/Patreon → engineering-education sponsors), and break-even math computed at bear/base/bull view medians.
4. **Packaging is a first-class system** — the census attributes breakout separation to title/thumbnail craft; the content engine (Phase 8) builds an explicit packaging iteration loop with scoring.

## Hard execution gates (from the policy hawk — binding on all later phases)

1. **Human narration.** The owner records the narration (faceless ≠ voiceless), or hires a human narrator. No TTS/AI voice: pure synthetic narration is a named monetization-risk factor, and the lane's one thriving indie stamps "No AI. Human Narrated." into every title as a survival defense. This is a hard gate, not a preference.
2. **Stylized, non-photorealistic art direction.** Diagrams, maps, period photos, illustrated reconstructions. No photorealistic AI scene generation (would trigger the synthetic-media disclosure label and its enforcement risk). Static archival photos must not be altered/animated in ways that change what the real event appears to be.
3. **Archival-imagery rights protocol.** Source only from verified public-domain/openly-licensed repositories (NARA, Library of Congress, Wikimedia Commons with license check, government inquiry documents); prefer accident-report figures and self-made diagrams; keep a per-video asset manifest with license provenance (template in `production/`). Agency-controlled press imagery (Getty/Mirrorpix/AP) is off-limits even when the underlying photo looks old.
4. **Payback-calibrated kill-switch.** At day 120 with ≥15 published, fully-packaged videos: if the trailing-10 median is under ~8k views **or** projected annualized revenue is under a defined floor, execute the C23 pivot playbook (with its shown-methodology defense from video 1) rather than zombie-grinding. This replaces v1's kill-switch, which the bear case correctly showed could never fire in the documented modal failure mode.

## What the panel's surviving objections still say (carried into the red team, Phase 11)

- The lane's failure denominator is systematically under-observed; the true cold-start base rate is worse than the visible cohort.
- Faceless channels face documented field-wide algorithmic headwinds in 2026 regardless of originality (French Whisperer, Doctor NOS reports).
- Growth gradient in this niche bends toward darker topics (school massacres outperform); house-style rules must resist that pull to protect ad suitability (hard constraint in Phase 7).
- n=1 thriving indie is thin proof; the bet is on severity-weighted policy logic plus incumbent non-decay, not on a dense success cohort.

**Fallback (unchanged):** C23 Relocation Report with shown-methodology defense from video 1, triggered by the gate-4 kill-switch.
