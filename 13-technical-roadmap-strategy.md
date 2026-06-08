# Pillar 13 — Technical Roadmap & Strategy
## Building a 12-Month Equities Tech Strategy That Survives Budget Season

**Layer:** Business | **Great Leader Anchor:** Jeff Bezos (Amazon) | **Related:** [Pillar 05](./05-managing-up-influence-negotiation.md) · [Pillar 10](./10-executive-presence-selling-the-team.md)

**Hogan Filter — Your Caution Trap:** You build roadmaps bottom-up from what feels safely achievable — a list of tickets dressed up as a strategy. This produces a defensible plan that nobody fights about and nobody champions. A great roadmap is a *bet*, stated with conviction, that forces prioritization and attracts investment. Your caution makes you hedge every bet into invisibility.

**Anti-Caution Directive:** A roadmap is a set of conviction bets, not a hedge against being wrong. State the bet in a headline. Allocate real capacity to Transform. Fund what works, kill what doesn't — loudly. Decisiveness in strategy is itself a visibility asset.

---

## In 60 Seconds

Budget season is where roadmaps die or get funded. A bottom-up ticket list gets interpreted as BAU maintenance. A stated 12-month bet, expressed in commercial terms, with clear capacity allocation — that gets investment. Bezos banned PowerPoint for strategy at Amazon because it allowed fuzzy thinking to hide behind bullet points. Your roadmap should be a memo, not a slide. And it should have a headline you'd be proud to read at a business review.

---

## The Core Framework: 3-Horizon Roadmap

```
HORIZON 1 — RUN (50–60% capacity)
  Keep the lights on. SLA maintenance, regulatory mandates, BAU support,
  critical bug fixes. Non-negotiable. The desk stops trading if this slips.

HORIZON 2 — GROW (25–35% capacity)
  Features and optimizations that measurably improve desk velocity, PnL
  enablement, or risk reduction. This is where you compete for budget.

HORIZON 3 — TRANSFORM (10–20% capacity)
  Bets that change the game in 12+ months. Re-platforming, new capabilities,
  ML/automation. High-risk, high-visibility. The thing that gets you promoted.
```

**The caution failure:** A cautious leader puts 90% in Horizon 1 and calls it "responsible." Without a visible Horizon 3, you have no strategic narrative, no growth story, and no argument for investment. That is how a team becomes a cost center.

---

## Bezos — Working Backwards & the Narrative Memo

Bezos banned PowerPoint for strategy at Amazon. Every major initiative starts with a **working-backwards document**: write the future press release and FAQ *before* you build anything. Do the same for your H2 and H3 bets:

```
FUTURE-STATE MEMO — [Initiative Name]

THE HEADLINE (12 months out):
"The equities desk now [does X] in [Y time] instead of [old way],
eliminating [Z risk/cost]."

THE CUSTOMER (who on the desk benefits):
[Specific trader/ops/risk persona and their current pain]

THE METRIC THAT PROVES IT:
[Before → After, quantified]

WHAT WE HAD TO BELIEVE TO BET ON THIS:
[The 2–3 assumptions. If these are wrong, the bet is wrong.]

THE COST:
[Engineer-quarters, infra spend, opportunity cost of what we don't do]
```

If you cannot write a crisp headline, the initiative isn't ready — and you shouldn't be defending it in budget season.

---

## One-Way vs. Two-Way Doors

Bezos's most-cited decision principle, applied to roadmap commitments:

| Door Type | Definition | Roadmap Examples | Speed |
|---|---|---|---|
| **Two-way (reversible)** | Walk back cheaply | Adopting a new library, feature flag rollout, sprint structure | Decide fast, delegate, iterate |
| **One-way (irreversible)** | Expensive or impossible to reverse | Core re-platform, vendor lock-in, public SLA commitment, schema migration | Slow down, validate to 70–80% |

**The caution trap:** You treat *every* roadmap decision as a one-way door. 90% of them are two-way. Spend your caution budget only on the genuinely irreversible bets. Move fast on everything else.

---

## The Roadmap-to-Budget Translation

Every H2/H3 item must be translated into budget-holder language before your review:

| Initiative | Engineering Frame | Budget-Season Frame |
|---|---|---|
| Latency re-platform | "Rewrite order routing in Rust" | "$X PnL recovery from 4ms→1ms fill improvement; 3 fewer P1s/year" |
| Test automation | "Increase coverage to 85%" | "Cut change-failure rate 60%; reclaim 1 eng-week/month of firefighting" |
| Observability stack | "Deploy distributed tracing" | "Cut MTTR from 30min→8min; reduce desk downtime cost by ~$X/incident" |
| React dashboard rewrite | "Upgrade to React 18 + Suspense" | "EOD position reporting from 8s to 900ms; desk uses one tool instead of three" |

---

## Quarterly Roadmap Review Cadence

| Activity | Frequency | Output |
|---|---|---|
| Horizon capacity check | Monthly | Are we actually at 50/30/20, or has Run eaten everything? |
| Future-state memo refresh | Quarterly | Are the assumptions behind H2/H3 bets still true? |
| Stakeholder pre-wire | Before each quarterly review | Bilateral alignment before the formal meeting |
| Kill / double-down review | Quarterly | What bet is failing? Kill it loudly. What's working? Fund it more. |

---

## The Caution Trap in Strategy

Your Hogan profile will push you toward:
- **Bottom-up roadmaps** — aggregating tickets instead of stating a bet
- **Over-weighting Horizon 1** — calling pure maintenance a "strategy"
- **Hedged language** — "we may explore" instead of "we will deliver"
- **Treating all doors as one-way** — slow-walking reversible decisions
- **No kill discipline** — keeping zombie projects alive because cancelling feels like admitting failure

**The Bezos Override:** A roadmap is a set of conviction bets. State the bet in a headline. Allocate real capacity to Transform. Fund what works, kill what doesn't — loudly, so the org sees you make hard calls. Decisiveness in strategy is itself a visibility asset.

---

## Weekly Experiments

1. **This week:** Tag every item on your current roadmap H1/H2/H3 and sum the capacity allocation. If Transform is at 0%, you have a cost-center roadmap. Carve out one Horizon 3 bet this quarter.
2. **This week:** Write one future-state memo in the Bezos format for your most important H2 initiative. Test it on a peer: can they repeat the headline back to you accurately? If not, sharpen it.
3. **This week:** Take your three biggest pending roadmap decisions. Classify each as one-way or two-way door. Make every two-way decision by Friday — you've been over-deliberating the reversible ones.

---

*Next: [Pillar 14 — Hiring](./14-hiring-for-equities-technology.md) | [Back to README](./README.md)*
