# Pillar 01 — Performance Feedback
## Radical Candor via SBI in Equities Technology

**Great Leader Anchor:** Andy Grove (Intel)
**Hogan Filter:** Your caution default is to soften feedback with qualifiers, frame criticism as "observations," and delay hard conversations until the quarterly review. That gap costs the team 4–6 weeks of correctable underperformance per cycle.

---

## The Core Framework: SBI (Situation → Behavior → Impact)

Strip emotional weight. Anchor every feedback exchange in observable engineering facts.

```
SITUATION:  When [specific sprint / incident / code review / deployment window]
BEHAVIOR:   You [concrete, observable action or inaction — no adjectives]
IMPACT:     It resulted in [measurable outcome tied to system, team, or business]
```

**Bad (Cautious Default):**
> "I've noticed you've maybe been a bit slower on tickets lately — just something to think about."

**Good (Grove Standard):**
> "In Sprint 14, three of your five assigned tickets missed the Thursday cut. That pushed two trading-desk features into the next release cycle, which the desk flagged as a delay to their end-of-day reporting workflow."

---

## Andy Grove's Feedback Operating System

Grove ran Intel's engineering org on the principle: **"A manager's output = the output of their team + the output of the adjacent teams they influence."**

His feedback model was clinical, not cruel:
- **High-frequency, low-latency:** Feedback within 48 hours of the observable event — not at the 6-month review.
- **Metric-anchored:** Attach a number. "Slow" is useless. "P95 PR review time was 4.2 days vs. team target of 1.5" is actionable.
- **Separated from compensation:** Feedback is a performance accelerator, not a threat signal.

---

## Equities Tech SBI Scripts

### Script 1 — Code Quality Slump
```
Situation:  During the last 3 code reviews (Jira tickets EQ-441, EQ-447, EQ-453)
Behavior:   Error handling for null Protobuf fields was absent, requiring senior review
            to catch before merge.
Impact:     Two of those PRs required rework cycles that added 1.5 days each to
            deployment lead time. For the next market-open feature, that's the
            difference between shipping Tuesday and shipping Thursday.
```

### Script 2 — Slow Incident Response
```
Situation:  During the P1 pricing feed outage on [date] between 14:32–14:58 EST
Behavior:   You were paged at 14:34 but your first Slack acknowledgment came at 14:51.
Impact:     The 17-minute gap meant trading desk escalated to my MD before we had
            a status update. That's a trust deficit we now have to rebuild upstream.
```

### Script 3 — Missed Deployment Deadline
```
Situation:  The React visualizer hotfix was scoped for Wednesday's 18:00 release window.
Behavior:   Final QA sign-off wasn't submitted until 17:52, leaving zero buffer for
            rollback validation.
Impact:     We deployed with 8 minutes of safety margin on a production trading system.
            That risk profile is unacceptable regardless of whether it went clean.
```

---

## The Caution Trap in Feedback

Your Hogan profile will push you toward:
- **Sandwiching** the hard message between praise (dilutes the signal)
- **Adding qualifiers:** "I might be wrong, but..." (destroys credibility)
- **Waiting** for a pattern of 3–4 events before speaking (too late)
- **Framing it as a question:** "Do you think the timeline was realistic?" (avoids accountability)

**The Grove Override:** Deliver the feedback as a statement of observed fact, not a hypothesis for debate. You are not asking for their interpretation of what happened. You are describing what happened and what it cost.

---

## Feedback Cadence for a 5-Person Team

| Format | Frequency | Duration | Scope |
|---|---|---|---|
| 1:1 Feedback | Weekly | 30 min | 1 SBI item minimum per session |
| Sprint Retro | Bi-weekly | 60 min | Team-level behavioral patterns |
| Micro-feedback | Same-day | 5 min (async Slack) | Catches and corrections in-flight |
| Written Review | Quarterly | Written doc | Aggregated SBI log → formal record |

---

## Weekly Experiments

1. **This week:** Identify one engineer who has had a performance drift in the last sprint. Deliver one SBI conversation within 48 hours — no sandwich, no qualifiers.
2. **This week:** Start a private feedback log. For each 1:1, write one Situation-Behavior-Impact entry before the meeting. Show up prepared with data, not impressions.
3. **This week:** Set a personal rule — if an engineering behavior negatively impacted a system or stakeholder, it gets a feedback conversation within 2 business days. No waiting for the quarterly cycle.
