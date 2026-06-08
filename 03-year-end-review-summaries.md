# Pillar 03 — Year-End Review Summaries
## Data-Driven Narratives That Connect Engineering Output to Business Value

**Layer:** Business | **Great Leader Anchor:** Jamie Dimon (JPMorgan Chase) | **Related:** [Pillar 10](./10-executive-presence-selling-the-team.md) · [Pillar 05](./05-managing-up-influence-negotiation.md)

**Hogan Filter — Your Caution Trap:** You write reviews that are technically accurate but commercially invisible — full of system metrics and sprint completions with no translation to commercial impact. Stakeholders reading your reviews cannot answer: "What would trading look like without this team?" That is the standard they judge by.

**Anti-Caution Directive:** Write commercial briefs with technical evidence, not technical reports with a business sentence stapled to the end. The trading desk narrative comes first. Always.

---

## In 60 Seconds

Year-end reviews are budget and headcount arguments in performance-document clothing. If your review doesn't make the commercial case in the first paragraph, an MD skimming it reaches one conclusion: stable headcount, no growth. Dimon's standard: technology is a revenue driver, not a cost center — your review must prove it in 90 seconds of reading.

---

## The Core Framework: IMPACT Narrative

```
I — Initiative:     What was built or improved (1 sentence, no jargon)
M — Metric:         Quantitative before/after (latency, uptime, cycle time, cost)
P — Problem Solved: Business risk or inefficiency eliminated
A — Attribution:    Name the engineer — make individuals visible, not just the team
C — Commercial Tie: Direct link to PnL enablement, risk reduction, or cost avoidance
T — Trajectory:     What this unlocks for next year
```

---

## Dimon's Narrative Standard

| Technical Review Language | Dimon Commercial Brief Language |
|---|---|
| "Achieved 99.98% uptime" | "Zero unplanned outages during earnings season — desk ran $2.1B in volume without a single system-induced trade delay" |
| "Reduced P95 latency by 40ms" | "40ms latency reduction on order routing eliminated the queue backlog causing 3–5 missed fills per day at market open" |
| "Migrated CI pipeline to GitHub Actions" | "CI migration cut deployment lead time from 4.2h to 47min — accelerating time-to-desk for every feature by ~3x" |
| "Refactored Protobuf serialization layer" | "Serialization rewrite eliminated the silent data corruption mode that caused 3 hours of stale position data in Q2" |
| "Upgraded React trading dashboard" | "Dashboard rewrite cut end-of-day position reporting latency from 8s to 900ms — desk now closes positions in one tool instead of three" |

---

## Individual Engineer Review Template

```markdown
### [Engineer Name] — [Year] Performance Summary

**Commercial Impact Rating:** High / Developing / Below Bar

#### Top 3 Contributions

1. **[Initiative Name]**
   - Built: [one-line, no jargon]
   - Metric: [before → after, quantified]
   - Business impact: [PnL, risk reduction, cost, speed outcome]
   - Stakeholder signal: [trading desk comment / MD acknowledgment — quote if available]

2. [repeat]
3. [repeat]

#### Behavioral Signals
- **Velocity:** On-time delivery rate, sprint commitment accuracy
- **Quality:** P1 incidents caused, code review cycle time, defect escape rate
- **Collaboration:** Cross-team unblocking, on-call reliability, knowledge transfer
- **Commercial awareness:** Does this engineer understand how their system touches PnL?

#### Development Vector
[One sentence: this engineer's ceiling and the single investment that unlocks it next year]

#### Rating Recommendation
[Exceeds / Meets / Below] — supported by the data above. No hedging.
```

---

## Team Summary Template (for MD / Trading Desk Head)

```markdown
## Equities Technology Squad — [Year] Summary

Bottom Line: 5 engineers, [X] production releases, [uptime%] across [systems],
directly enabled [$ volume / risk outcome / cost savings].

### Business Impact — Top 5 Deliveries
| Delivery | Business Outcome | Beneficiary |
|---|---|---|
| [feature/fix] | [commercial outcome] | [desk/team] |

### Operational Health
- Unplanned outages: [N] (vs. [N+x] prior year)
- Mean time to recovery: [Xmin] (vs. [X+Ymin] prior year)
- Deployment frequency: [N/month] (vs. [N-1/month] prior year)
- Change failure rate: [X%]

### Investment Recommendation for [Next Year]
[2–3 sentences: headcount, tooling, or process investment needed and
the specific business outcome it generates]
```

---

## Metrics to Capture All Year (Not Just at Review Time)

```
- Deployment count and success rate (monthly)
- P1/P2 incident count and MTTR
- Sprint commitment accuracy (committed vs. delivered)
- PR review cycle time (open → merge)
- Stakeholder commendations (email, Slack, verbal — screenshot and date)
- Feature adoption signals (trading desk usage post-launch)
- Cost avoidance events (incidents prevented, manual ops time saved)
```

---

## The Caution Trap in Year-End Reviews

Your Hogan profile will push you toward:
- **Over-documentation** — 5-page reviews no MD reads past paragraph 2
- **Team-only attribution** — hiding individual performance behind "the team delivered X"
- **No commercial translation** — assuming the business will infer the value (they won't)
- **Recency bias** — defaulting to the last 6 weeks of data, ignoring the full year

**The Dimon Override:** Before submitting any review, ask: "If I read this aloud to the trading desk head in 90 seconds, would they be able to articulate why this engineer deserves their compensation?" If not, rewrite it.

---

## Weekly Experiments

1. **This week:** Write one IMPACT narrative for a team delivery in the last 30 days. Send it to your MD as a "Q[X] delivery brief" — one paragraph, commercial framing, zero jargon. Measure the response.
2. **This week:** Start a shared wins log. Every time a stakeholder gives positive signal — Slack, email, verbal — log it with date and name.
3. **This week:** Pull last quarter's metrics. Write the one-sentence business translation for each one.

---

*Next: [Pillar 04 — Talent Density](./04-talent-density-stack-ranking.md) | [Back to README](./README.md)*
