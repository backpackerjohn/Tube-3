# Monetization Roadmap — Mode of Failure

**Phase 10 deliverable · 2026-07-13 · Binding upstream documents:** `research/SELECTION_MEMO.md` (memo v2 + gate 4), `content-engine/CONTENT_ENGINE.md` (≤10h/video, $7,200/yr floor, dashboard), `content-engine/PACKAGING_PLAYBOOK.md` (§6.3 darkness-drift rule), `brand/POSITIONING.md` (personas, never-list), `research/validation/probe-monetization-policy-status.md` (policy probe), `research/validation/census-C09-quiet-catastrophes.json` (census), `research/candidates/hunt-meta-monetization-policy.json` (YPP thresholds + RPM evidence), `logs/DECISION_LOG.md` (D-003 long-form first, D-005 ≤$100/mo tooling).

This document answers the bear-case skeptic's accepted objection (memo v2: "economic failure if AdSense-only and effort stays at 15–25h/video") with the payback model v1 never had. Every number is either sourced from the files above or explicitly labeled **[inference]** or **[modeled]**.

---

## (a) The staged revenue model, with dated projections

### The stages (thresholds A-grade, verified in `hunt-meta-monetization-policy.json`)

| Stage | Threshold | What it unlocks | Source |
|---|---|---|---|
| **0. Pre-YPP affiliate layer** | 0 subs, day 1 | Affiliate links in descriptions (FTC-disclosed). Zero cost, zero gate. | Programs verified joinable at 0 subs — see `SPONSOR_AFFILIATE_TARGETS.md` quick-start |
| **1. YPP lower tier** | **500 subs + 3 public uploads/90d + (3,000 valid watch-hours/12mo OR 3M Shorts views/90d)** | Fan funding only: Super Thanks, channel memberships, Shopping. **NOT ad revenue.** ~1-month review after applying. | support.google.com/youtube/answer/13429240 [A] |
| **2. Full YPP** | **1,000 subs + (4,000 watch-hours/12mo OR 10M Shorts views/90d)** | Ad revenue share (~55% long-form, 45% Shorts). Auto-upgrade path from lower tier at 1,000 subs. | support.google.com/youtube/answer/72851 [A] |
| **3. Memberships / Patreon** | Evidence-gated, not platform-gated (see §d) | Recurring fan revenue | Census Q3: FH Patreon in 100/100 descriptions — the in-lane proof |
| **4. Sponsors** | ~7–10k subs (evidence-backed entry) | $300–900/read early **[modeled]** | Census: Forgotten Disasters carries Aura + Factor reads at 7k subs |

Our path to the watch-hour thresholds is long-form, not Shorts: 3M Shorts views/90d is not a realistic target at 2 mechanism Shorts/week (D-003; Shorts are a discovery surface, never a revenue line — Shorts RPM $0.01–0.06, S051 via `CONTENT_ENGINE.md` §f). At 12–20 min videos and ~7 min average watch **[inference: 45–55% avg-viewed at documentary pacing]**, 1 view ≈ 0.117 watch-hours, so 3,000h ≈ 25,700 views and 4,000h ≈ 34,200 views — the **subscriber counts are the binding constraint in every scenario**, not watch-hours.

### The three view scenarios, grounded in the census cohort

Sub-conversion rate used throughout: **~7.5 subs per 1,000 views** (census, API-verified: DisastersUncovered 26.6k subs / 3.76M views = 7.1; Forgotten Disasters 7.07k / 837k = 8.4).

| Scenario | Anchor (census, API-verified 2026-07-12) | Per-video 12-mo views **[modeled]** | Trailing-10 median at day 120 **[modeled]** |
|---|---|---|---|
| **Bear** | Forgotten Disasters path: median ~4.2k/upload after 10 months, breakouts 20–55k, sponsors at 7k subs but modal uploads 1–5k | avg 6k (median ~4.2k) | ~4–5k |
| **Base** | Geometric midpoint of the two indie trajectories; consistent with a packaging-led launch that clears the 8k gate but doesn't break out | avg 15k (median ~10–12k) | ~10–11k |
| **Bull** | DisastersUncovered path: median ~35k on last 20 uploads at 26.6k subs, 6 of 20 over 100k, 18 months in | avg 45k (median ~35k) | ~30k+ |

