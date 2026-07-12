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
