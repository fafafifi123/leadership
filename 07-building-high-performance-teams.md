# Pillar 07 — Building High-Performance Tech Teams
## Optimizing Engineering Velocity, Quality, and Psychological Safety

**Layer:** Team | **Great Leader Anchor:** Elon Musk (Tesla/SpaceX) | **Related:** [Pillar 11](./11-strategic-decisiveness-under-uncertainty.md) · [Pillar 08](./08-will-skill-matrix.md)

**Hogan Filter — Your Caution Trap:** You protect the team from stretch goals and aggressive timelines, framing this as "realistic planning." The consequence is a team that runs at 70% capacity, has no forcing function for process improvement, and cannot demonstrate the velocity that would justify additional headcount or investment.

**Anti-Caution Directive:** Publish your DORA metrics. Commit to 10% more than feels safe. Eliminate one step in your deployment pipeline this sprint. Teams that make velocity visible attract investment. Teams that hide metrics get treated as cost centers.

---

## In 60 Seconds

High-performance teams in equities technology have two non-negotiables: they ship fast (deployment frequency), and they recover fast (MTTR). Everything else — psychological safety, technical investment, sprint structure — exists to serve those two outcomes. If you cannot state your current deployment frequency and MTTR in under 10 seconds, you are not yet running a metrics-driven team.

---

## The Core Framework: 4 DORA Metrics (Weekly Tracking)

```
METRIC 1 — DEPLOYMENT FREQUENCY
  Target: ≥2 production deployments per engineer per sprint
  Low frequency = process friction, not engineering complexity

METRIC 2 — LEAD TIME FOR CHANGE
  Target: Commit → Production ≤4h for hotfixes, ≤24h for features
  Long lead time = CI/CD bottleneck or approval process overhead

METRIC 3 — CHANGE FAILURE RATE
  Target: <5% of deployments require hotfix or rollback
  High rate = insufficient test coverage or pre-prod environment gap

METRIC 4 — MEAN TIME TO RECOVERY (MTTR)
  Target: P1 incidents resolved ≤30 minutes during market hours
  High MTTR = runbook gaps, on-call skill deficit, or alert fatigue
```

Track these weekly. Not quarterly. Weekly.

---

## Equities-Specific Performance Metrics

### UI / React Trading Dashboard Performance
```
- Total Blocking Time (TBT):       Target <200ms
- Largest Contentful Paint (LCP):  Target <1.5s for market-open dashboards
- Frame Rate (FPS):                Target ≥60fps on real-time price feeds
- Bundle Size Delta:               Monitor on every PR — flag regressions in CI
```

### Backend / Data Pipeline Performance
```
- Protobuf deserialization latency: Track P50/P95/P99 — alert on P99 drift
- Order routing P99 latency:        Hard SLA — define it, instrument it, hold it
- Feed reconnect time:              Market hours SLA ≤5 seconds
- Test coverage on critical paths:  ≥80% for order state machine, pricing engine
```

---

## Musk's First-Principles Engineering Model

**"The best part is no part. The best process is no process. Eliminate before you optimize."**

Applied to your deployment pipeline:
1. **Map every step** from commit to production (write it out — most teams can't do this cleanly)
2. **Challenge each step:** "Does this exist because it must, or because it always has?"
3. **Delete or automate** any step that cannot pass that test
4. **Only then** optimize what remains

If your PR approval requires 3 sign-offs for a config change, ask: have 3 sign-offs ever caught a critical defect that 1 would have missed? If not, eliminate the ceremony. Your caution derailer builds these ceremonies. First-principles thinking tears them down.

---

## The High-Performance Sprint Architecture

```
SPRINT CAPACITY ALLOCATION (2-week cycle, 5 engineers):

  70% — Committed delivery    (business features + critical fixes)
  20% — Technical investment  (test coverage, tooling, debt reduction)
  10% — Slack / exploration   (unplanned incidents, investigation, learning)

NEVER run at 100% committed capacity.
The 30% buffer is not slack — it is your production stability insurance.
```

A cautious leader runs at 60% committed to "guarantee delivery." This is invisible to the business, signals a team with excess capacity, and destroys the case for investment.

---

## Psychological Safety Without Coddling

High-performance teams require both psychological safety (engineers can flag problems without fear) and high accountability (problems get fixed, not just flagged). These are complementary, not in tension.

**The operating contract:**
```
"On this team:
- You will not be blamed for incidents caused by system complexity or design debt.
- You WILL be held accountable for not following our established runbooks.
- You can raise a risk or concern in any forum — Slack, 1:1, retro — without
  it being treated as a career signal.
- You WILL be expected to bring a solution when you raise a structural problem."
```

Psychological safety covers **context and process failures**. Accountability covers **individual behavioral commitments**.

---

## Team Velocity Acceleration Tactics

| Tactic | Implementation | Expected Impact |
|---|---|---|
| Kill your slowest tests | Find the slowest 10% of tests; parallelize or quarantine | 20–40% CI time reduction |
| Trunk-based development | Feature flags over long-lived branches | Eliminates merge conflict tax |
| Runbook automation | Convert top 5 P1 runbook steps to executable scripts | Direct MTTR reduction |
| PR size limit | Enforce max 400 lines per PR via CI check | 60% faster review cycle |
| Daily async standup | Written, async, time-boxed to 10 min | Eliminates stand-up meeting overhead |

---

## The Caution Trap in Team Building

Your Hogan profile will push you toward:
- **Protecting sprint capacity** — padding estimates and under-committing to stakeholders
- **Avoiding aggressive timelines** that would expose process inefficiencies
- **Over-engineering quality gates** that slow deployment without proportionate risk reduction
- **Not publishing metrics** — because they might invite scrutiny

**The Musk Override:** Publish your 4 DORA metrics to your MD quarterly. Teams that make their velocity visible attract investment. Teams that hide their metrics behind verbal updates get treated as cost centers. Scrutiny is not a threat — it is an opportunity to demonstrate what your team actually does.

---

## Weekly Experiments

1. **This week:** Run a pipeline audit. Map every step from commit to production. Identify the single highest-latency step. Assign one engineer to eliminate or automate it this sprint.
2. **This week:** Pull your team's TBT and FPS data for the last release. If you don't have automated performance benchmarks, that is your highest-priority technical investment this sprint.
3. **This week:** Measure current PR cycle time (open → merge). If over 24h on average, identify the bottleneck: review availability, CI duration, or approval process. Address the root cause, not the symptom.

---

*Next: [Pillar 08 — Will/Skill Matrix](./08-will-skill-matrix.md) | [Back to README](./README.md)*