Honest caveats carried from the census: the visible cohort overstates success odds (failure denominator systematically undercounted); Disaster Digest proves early traction can be revoked (~1M lifetime views → 62–820/upload); bear is the *documented modal outcome*, not a tail case.

### Dated milestone projections (launch Sat Aug 1, 2026; 1 video/week; ~55% of a video's 12-mo views land in month 1 [modeled])

| Milestone | Bear | Base | Bull |
|---|---|---|---|
| 500 subs (≈67k cum views) → apply lower tier | ~Nov 2026 (video ~13) | ~mid-Sep 2026 (video ~6) | ~mid-Aug 2026 (video ~3) |
| Lower-tier approval (+~1 mo review) → Super Thanks on | ~Dec 2026 | ~Oct 2026 | ~Sep 2026 |
| 1,000 subs (≈133k cum views) → full YPP eligible | ~Feb 2027 (**moot — gate fires first, see §b**) | ~late Oct 2026 (video ~11) | ~early Sep 2026 (video ~5) |
| **Ads live** (+~1 mo review) | never (pivot) | ~late Nov 2026 | ~early Oct 2026 |
| 2,000 subs → Patreon trigger (§d) | — | ~Feb 2027 | ~Oct 2026 |
| 7,000 subs → sponsor-entry evidence line (census: FD carries reads here) | — | ~Sep 2027 | ~Jan–Feb 2027 |
| 10,000 subs → active sponsor outreach | — | ~Q4 2027 | ~Mar–Apr 2027 |

Watch-hour check: base crosses 4,000h at ≈34k cumulative views — inside month 1–2 — confirming subs, not hours, gate every stage.

---

## (b) The payback model the skeptics demanded

### Cost per video

| Component | Value | Basis |
|---|---|---|
| Hours | 10.0 | Hard gate (`CONTENT_ENGINE.md` §b — budget sums to exactly 10.0h; hours creep is audited on the dashboard) |
| Imputed owner rate | **$25/hr [inference]** | Solo-operator opportunity cost; sensitivity shown at $15 and $50 below |
| Tooling | $23/video | D-005 cap $100/mo ÷ 4.33 videos/mo (recording, edit suite, music library, diagram tools all inside the cap) |
| **Full economic cost / video** | **$273** | |
| **Cash cost / video** | **$23** | What actually leaves the bank account |

Sensitivity: at $15/hr the full cost is $173/video; at $50/hr, $523/video. The two-lens point below survives all three rates.

### Revenue per video (AdSense leg)

RPM evidence: **documentary/history band $4–12 — C-grade, flagged.** Sources: `hunt-meta-monetization-policy.json` ("History/documentary $4–12", outlierkit/fluxnote aggregations, reliability C) and `probe-monetization-policy-status.md` Task 3 ("faceless history/documentary RPM commonly reported at $5–12", LOW reliability, ballpark only). No first-person RPM report from FH or peers exists in indexed sources (census Q3 gap). Scenario RPMs used: bear $5 · base $7 · bull $10, with Q4 +30–50% seasonality (hunt-meta). **Every revenue number downstream inherits this C-grade.**

| Per-video, 12-mo | Bear | Base | Bull |
|---|---|---|---|
| Views | 6,000 | 15,000 | 45,000 |
| AdSense revenue | $30 | $105 | $450 |
| vs full cost $273 | **−$243** | **−$168** | **+$177** |
| vs cash cost $23 | +$7 | +$82 | +$427 |

