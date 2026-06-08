# Pillar 01 — Performance Feedback
## Radical Candor via SBI in Equities Technology

**Layer:** Team | **Great Leader Anchor:** Andy Grove (Intel) | **Related:** [Pillar 08](./08-will-skill-matrix.md) · [Pillar 04](./04-talent-density-stack-ranking.md)

**Hogan Filter — Your Caution Trap:** You soften feedback with qualifiers, frame criticism as "observations," and delay hard conversations until the quarterly review. That gap costs 4–6 weeks of correctable underperformance per cycle. The trading desk does not get 6-week grace periods — neither does your team.

**Anti-Caution Directive:** Feedback within 48 hours of the event. No sandwiching. No qualifiers. State the observable fact and the business cost. Then stop talking.

---

## In 60 Seconds

Feedback is a performance accelerator, not a threat signal. Delivered clinically, anchored in observable engineering facts, and decoupled from compensation, it is the highest-leverage management tool on a 5-person team. One delayed feedback conversation compounds into a sprint of degraded output that the trading desk eventually feels.

---

## The Core Framework: SBI

```
SITUATION:  When [specific sprint / incident / code review / deployment window]
BEHAVIOR:   You [concrete, observable action or inaction — no adjectives]
IMPACT:     It resulted in [measurable outcome tied to system, team, or business]
```

**Caution default:**
> "I've noticed you've maybe been a bit slower on tickets lately — just something to think about."

**Grove standard:**
> "In Sprint 14, three of your five assigned tickets missed the Thursday cut. That pushed two trading-desk features into the next release cycle, which the desk flagged as a delay to their end-of-day reporting workflow."

---

## Andy Grove's Feedback Operating System

Grove ran Intel's engineering org on the principle: **"A manager's output = the output of their team + the output of the adjacent teams they influence."**

His feedback model:
- **High-frequency, low-latency:** Feedback within 48 hours of the observable event — not at the 6-month review.
- **Metric-anchored:** Attach a number. "Slow" is useless. "P95 PR review time was 4.2 days vs. team target of 1.5" is actionable.
- **Separated from compensation:** Feedback is a performance signal, not a threat. Never conflate them in the same conversation.

---

## Equities Tech SBI Scripts

### Script 1 — Code Quality Slump
```
Situation:  During the last 3 code reviews (tickets EQ-441, EQ-447, EQ-453)
Behavior:   Error handling for null Protobuf fields was absent, requiring senior
            review to catch before merge.
Impact:     Two PRs required rework cycles adding 1.5 days each to deployment
            lead time. For the next market-open feature, that's the difference
            between shipping Tuesday and shipping Thursday.
```

### Script 2 — Slow Incident Response
```
Situation:  During the P1 pricing feed outage on [date] between 14:32–14:58 EST
Behavior:   You were paged at 14:34 but your first Slack acknowledgment came at 14:51.
Impact:     The 17-minute gap meant the trading desk escalated to my MD before we
            had a status update. That's a trust deficit we now have to rebuild
            upstream — and it was avoidable.
```

### Script 3 — Missed Deployment Deadline
```
Situation:  The React visualizer hotfix was scoped for Wednesday's 18:00 release window.
Behavior:   Final QA sign-off wasn't submitted until 17:52 — 8 minutes of safety
            margin with no rollback validation window.
Impact:     We deployed with near-zero margin on a live trading system. That risk
            profile is unacceptable regardless of whether it went clean.
```

### Script 4 — Protobuf Schema Regression
```
Situation:  In the order state machine refactor merged Tuesday
Behavior:   Protobuf schema version was incremented without updating the consumer
            deserialization logic in the risk aggregation service.
Impact:     3 hours of silent data corruption before detection. Desk operated on
            stale position data during the morning session.
```

---

## The Caution Trap in Feedback

Your Hogan profile will push you toward:
- **Sandwiching** the hard message between praise — dilutes the signal
- **Adding qualifiers:** "I might be wrong, but..." — destroys credibility
- **Waiting** for a 3–4 event pattern before speaking — 4–6 weeks too late
- **Framing as a question:** "Do you think the timeline was realistic?" — avoids accountability

**The Grove Override:** Deliver the feedback as a statement of observed fact, not a hypothesis for debate. You are describing what happened and what it cost. Then you stop talking and let them respond.

---

## Feedback Cadence — 5-Person Team

| Format | Frequency | Duration | Scope |
|---|---|---|---|
| 1:1 Feedback | Weekly | 30 min | 1 SBI item minimum per session |
| Sprint Retro | Bi-weekly | 60 min | Team-level behavioral patterns |
| Micro-feedback | Same-day | 5 min async | In-flight corrections |
| Written Review | Quarterly | Written doc | Aggregated SBI log → formal record |

---

## Weekly Experiments

1. **This week:** Identify one engineer who has had performance drift in the last sprint. Deliver one SBI conversation within 48 hours — no sandwich, no qualifiers.
2. **This week:** Start a private feedback log. For each 1:1, write one SBI entry *before* the meeting. Show up with data, not impressions.
3. **This week:** Set a rule — any engineering behavior that negatively impacted a system or stakeholder gets a feedback conversation within 2 business days. No exceptions.

---

*Next: [Pillar 02 — Team Conflict Resolution](./02-team-conflict-resolution.md) | [Back to README](./README.md)*
