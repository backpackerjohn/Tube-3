# Build Log — Tube-3 Channel Blueprint

Chronological record of every phase, tool result, decision, failure, and workaround.
Companion files: [DECISION_LOG.md](DECISION_LOG.md) (assumed answers to questions never asked), [../research/sources/SOURCE_LOG.md](../research/sources/SOURCE_LOG.md) (every URL cited anywhere).

---

## 2026-07-12 — Session start

**Mission ingested** from `master_prompt_3.pdf` (3 pages). Parsed: 9 guardrails, 13-phase arc, definition of done. Mode: fully autonomous, never ask, everything committed to this repo on branch `claude/pdf-instruction-review-hhrb8j`.

**Environment verification:**
- Repo `backpackerjohn/Tube-3` — empty, no commits, already on target branch. ✅
- YouTube Data API v3 — test call to `search.list` succeeded (HTTP 200, valid JSON). Key active. ✅
- vidIQ MCP connection — live. **Constraint discovered: only 30 credits available** (10 renewable + 20 add-on; renews 2026-08-02). Most vidIQ tools cost 5 credits/call → **budget ≈ 6 vidIQ calls for the entire mission.** ✅ but tight.
- Web research (search + fetch) — available. ✅

**Consequence of the credit constraint (logged as Decision D-002):** vidIQ is used surgically at the two points where it is irreplaceable — (1) faceless-channel discovery at the start of the hunt, (2) keyword-metrics validation of the finalists — while the free YouTube Data API (10,000 quota units/day) and open web carry the volume work. All vidIQ calls are made from the main session, never from subagents, so spend stays controlled and auditable.

**Repo scaffolded:** research/{sources,candidates,validation,keywords}, brand/, content-engine/, scripts/, production/, monetization/, red-team/, logs/.

## Phase 1 — Opportunity hunt

**vidIQ discovery call #1 (5 credits, 25 remain):** `vidiq_channel_search` — faceless=true, breakout=true, long-form, 20k–2M subs, created ≥ 2024-07, sorted by 30-day subscriber growth. **5,165 matching channels total**; top 50 saved to `research/candidates/vidiq-faceless-breakout-scan.json`. Read of the field: the fastest growers are dominated by Shorts/compilation/meme formats (reused-content traps we must avoid per guardrail 6), but real long-form original formats are breaking out too: medical explainers (Eric Bennett MD — 60 long videos in 30d; QuantumZoom), lore/analysis (Digital Circus Explained), build/restoration (DIY Tractor Mini, Structverse), narrative pet rescue (Second Chance Dog).

**Cross-verification (YouTube Data API `channels.list`):** all six spot-checked channels are real and the numbers agree with vidIQ within normal growth drift (e.g. Eric Bennett MD: vidIQ 40.2k subs → API 42.7k; QuantumZoom 139k → 141k). Notable: Eric Bennett MD created **2026-05-14** (2 months old) already at 42.7k subs / 2.58M views. Saved to `research/candidates/yt-api-crosscheck-breakouts.json`. This validates that new faceless channels are still breaking out in 2026 — the core premise of the mission is alive.

**Workflow `opportunity-hunt` launched:** 7 parallel hunter agents (history, gaming, AI, travel, money/business, science/true-story, wildcard) + 2 meta researchers (RPM/monetization policy; market trends & AI-content policy). Each must back every claim with fetched URLs, use the YouTube API for competitor scans, and is barred from vidIQ calls (credit protection).

**Hunt complete (9/9 agents, 227 tool calls):** 28 candidates produced with YouTube-API-verified competitor scans — saved per lane to `research/candidates/hunt-*.json`, consolidated in `candidates.md`. 147 unique sources appended to the source log. One hunter noted YouTube API search.list quota pressure and switched to web-search-then-API-verify — accepted workaround, logged.

**Key meta findings shaping everything downstream:**
- YouTube took 12.5–13.5% of ALL US TV viewing every month from mid-2025 through Mar 2026 (Nielsen, A-grade); FY2025 YouTube revenue > $60B (Alphabet 10-K). Platform demand is not the risk.
- YPP July 15, 2025 "inauthentic content" policy is the central constraint for faceless channels: mass-produced templated output is demonetizable; AI-assisted content stays monetizable when "significantly original and authentic" (TechCrunch/Rene Ritchie, A-grade). Our originality defense must be structural, not cosmetic.
- Realistic synthetic media requires the March-2024 disclosure label; typical AI narration over unrealistic/animated visuals does not (YouTube official blog, A-grade).
- Documented proof faceless channels monetize at scale in 2025-26: Fortune-verified case ($40–60k/mo, AdSense screenshots); Fall of Nations (0→204k subs in 20 months); Dr. Jonathan Tam (0→109k in <11 months). Survivorship bias noted — to be stress-tested by judges and red team.
- Vendor-blog "faceless niche" statistics are C-grade marketing; excluded from load-bearing decisions.

## Phase 2 — Tournament

**Workflow `candidate-tournament` launched:** 3 independent judges (demand skeptic / new-entrant realist / business operator) score all 28 candidates on the six required criteria with hard gates (faceless, originality, policy safety), a synthesizer builds the consensus matrix and names 4-5 finalists, and a completeness critic attacks the field before selection.

**Tournament complete.** Finalists: C13 Paycheck Nation (7.37), C10 How Nations Break (7.30), C09 Quiet Catastrophes (7.10), C23 Relocation Report (6.78), C16 Modern Fraud Files (6.63). Full matrix in `research/candidates/scoring-matrix.md`; judges' full scores in `tournament/`. Completeness critic flagged: (1) horror-storytelling niche missing from the field despite an apparent strong vidIQ signal; (2) proof-channels' post-July-2025 monetization status unverified; (3) survivorship bias — C13 rests on n=1, C23 on incumbents only. All three became Phase-3 work items.

