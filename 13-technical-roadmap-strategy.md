# Pillar 13 — Technical Roadmap & Strategy
## Building and Owning a 12-Month Equities Tech Strategy That Survives Budget Season

**Great Leader Anchor:** Jeff Bezos (Amazon) — working-backwards, one-way vs. two-way doors, the narrative memo
**Hogan Filter:** Your caution default is to build roadmaps bottom-up from what feels safely achievable — a list of tickets dressed up as a strategy. This produces a defensible plan that nobody fights about and nobody champions. A great roadmap is a *bet*, stated with conviction, that forces prioritization and attracts investment. Your caution makes you hedge the bet into invisibility.

---

## The Core Framework: The 3-Horizon Roadmap

For a 5-person equities tech squad, every initiative must map to one of three horizons with an explicit capacity allocation.

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

**The caution failure:** A cautious leader puts 90% in Horizon 1 and calls it "responsible." That is how a team becomes a cost center. Without a visible Horizon 3, you have no strategic narrative and no growth story.

---

## Bezos — Working Backwards & the Narrative Memo

Bezos banned PowerPoint for strategy at Amazon. Every major initiative starts with a **working-backwards document**: write the future press release and FAQ *before* you build anything.

For your roadmap, write a **1-page future-state memo** for each Horizon 2/3 bet:

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
[Engineer-quarters, infra spend, opportunity cost of what we DON'T do]
```

Bezos's discipline forces clarity. If you cannot write a crisp headline, the initiative isn't ready — and you shouldn't be defending it in budget season.

---

## One-Way vs. Two-Way Doors (Roadmap Decisiveness)

Bezos's most-cited decision principle, applied to roadmap commitments:

| Door Type | Definition | Roadmap Examples | Decision Speed |
|---|---|---|---|
| **Two-way (reversible)** | You can walk back through it cheaply | Adopting a new library, trying a sprint structure, a feature flag rollout | Decide fast, delegate, iterate |
| **One-way (irreversible)** | Expensive or impossible to reverse | Core re-platform, vendor lock-in, public SLA commitment to the desk, schema migration | Slow down, validate to 70–80% |

**The caution trap:** You treat *every* roadmap decision as a one-way door. 90% of them are two-way. Spend your caution budget only on the genuinely irreversible bets; move fast on everything else.

---

## The Roadmap-to-Budget Translation

Budget season is where roadmaps die or get funded. Translate every Horizon 2/3 item into the language of the people holding the budget.

```
| Initiative | Engineering Frame | Budget-Season Frame |
|---|---|---|
| Latency re-platform | "Rewrite order routing in Rust" | "$X PnL recovery from 4ms→1ms fill improvement; 3 fewer P1s/yr" |
| Test automation | "Increase coverage to 85%" | "Cut change-failure rate 60%; reclaim 1 eng-week/month of firefighting" |
| Observability stack | "Deploy distributed tracing" | "Cut MTTR 30min→8min; reduce desk downtime cost by ~$X/incident" |
```

---

## The Quarterly Roadmap Review Cadence

| Activity | Frequency | Output |
|---|---|---|
| Horizon capacity check | Monthly | Are we actually spending 50/30/20, or has Run eaten everything? |
| Future-state memo refresh | Quarterly | Are the assumptions behind H2/H3 bets still true? |
| Stakeholder pre-wire | Before each quarterly review | Bilateral alignment with MD + desk before the formal meeting |
| Kill / double-down review | Quarterly | What bet is failing? Kill it loudly. What's working? Fund it more. |

---

## The Caution Trap in Strategy

Your Hogan profile will push you toward:
- **Bottom-up roadmaps** — aggregating tickets instead of stating a bet
- **Over-weighting Horizon 1** — calling pure maintenance a "strategy"
- **Hedged language** — "we may explore" instead of "we will deliver"
- **Treating all doors as one-way** — slow-walking reversible decisions
- **No kill discipline** — keeping zombie projects alive because cancelling feels like admitting a wrong bet

**The Bezos Override:** A roadmap is a set of conviction bets, not a hedge against being wrong. State the bet in a headline. Allocate real capacity to Transform. Fund what works, kill what doesn't — loudly, so the org sees you make hard calls. Decisiveness in strategy is itself a visibility asset.

---

## Weekly Experiments

1. **This week:** Audit your current roadmap. Tag every item H1/H2/H3 and sum the capacity. If Transform is at 0%, you have a cost-center roadmap. Carve out one Horizon 3 bet this quarter.
2. **This week:** Write one future-state memo (the Bezos format) for your most important Horizon 2 initiative. Test it on a peer: can they repeat the headline back to you? If not, sharpen it.
3. **This week:** Take your three biggest pending roadmap decisions. Classify each as one-way or two-way door. Make every two-way decision by Friday — you've been over-deliberating the reversible ones.
