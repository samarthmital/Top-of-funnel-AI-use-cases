# 09 — Executive Summary (1-Page)

> **For:** Revenue Engineering leadership + business process owners
> **Decision requested:** Fund a phased build to bring AI agents into the top of the funnel,
> starting with a single inbound "wedge" use case.

---

## The opportunity

Our funnel loses conversion to **slow response, unqualified hand-offs, stalled trials, and
manual account research**. A proven, production pattern from a **$1B+ ARR public B2B SaaS
company** shows AI agents closing those gaps — in one year handling **tens of thousands of
leads**, booking **thousands of meetings**, and generating **millions in pipeline**, while
cutting demo-request response time from **~24 hours to under 2 minutes**.

## The proof (anonymized reference deployment)

| Workflow | Outcome |
|----------|---------|
| Inbound voice qualifier | **100%** of in-scope inbound handled; **<2 min** response (was ~24 h); **0%** live-scheduling failures |
| In-app trial activation | **2.5×** trial→paid conversion vs. control; 50% of users return for a 2nd session |
| Outbound research/planning | Account research + plan + cadence in **~5 min** (was 1–2 weeks) |

## What we'd build

Three agents, one per funnel stage, sharing one architecture:

1. **Inbound Qualifying & Hand-off Agent** — voice-qualifies inbound "contact sales" requests
   (BANT) and hands reps a **prepared, qualified meeting** — never a raw lead.
2. **In-Platform Trial Activation Agent** — a live in-app "personal sales engineer" that detects
   intent and routes trial users to value.
3. **Outbound Research & Account Planning Agent** — deep research, account plans, and cadences at
   scale for named/enterprise accounts.

## The one principle that makes it reliable

**"Smart tools and naive agents."** Push determinism into tools/microservices; use the LLM only
where genuine reasoning is required. In the reference deployment this single decision took live
meeting-scheduling to a **0% failure rate** and was *the* unlock for organizational trust.

## Recommended path

- **Start with the inbound wedge** (speed-to-lead): clearest baseline, cleanest A/B, fastest ROI.
- **Deploy at ~60% readiness** behind a holdout control; iterate with an eval harness.
- **Sequence:** wedge → deterministic backbone → agents-as-code + eval → localization → expand to
  the other two workflows. (Full plan: [07 — Rollout](07-rollout-build-vs-buy-risks.md).)

## The ask

| We need | Why |
|---------|-----|
| A small, dedicated **AI-for-GTM squad** (eng + RevOps + a business process owner) | Treated as an "internal startup"; the reference team rebuilt 4× in a year |
| Budget for a **swappable reference stack** (telephony, voice, orchestration, LLM, CRM) | Buy commodities, build reliability glue; avoid vendor/model lock-in |
| Approval to run a **holdout A/B** on one market | Prove causal lift before scaling |

## Success criteria (first 90 days)

- Inbound response time **< 2 min** on the pilot market
- **Provable conversion lift** vs. holdout
- **0%** critical scheduling failures via the deterministic backbone
- Eval harness live in CI; model/vendor routing swappable

> Full detail: [00 — Overview](00-overview.md) · build plan: [10 — Build Backlog](10-build-backlog.md)