## Phase 3 — Validation

**vidIQ keyword validation (3 × 5 credits, 10 remain, reserved for winner):** disaster/history seeds show the best opportunity ratios ("history documentary": 89.4 volume / 49 competition / 74.1 overall, ~981k monthly searches; "seconds from disaster" at 29.1 competition). Money seeds sit at competition 60–75. Saved to `research/validation/vidiq-keyword-validation.json`.

**Workflow `finalist-validation`:** 5 cold-start cohort censuses (one per finalist; YouTube API-verified cohorts of young channels incl. failures) + monetization/policy probe + C29 horror late-entrant probe. **Interruption:** 6 of 7 agents failed on an account spend limit mid-run; the C13 census completed first and was banked. Resumed the workflow ~40 min later (cached C13 replayed free); all 7 completed. Total: 270 tool calls.

**Census verdicts:** C09 **OPEN** (winners minted in every vintage 2019→2025; DisastersUncovered's new uploads out-view its sub count 4–10× in July 2026). C23 OPEN-but-boom-bust (MrState 0→137k/13mo proves entry; violent cycles; policy WARN stands). C13 **CLOSING** (0/5 cold-starts converted; incumbents captured the shelf; exemplar's median −4×). C10 **CLOSING** (open through Jan 2026, Mar–Jun entrants near-zero). C16 **CLOSING** (exact-format entrants DOA at 5–4,800 lifetime views).

**Policy probe:** the 2025–26 faceless demonetization wave is real and documented (French Whisperer −60% views under slop flood, 404 Media; Doctor NOS "most of them are getting demonetized", Hollywood Reporter June 2026; Jan 2026 purge of 16 top-100 AI-slop channels; Screen Culture/KH Studio demonetized→terminated arc, Deadline). Disclosure-label ruling by format: charts/maps/archival + generic AI voice = no label; photorealistic AI historical scenes = label required; stylized/illustrated AI imagery = exempt (compliance-optimal art direction).

**C29 horror probe: the trigger signal was a data error.** vidIQ's "Ms Nightcipher" record (73k subs, $68k/mo est.) resolves via channels.list to **Structverse** — an AI-transformation-Shorts channel, no horror, dormant since 2026-04-08; no "Ms Nightcipher" channel exists anywhere on the web. C29 scored 5.28 on its real merits (entrenched incumbents, $4–8 RPM, policy-targeted cheap mode) — does not displace any finalist. **Data-quality lesson logged: vidIQ scan records must be API-verified before they carry weight.**

## Phase 4 — Selection

**Winner: C09 Quiet Catastrophes** — the only OPEN census verdict, zero gate flags, best sustainability (8.0), best keyword opportunity ratios, policy-safest originality structure. Higher-seeded C13/C10 were falsified by their censuses (CLOSING). Full reasoning in `research/SELECTION_MEMO.md`. Fallback designated: C23. **Workflow `selection-skeptics` launched** — 3 adversarial skeptics (evidence auditor, bear case, policy hawk) try to refute the pick before it is locked.

**Skeptic panel result (2 refuted / 1 conditional-uphold → mandatory re-adjudication):** the evidence auditor caught five real errors in memo v1 — most seriously, the Tenerife "duplicate absorption" proof was one syndicated 87-minute documentary counted twice (identical durations; second channel is a Little Dot Studios network property), and "multiple thriving young indies" was actually n=1. The bear case proved v1 had no payback model and a kill-switch that could never fire in the documented modal failure (1–5k views/upload ≈ $200–600/mo). The policy hawk independently RE-VERIFIED the decisive fact: C09's incumbents show zero decay (Fascinating Horror Mar–Jul 2026 uploads at 169k–795k views) while C10/C13 lanes decay — the OPEN/CLOSING asymmetry is real.

**Re-adjudication (memo v2):** C09 confirmed over C23 on severity-weighted worst case (limited-ads haircut vs channel-level demonetization) and 3-year durability, with the thesis corrected: marquee-adjacent topics first (long-tail demand is authority-gated), engineering-forensics spine as differentiator, economics designed with a payback model, and four hard gates (human narration; stylized non-photorealistic art; archival-rights protocol; payback-calibrated kill-switch). All v1 errors preserved in a corrections table per guardrail 3. This is the adversarial process working as intended.

## Phase 5 — Keyword research & launch slate

**vidIQ call #5 (5 credits, 5 remain in reserve):** "engineering disasters" — 58.6k monthly searches at competition 42.5 (overall 65.7), beating the pure disaster-documentary frame on every axis; the errors/fails/mistakes cluster adds ~55k monthly at comp 42–47. The engineering-forensics reframe is keyword-validated.

**Workflow `video-slate`:** 3 proposal agents + synthesizer. Spend limit struck again mid-run: cohort-proven and report-vault agents completed (24 evidence-backed topics, every one with API-verified view numbers on existing coverage); the search-demand agent and synthesizer died. Route-around: autocomplete checked directly from the main loop (endpoint proxy-blocked — logged as gap), and the slate was synthesized in the main loop from the 24 surviving proposals. Result: `research/keywords/LAUNCH_SLATE.md` — 10 ordered launch videos with per-topic evidence, class-diversity check, backlog of 14, keyword map, and honest evidence-gap notes. Standout finds: Champlain Towers post-NIST-findings vacuum (findings June 2026, zero incumbent coverage since), Texas City's 4M-view topic with a 3,272-view best indie treatment, Ocean Ranger's withdrawn 4.19M-view supply.
