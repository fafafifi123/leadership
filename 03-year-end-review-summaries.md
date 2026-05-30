# Pillar 03 — Year-End Review Summaries
## Data-Driven Narratives That Connect Engineering Output to Business Value

**Great Leader Anchor:** Jamie Dimon (JPMorgan Chase)
**Hogan Filter:** Your caution default is to write reviews that are technically accurate but business-invisible — full of system metrics and sprint completions with no translation to commercial impact. Stakeholders reading your reviews cannot answer the question: "What would trading look like without this team?"

---

## The Core Framework: IMPACT Narrative Architecture

```
I — Initiative:     What was built or improved (1 sentence, no jargon)
M — Metric:         The quantitative before/after (latency, uptime, cycle time, cost)
P — Problem Solved: The business risk or inefficiency that was eliminated
A — Attribution:    Name the engineer — make individuals visible, not just the team
C — Commercial Tie: Map directly to PnL enablement, risk reduction, or cost
T — Trajectory:     What this unlocks for next year
```

---

## Jamie Dimon's Narrative Principle

Dimon runs JPMorgan's $15B+ technology investment on a single communication mandate: **technology is a revenue driver, not a cost center, and every technology leader must be able to articulate that distinction in under 60 seconds.**

His senior tech leaders do not write reviews. They write **commercial briefs with technical evidence.** The distinction:

| Review Mindset | Commercial Brief Mindset |
|---|---|
| "We achieved 99.98% uptime" | "Zero unplanned outages during earnings season — desk ran $2.1B in volume without a single system-induced trade delay" |
| "Reduced P95 latency by 40ms" | "40ms latency reduction on the order routing path eliminated the queue backlog that was causing 3–5 missed fills per day at market open" |
| "Migrated CI pipeline to GitHub Actions" | "CI migration cut deployment lead time from 4.2 hours to 47 minutes — accelerating time-to-desk for every feature this year by ~3x" |

---

## Review Template — Individual Engineer

```markdown
### [Engineer Name] — [Year] Performance Summary

**Commercial Impact Score:** [High / Medium / Developing]

#### Top 3 Contributions

1. **[Initiative Name]**
   - Built: [one-line description]
   - Metric: [before → after]
   - Business impact: [PnL, risk, cost, or speed outcome]
   - Quote or stakeholder signal: [trading desk comment / MD acknowledgment]

2. [repeat]

3. [repeat]

#### Behavioral Signals
- **Velocity:** [on-time delivery rate, sprint commitment accuracy]
- **Quality:** [P1 incidents caused, code review cycle time, defect escape rate]
- **Collaboration:** [cross-team unblocking, knowledge transfer, on-call reliability]

#### Development Vector
[One sentence: what is this engineer's ceiling and what is the single investment that unlocks it next year]

#### Rating Recommendation
[Exceeds / Meets / Below] — supported by data above
```

---

## Review Template — Team Summary (for MD / Senior Stakeholder)

```markdown
## Equities Technology Squad — [Year] Summary
### For: [MD Name / Trading Desk Head]

**Bottom Line:** The 5-person squad delivered [X] production releases, maintained
[uptime %] across [systems], and directly enabled [$ volume / risk reduction /
cost savings] in [Year].

#### Business Impact — Top 5 Deliveries
| Delivery | Business Outcome | Desk / Stakeholder |
|---|---|---|
| [feature/fix] | [commercial outcome] | [who benefits] |

#### Operational Health
- Unplanned outages: [N] (vs. [N-1] prior year)
- Mean time to recovery: [X min] (vs. [X+Y] prior year)
- Deployment frequency: [N/month] (vs. [N-1] prior year)

#### Team Investment Recommendations
[2–3 sentences on headcount, tooling, or process investment needed to
maintain this trajectory in [Next Year]]
```

---

## The Caution Trap in Year-End Reviews

Your Hogan profile will push you toward:
- **Over-documentation:** Writing 5-page reviews full of technical detail that no MD will read past paragraph 2
- **Team attribution only:** Hiding individual performance behind "the team delivered X" (protects you from rating conversations but destroys your credibility as a manager)
- **Avoiding commercial translation:** Assuming the business stakeholder will infer the value — they won't
- **Recency bias:** Defaulting to the last 6 weeks of performance data instead of the full year

**The Dimon Override:** Before submitting any review, ask yourself: "If I read this aloud to the trading desk head in 90 seconds, would they be able to articulate why this engineer deserves their compensation?" If not, rewrite it.

---

## Metrics to Capture All Year (Not Just at Review Time)

Maintain a running log:
```
- Deployment count and success rate (monthly)
- P1/P2 incident count and MTTR
- Sprint commitment accuracy rate (committed vs. delivered)
- Code review cycle time (PR open → merge)
- Stakeholder mentions / commendations (email trail, Slack, MD feedback)
- Business feature adoption rate (trading desk usage post-launch)
```

---

## Weekly Experiments

1. **This week:** Write one IMPACT narrative for a delivery your team made in the last 30 days. Send it to your MD as a "Q[X] delivery brief" — one paragraph, commercial framing, no technical jargon. Measure the response.
2. **This week:** Start a "wins log" shared doc for your team. Any time a stakeholder gives positive signal (Slack, email, verbal), log it with date and name. This is your review ammunition.
3. **This week:** Pull last quarter's metrics (deployments, incidents, cycle time). Write the one-sentence business translation for each. Practice converting engineering output into commercial language fluently.
