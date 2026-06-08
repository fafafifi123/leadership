# Pillar 04 — Talent Density & Stack Ranking
## High-Integrity Performance Management for a 5-Person Equities Tech Squad

**Layer:** Team | **Great Leader Anchor:** Steve Jobs (Apple) | **Related:** [Pillar 08](./08-will-skill-matrix.md) · [Pillar 01](./01-performance-feedback.md)

**Hogan Filter — Your Caution Trap:** You avoid differentiation — treating all five engineers as "solid contributors" to reduce the discomfort of ranking conversations. This creates a low-density team where your best engineer carries the weight of your weakest without recognition or consequence for either. On a 5-person squad, one C-player is a 20% density tax paid by the other four — in code quality, on-call load, and morale.

**Anti-Caution Directive:** Rank quarterly. Name the gap. Act within one sprint of naming it. Delayed PIP is not kindness — it is a compounding cost paid by your A-players.

---

## In 60 Seconds

Jobs's law: A-players want to work with A-players. The moment you tolerate a B-player who doesn't improve, they hire C-players to feel comfortable, and density collapses. For a 5-person trading technology team, talent density is not an HR concept — it is a production risk. A C-player's on-call gaps, code defects, and architectural blindspots become your P1 incidents.

---

## The Core Framework: 4-Dimension Quantitative Ranking

```
DIMENSION 1 — Technical Output (40%)
  Story points delivered vs. committed (sprint accuracy)
  PR merge rate and code review cycle time
  Production defect escape rate
  System complexity handled (P1 systems vs. low-criticality)

DIMENSION 2 — Operational Reliability (30%)
  On-call incident response time (paged → acknowledged)
  MTTR on incidents they personally owned
  Unplanned outages caused by their code changes

DIMENSION 3 — Team Leverage (20%)
  Knowledge transfer (documentation, runbooks, pair sessions)
  Unblocking others (cross-PR reviews, architectural guidance)
  Junior engineer development contribution

DIMENSION 4 — Commercial Awareness (10%)
  Understands how their system touches trading desk PnL or risk
  Proactively flags business-impact risks, not just technical ones
```

---

## The 5-Person Stack Rank Template

```
| Rank | Engineer | Technical | Ops     | Leverage | Commercial | Overall |
|------|----------|-----------|---------|----------|------------|---------|
|  1   | [Name]   |     A     |    A    |    B     |     A      |    A    |
|  2   | [Name]   |     A     |    B    |    A     |     B      |   A-    |
|  3   | [Name]   |     B     |    A    |    B     |     B      |   B+    |
|  4   | [Name]   |     B     |    B    |    C     |     B      |    B    |
|  5   | [Name]   |     C     |    B    |    B     |     C      |   C+    |
```

Rank 5 triggers an immediate conversation — not a mental note.

---

## Performance Intervention Scripts

### Script 1 — A-Player Recognition & Retention
```
"I want to be direct: you are the highest-impact engineer on this team.
In [specific quarter], you shipped [X deliveries], maintained [system] at
[uptime], and were the reason [business outcome] landed on time.

I'm making sure that's reflected in your comp review. More importantly —
what's your next 18-month technical challenge? Tell me what problem you wish
you were working on. I'd rather find it here than lose you to somewhere else."
```

### Script 2 — B-Player Growth Contract
```
"You're delivering consistently but there's a ceiling forming. The gap I see
is [specific dimension — e.g., operational ownership, cross-team leverage].

Here's my offer: I'll assign you lead ownership of [specific system or project]
for next quarter. Intentional stretch. In exchange: [specific behavioral target —
e.g., PR cycle time under 1 day, zero on-call escalations to me]. We review
at 8 weeks. Clear?"
```

### Script 3 — C-Player PIP Initiation
```
"I'm going to be direct because I respect you enough not to let this drift.

Over the last [N weeks]: [specific pattern — 3 production defects, 2 missed
sprint commitments, 1 escalated P2 incident that should have been resolved
at your level].

This isn't a surprise — I flagged [earlier instance] in our 1:1 on [date].
We're now at formal improvement plan territory.

Here's what that means: [measurable targets], [30/60-day timeline],
[support available from me], and [consequence if not met].
I want you to succeed here. But I need a different output trajectory
starting this sprint."
```

---

## Safe PIP / Exit Execution — 5-Person Team Sequencing

With only 5 engineers, a PIP or exit has immediate operational impact. Sequence matters:

1. **Before PIP initiation:** Ensure knowledge transfer plan exists for all systems they own
2. **During PIP period:** No new critical-path work — stabilize their current ownership scope
3. **Exit decision:** Pre-brief your MD and HR *before* the conversation — never after
4. **Post-exit:** Redistribute on-call temporarily; do not silently overload your A-players
5. **Backfill:** Start the hiring process at PIP initiation, not at exit decision (→ [Pillar 14](./14-hiring-for-equities-technology.md))

---

## The Caution Trap in Talent Management

Your Hogan profile will push you toward:
- **Rating inflation** — everyone gets "meets expectations" to avoid conflict
- **Delayed PIP** — waiting for a fourth or fifth event before formalizing
- **Protecting the weak** — shielding underperformers from high-stakes assignments that would surface the gap
- **Effort vs. output confusion** — rewarding visible effort rather than measurable business impact

**The Jobs Override:** Ask yourself quarterly — "If this engineer resigned tomorrow, would I fight to keep them?" If the answer is no for anyone on your 5, you already know what action is required. The longer you wait, the more you're taxing the engineers who are performing.

---

## Weekly Experiments

1. **This week:** Score each of your 5 engineers privately across the 4 dimensions. Identify your rank 5. Write down the one conversation you've been avoiding. Schedule it this week.
2. **This week:** Have a 15-minute retention conversation with your rank 1. Ask: "What technical problem are you not getting to work on that you wish you were?" Solve it, or lose them.
3. **This week:** Review the last 3 sprints. Calculate each engineer's story-point commitment accuracy. If anyone is consistently over-committing and under-delivering, that's your next SBI conversation — this week.

---

*Next: [Pillar 05 — Managing Up](./05-managing-up-influence-negotiation.md) | [Back to README](./README.md)*
