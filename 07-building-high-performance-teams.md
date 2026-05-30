# Pillar 07 — Building High-Performance Tech Teams
## Optimizing Engineering Velocity, Quality, and Psychological Safety

**Great Leader Anchor:** Elon Musk (Tesla/SpaceX)
**Hogan Filter:** Your caution default is to protect the team from stretch goals and aggressive timelines, framing this as "realistic planning." The consequence is a team that runs at 70% capacity, has no forcing function for process improvement, and cannot demonstrate the velocity that would justify additional headcount or investment.

---

## The Core Framework: The 4-Metric Operating Dashboard

For a 5-person equities tech team, track these four metrics weekly — not quarterly.

```
METRIC 1 — DEPLOYMENT FREQUENCY
  Target: ≥2 production deployments per engineer per sprint
  Signal: Low frequency = process friction, not engineering complexity

METRIC 2 — LEAD TIME FOR CHANGE
  Target: Commit → Production ≤ 4 hours for hotfixes, ≤ 24h for features
  Signal: Long lead time = CI/CD bottleneck or approval process overhead

METRIC 3 — CHANGE FAILURE RATE
  Target: <5% of deployments require hotfix or rollback
  Signal: High rate = insufficient test coverage or pre-prod environment gap

METRIC 4 — MEAN TIME TO RECOVERY (MTTR)
  Target: P1 incidents resolved in ≤30 minutes during market hours
  Signal: High MTTR = runbook gaps, on-call skill deficit, or alert fatigue
```

These are the DORA metrics. They are the closest thing equities tech has to a universal team health dashboard.

---

## Equities-Specific Performance Metrics

### UI/Visualizer Performance (React Trading Dashboards)
```
- Total Blocking Time (TBT):        Target < 200ms
- Largest Contentful Paint (LCP):   Target < 1.5s for market-open dashboards
- Frame Rate (FPS):                 Target ≥ 60fps for real-time price feeds
- Bundle Size:                      Monitor Δ on every PR — no unreviewed regressions
```

### Backend / Data Pipeline Performance
```
- Protobuf deserialization latency:  Track P50/P95/P99
- Order routing P99 latency:         Hard SLA — define and hold it
- Feed reconnect time:               Market hours SLA ≤ 5 seconds
- Test coverage on critical paths:   ≥ 80% for order state machine, pricing engine
```

---

## Elon Musk's First-Principles Engineering Model

Musk's operating principle: **"The best part is no part. The best process is no process. Eliminate before you optimize."**

For your team's development cycle:
1. **Map your current deployment pipeline.** Write every step from commit to production.
2. **Challenge each step:** "Does this step exist because it must, or because it always has?"
3. **Delete or automate** any step that cannot pass that test.
4. **Only then** optimize what remains.

Applied: If your PR approval cycle requires 3 sign-offs for a config change, ask whether 3 sign-offs have ever caught a critical defect that 1 would have missed. If not, eliminate the ceremony.

---

## The High-Performance Sprint Architecture

```
SPRINT STRUCTURE (2-week cycle for 5 engineers):

├── 70% — Committed delivery (business features + critical fixes)
├── 20% — Technical investment (test coverage, tooling, debt reduction)
└── 10% — Slack / exploration (unplanned incidents, investigation, learning)

NEVER run at 100% committed capacity.
The 30% buffer is not slack — it is your production stability insurance.
```

---

## Psychological Safety Without Coddling

High-performance teams require both psychological safety (engineers can flag problems without fear) and high accountability (problems get fixed, not just surfaced). These are not in tension — they are complementary.

**The operating contract:**
```
"On this team:
- You will not be blamed for incidents caused by system complexity or design debt.
- You WILL be held accountable for not following our incident runbooks.
- You can raise a risk or concern in any forum — Slack, 1:1, retro — without it
  being treated as a career signal.
- You WILL be expected to bring a solution when you raise a structural problem."
```

The distinction: psychological safety covers **context and process failures**. Accountability covers **individual behavioral commitments**.

---

## Team Velocity Acceleration Tactics

| Tactic | Implementation | Impact |
|---|---|---|
| Kill your longest test suite | Find the slowest 10% of tests; parallelize or quarantine | 20–40% CI time reduction |
| Trunk-based development | Feature flags over long-lived branches | Eliminates merge conflict tax |
| Runbook automation | Convert top 5 P1 runbook steps to scripts | MTTR reduction |
| PR size limit | Enforce max 400 lines per PR via CI check | 60% faster review cycle |
| Daily async standup | Written, async, time-boxed to 10 min | Eliminates meeting overhead |

---

## The Caution Trap in Team Building

Your Hogan profile will push you toward:
- **Protecting sprint capacity** by padding estimates and under-committing to stakeholders
- **Avoiding aggressive timelines** that would expose process inefficiencies
- **Over-engineering quality gates** that slow deployment without proportionate risk reduction
- **Not publishing metrics** because they might invite scrutiny

**The Musk Override:** Publish your 4 DORA metrics to your MD quarterly. Teams that make their velocity visible attract investment. Teams that hide their metrics behind verbal updates get treated as cost centers.

---

## Weekly Experiments

1. **This week:** Run a pipeline audit. Map every step from commit to production deployment. Identify the single highest-latency step. Assign one engineer to eliminate or automate it this sprint.
2. **This week:** Pull your team's TBT and FPS data for the last release. If you don't have automated performance benchmarks, that is your highest-priority technical investment for this sprint.
3. **This week:** Measure your current PR cycle time (open → merge). If it is over 24 hours on average, identify the bottleneck — is it review availability, CI duration, or approval process? Address the root cause, not the symptom.