**The honest per-video statement:** AdSense-only payback of the owner's time requires ≈39,000 lifetime views at $7 RPM. Only bull clears it per-video. Base recovers the owner's time only at portfolio level — catalog compounding (documentary views accrue for years; FH's 4.5-year-old Lac-Mégantic video still ranks) plus the non-ad legs. Bear never pays back time. But **cash costs are cleared even in bear** — the channel cannot bleed the owner's bank account, only their hours. This is exactly the trade the ≤10h gate was built to cap.

### Cumulative break-even chart (full economic cost, all revenue legs, [modeled] on the assumptions above)

Includes 3 pre-launch banked videos in month-1 cost. Revenue = AdSense (from the ads-live dates in §a) + fan funding + affiliates + sponsors (from the evidence-gated dates in §d). Q4 uplift applied Nov–Dec.

| Month (end) | Videos | Cum full cost | Bear cum rev | Bear net | Base cum rev | Base net | Bull cum rev | Bull net |
|---|---|---|---|---|---|---|---|---|
| Aug 2026 | 7 | $1,911 | $20 | −$1,891 | $30 | −$1,881 | $60 | −$1,851 |
| Sep 2026 | 12 | $3,276 | $45 | −$3,231 | $80 | −$3,196 | $200 | −$3,076 |
| Oct 2026 | 16 | $4,368 | $75 | −$4,293 | $180 | −$4,188 | $900 | −$3,468 |
| Nov 2026 (day 120) | 20 | $5,460 | $110 | −$5,350 | $730 | −$4,730 | $2,800 | −$2,660 |
| Dec 2026 | 24 | $6,552 | *pivot* | −$5,350 | $1,430 | −$5,122 | $5,400 | −$1,152 |
| Feb 2027 | 33 | $9,009 | — | — | $2,700 | −$6,309 | $9,800 | +$791 |
| Apr 2027 | 42 | $11,466 | — | — | $4,200 | −$7,266 | $14,600 | +$3,134 |
| Jul 2027 (yr 1) | 55 | $15,015 | — | — | $6,900 | −$8,115 | $22,500 | +$7,485 |
| Dec 2027 | 76 | $20,748 | — | — | $13,500 | −$7,248 | $42,000 | +$21,252 |
| Jul 2028 (yr 2) | 107 | $29,211 | — | — | $26,500 | **−$2,711** | $72,000 | +$42,789 |
| ~Oct 2028 | — | — | — | — | — | **≈ break-even** | — | — |

Readings:
- **Bull: full economic break-even ~month 6–7 (Feb 2027)**, driven by ads + sponsor reads from ~7k subs (Jan–Feb 2027) — consistent with the DU-anchor being an 18-month channel earning at scale.
- **Base: cash break-even ~month 6; full economic break-even ~month 26–27 (Q4 2028)** — the owner works below their imputed rate for two years, then the compounding catalog + sponsor era carries it. This is a *viable-if-patient* business, not a fast one. It only works because cost/video is capped at 10h; at the skeptic's 15–25h/video it never crosses.
- **Bear: the kill-switch fires at day 120 with ~$5,350 of sunk imputed time and ~$460 of sunk cash.** The catalog stays up as a maintenance asset (engine protocol §e.3) but its ~4k views/mo tail is immaterial (<$500/yr even if eventually monetized). The gate exists precisely to cap this loss at one quarter of effort.

### Explicit comparison against the $7,200/yr kill-switch floor (day 120 = Nov 29, 2026)

| Scenario | Median test (<8k fires) | Revenue projection — engine formula (trailing-8-wk actual ÷8 ×52) | Revenue projection — forward run-rate (trailing-28d all-legs ×12) [modeled] | Gate outcome |
|---|---|---|---|---|
| Bear | ~4.2k → **FAIL** | ~$450/yr → **FAIL** | ~$1,600/yr → FAIL | **Fires on both arms. Execute C23 pivot playbook.** |
| Base | ~10–11k → PASS | ~$1,800/yr → **FAIL** | ~$5,400–7,600/yr → **straddles the floor** | **Knife-edge — see finding below** |
| Bull | ~30k+ → PASS | ~$8,000–12,000/yr → PASS | ~$18,000–30,000/yr → PASS | Clears 2–4× |

**FINDING (flagged for owner sign-off — this is the model's most important output):** the engine's trailing-8-week revenue formula, applied at day 120, measures *YPP approval latency*, not channel economics. In the base case, ads have been live only ~2 weeks of the trailing 8, so the formula annualizes mostly pre-monetization zeros and fires the gate on a channel that *passes the median test* — the two arms become inconsistent (any channel that barely passes 8k-median produces only ~$3–4k/yr of ad run-rate at documentary RPM). Recommended resolution, which **does not lower the floor** (engine rule: may raise, never lower):

1. **Keep the floor at $7,200/yr, unchanged.**
2. **Measure the day-120 revenue arm as forward run-rate**: (trailing-28-day channel views × evidence-band RPM, Q4-normalized) + trailing-28-day fan funding + affiliates + contracted sponsor value, ×12. This is a measurement clarification within Phase-10's remit ("a defined floor" was delegated to this model), but because the engine specified the trailing-8-week method, adoption requires an explicit owner decision — log it in `logs/DECISION_LOG.md`.
3. **Add a second, raised floor at day 240 (≈Mar 29, 2027): projected annualized gross < $14,400/yr → pivot.** $14,400 = full economic cost of the cadence at $25/hr (52 × $273 ≈ $14.2k, rounded). This is a floor *raise*, explicitly permitted, and it gives the skeptics the guarantee v1 lacked: by month 8 the channel must be on a path to paying for the owner's time, not merely beating the failure band.
4. Even under forward run-rate, **base sits within ±15% of the $7,200 floor at day 120** — the engine's protocol §e.4 "almost fires" clause then governs: continuation requires a written diagnosis naming what changes, and a hard day-180 re-check. Base-case survival therefore depends on front-loading every non-ad revenue leg (§d). That is not a caveat; it is the design.

---

## (c) Ad-suitability management plan (tragedy-adjacent content)

The exposure, stated from evidence: tragedy/"sensitive events" is limited-ads territory by default under the advertiser-friendly guidelines (support.google.com/youtube/answer/6162278 [A], via census Q3), but **historical, non-graphic treatment is explicitly monetizable** — the memo's re-adjudication rests on it, and FH has monetized this register for 7+ years (census). Worst case by design is a *per-video yellow-icon haircut*, never channel-level enforcement — the never-list and hard gates 1–3 exist to keep it that way (POSITIONING §f standing rule).

### 1. Self-certification strategy

- Complete the self-certification questionnaire on **every** upload, accurately. The content design makes honest answers green-friendly: no graphic imagery, no victim sensationalism, deaths stated once with sourcing, episodes end on the fix (BRAND_GUIDELINES voice rules 1, 4, 10 — the ad-suitability armor is written into the register).
- Expected steady state: **green with occasional yellow** on recent-event topics (Surfside, Key Bridge) — recency, not tragedy per se, drives "sensitive events" classification. G6 (no live-litigation/raw-grief topics) already limits this exposure.
- Accurate self-certification builds the channel's rater-trust score, which reduces bot-overrule frequency over time — the compounding reason never to shade an answer. **[inference from how the self-cert system is documented to work; no in-lane first-person data]**
- Never monetize a video that fails its own packaging pre-mortem suitability check (`CONTENT_ENGINE.md` stage 8 gate).

### 2. Yellow-icon appeal SOP

1. **Upload Thursday for Saturday publish** (the pipeline already schedules this) — the ~48h gap lets the automated rating land while the video is still scheduled/private.
2. If yellow at upload: verify self-certification answers, then **request human review immediately**. Human review is available as soon as the channel is in YPP; reviews typically resolve in days and the verdict is final-ish, so the appeal window sits inside the scheduling gap by design.
3. **Do not move the publish date** for a pending review — first-72h velocity matters more than the delta between limited and full ads on day 1 (browse/suggested is the primary growth channel, memo correction #4).
4. Log every icon event in the dashboard (new column, Tab 1): video, auto-rating, appeal filed y/n, outcome, suspected trigger phrase. Two yellows in one pillar → run the script through the banned-vocabulary QA list (BRAND_GUIDELINES §2) and the thumbnail through the §3.4 hard-bans before the next video in that pillar.
5. If a video is *confirmed* limited-ads after human review: leave it up (catalog value + memberships/affiliates still earn), note it in the topic log, and treat the topic class as yellow-flagged for future scoring.

### 3. Topic-mix guardrail (the darkness-drift rule)

- `PACKAGING_PLAYBOOK.md` §6.3.3 is binding here: monthly pattern-log check — *"if the best-performing packaging is drifting darker … the never-list wins and the drift is named in the log. This check exists because the drift will be tempting precisely when it works."* Monetization adds the enforcement teeth: darkness drift converts green inventory into yellow inventory, so the drift check is a **revenue control**, not just a brand control.
- Structural limits already in force: no massacre-class topics ever (never-rule 5 — the Bath School 177k data point is traffic deliberately refused); ≤2 recent-event (freshness) topics per rolling 10 (cadence rule 3 + G6) keeps the "sensitive events" surface small; ≤2 videos per pillar per rolling 10 prevents a run of same-class yellow flags.
- KPI: **share of trailing-10 videos fully monetized (green) ≥ 80%.** Below that for two consecutive months → treat as an amber event in the dashboard and audit scripts/packaging before topic selection changes.

---

## (d) Revenue diversification sequencing — WHY-gated triggers

Order matters: each leg turns on only when its evidence condition is met, and no leg may breach the 10h/video budget (legs are description links, uploads of existing assets, and batched monthly work).

| # | Leg | Trigger (WHY-gated) | Why — the evidence | Time cost |
|---|---|---|---|---|
| 1 | **Affiliate links** (Ground News, CuriosityStream, Brilliant, Amazon — see `SPONSOR_AFFILIATE_TARGETS.md`) | Day 0 — launch with them | Joinable at 0 subs, $0 cost (fits D-005); description-link monetization is proven in-lane (FH links Patreon in 100/100 descriptions — the description real estate works, census Q3). FTC disclosure line in every description. | ~1h setup once; 0/video |
| 2 | **Super Thanks** | Day 1 of lower-tier approval | Zero marginal effort; the only revenue available at 500 subs (lower tier unlocks fan funding only [A]) | 0 |
| 3 | **Patreon** | **2,000 subs OR a sustained Persona-3 signal (≥10 "I work in this field"-class comments/week for a month), whichever first** | FH evidence shows the leg works in-lane: Patreon linked in 100/100 sampled descriptions, 460 patron-gated posts (census Q3 — scale unverified, flagged). POSITIONING §b: Domain Professionals are "the natural first members/patrons." Launching before an audience exists burns setup time for $0 — hence the gate. | ~4h setup; ≤1h/mo |
| 4 | **Channel memberships** | Lower-tier unlock available, but hold until Patreon is live and stable | Same perks would cannibalize; Patreon owns the relationship off-platform (survives any YPP event — see risk table). Turn on memberships as the low-tier mirror ($1.99–2.99) for viewers who won't leave YouTube. **[inference — no in-lane membership data exists; FH's join-button status unverifiable via API, probe Task 1 method note]** | ~1h |
| 5 | **Sponsor reads** | Passive: business email in About from day 1. Active outreach at **10,000 subs**; accept credible inbound from ~7,000 | Census: Forgotten Disasters carries **Aura and Factor reads at 7k subs**; DisastersUncovered ran Factor at ~26k — sponsors demonstrably buy this exact inventory down-market. Marquee-tier reads are sparse (FH ~3/100 — memo correction #5), so sponsors are a mid-game leg, never the load-bearing one. Rules: ≤1 read per 2 videos, 60–90s post-cold-open, calm register, suitability screen per `SPONSOR_AFFILIATE_TARGETS.md`. | ~1h/read incl. integration |
| 6 | **Patreon perk set (faceless-format-fit)** | With leg 3 | Perks that need no face and reuse pipeline exhaust: early access (48–72h), the **source pack** (report digest PDF with section citations — stage-1 output, zero extra work), hi-res diagram downloads/prints (stage-5 output), backlog topic-poll votes (feeds §d topic system), name-in-credits. Explicitly out: face reveals, vlogs, live hangouts on a schedule — parasocial perks the faceless format can't honestly deliver. | ≤1h/mo |
| 7 | **Diagram print merch** | 25,000 subs + repeated organic requests | Deferred: fulfillment overhead vs D-005 budget; revisit only on demand evidence. | — |

Sequencing logic in one line: **cash-free legs first (affiliates), platform legs as they unlock (Super Thanks → ads), relationship legs when the audience exists (Patreon at the P3 signal), sponsor legs when the census says buyers show up (7–10k subs).**

---

## (e) Honest risk table — what kills each revenue leg

| Leg | What kills it | Likelihood / severity | Mitigation (already binding) |
|---|---|---|---|
| **AdSense — channel-level** | Inauthentic-content enforcement (channel-level, July 2025 policy [A]); the Jan 2026 purge shape (16 of top-100 slop channels, 35M subs, ~$10M/yr — probe Case 3) | Low for this design / **fatal** | Maximum-distance profile: human narration (gate 1), report-first originality, per-episode unique causal webs (POSITIONING §d). This risk is why C09 won the re-adjudication — never trade these gates for growth. |
| **AdSense — per-video** | Limited-ads (yellow) wave on tragedy adjacency; a darkness drift that converts the catalog to yellow | Medium / haircut (survivable by design) | §c plan: self-cert, appeal SOP, drift rule, ≥80% green KPI |
| **AdSense — distribution** | Field-wide faceless deprioritization: French Whisperer −60% views YoY to the slop flood; Doctor NOS "most of them are getting demonetized" (probe Cases 1–2, B+ sources) | **Medium-high / severe** — the lane's documented headwind | Accountable-faceless posture (real voice, sign-off, pinned owner comments — BRAND §4.5); diagrams as un-fakeable packaging; kill-switch caps the downside if distribution never arrives |
| **AdSense — rate** | RPM lands at the $4 bottom of the C-grade band, or the band itself is wrong (no first-person in-lane RPM exists — census Q3 gap) | Unknown / −40% on every ad projection | First 8 weeks of real RPM data replace the band in the dashboard; day-240 raised floor catches a bad rate early |
| **Memberships/Patreon** | Audience never reaches scale (bear); faceless parasocial ceiling — patrons pay creators they *know*, and we offer competence, not intimacy **[inference]**; FH's patron *scale* is unverified (census Q3 — could be modest) | Medium / caps the leg, doesn't zero it | P3-signal trigger prevents premature launch; perks are artifact-based (source packs, diagrams) not persona-based, which travels better for faceless formats |
| **Sponsors** | Brand-safety veto on tragedy adjacency; sparse marquee-tier evidence (FH ~3/100 — correction #5 says never model this leg as load-bearing); a single mis-fit read damages the trust register the channel sells | Medium / bounded (leg is capped at ≤1 read per 2 videos anyway) | Engineering-education framing widens the sponsor surface beyond tragedy (memo thesis §2); suitability screen in `SPONSOR_AFFILIATE_TARGETS.md`; census-contradicted classes (VPN/audiobook) carried only with caveats |
| **Affiliates** | Program shutdowns/rate cuts (CuriosityStream's bundle economics already contracted once — Nebula bundle ended Dec 31, 2024, en.wikipedia.org/wiki/Nebula_(streaming_service) [B]); description-link CTR is tiny at small scale | High churn / small $ | Diversify across 4+ programs; treat as pocket money until proven; never build content around an affiliate |
| **Shorts** | Not a revenue leg and never becomes one (RPM $0.01–0.06, S051; D-003) | — | Judged only on YPP-threshold progress and long-form conversion (`CONTENT_ENGINE.md` §f) |
| **The whole stack** | The kill-switch itself: bear-case reality. All legs together in bear ≈ $1.6k/yr against $14k/yr of imputed time | Real — bear is the documented modal outcome | Gate 4 fires Nov 29, 2026, caps the loss at ~$5.4k imputed / ~$460 cash, and the C23 pivot playbook is pre-written (memo fallback) |

**Bottom line for the skeptics:** the channel is cash-positive by month 6 in base and can never bleed more than ~$100/mo of cash (D-005). What it *can* bleed is the owner's time — and the model shows exactly where that stops: day 120 (bear), day 240 raised floor (slow base), or full payback ~month 26 (base) / month 6–7 (bull). No zombie-grinding path remains open.
