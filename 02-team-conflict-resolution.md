# Pillar 02 — Team Conflict Resolution
## De-escalating Technical Disputes in High-Stakes Trading Systems

**Layer:** Team | **Great Leader Anchor:** Nelson Mandela | **Related:** [Pillar 06](./06-situational-leadership.md) · [Pillar 08](./08-will-skill-matrix.md)

**Hogan Filter — Your Caution Trap:** You avoid conflict by staying neutral too long, hoping engineers self-resolve. In a 5-person team, unresolved friction metastasizes fast — one architecture dispute left open for two sprints can split the team into factions that slow every subsequent delivery. Your passivity reads as weakness to engineers who are waiting for a decision.

**Anti-Caution Directive:** Conflict is resolved by inserting structure, not by waiting for it to cool. You are the decision-forcing mechanism. Name the shared constraint. Make the call. Close the loop in writing — today.

---

## In 60 Seconds

Every technical dispute has two layers: the technical argument and the underlying interest (on-call burden, ownership, career visibility, latency anxiety). Resolution means separating them. Your job is not to determine who is technically correct — it is to surface the shared constraint and make the decision that satisfies it best. Then close in writing.

---

## The Core Framework: ARIA

```
ACKNOWLEDGE:  Surface and validate both positions without judgment
ROOT CAUSE:   Separate the technical argument from the underlying interest
INTEGRATE:    Find the shared constraint (latency, risk, timeline, ownership)
ALIGN:        Make a decision. Own it. Close the loop in writing today.
```

---

## Mandela's Operating Principle

**"Speak to a man's interests, not his positions."**

In equities tech:
- An engineer's **position** is: "We should use Kafka for this."
- Their **interest** is: "I need this system to not page me at 3am."

Conflict resolution is never about who is technically right. It is about surfacing what constraint each engineer is protecting and finding the decision that satisfies those constraints best.

---

## The Four Conflict Archetypes in Equities Tech

### Archetype 1 — Architecture / Tech Stack Dispute
**Scenario:** Two engineers disagree on gRPC vs REST for a new internal pricing service. PR comments are getting personal.

```
"I'm stopping this debate and reframing it. We are not deciding gRPC vs REST
in the abstract. We're deciding: given our P99 latency budget of 2ms, our
existing Protobuf investment, and our team's operational familiarity — which
option reduces production risk for us specifically?

One page each, 48 hours, addressing those three constraints only.
I'll make the call Thursday. This is not up for extended debate."
```

### Archetype 2 — Tech Debt vs. Feature Velocity
**Scenario:** Senior engineer refuses new feature tickets: "The legacy order routing module is a time bomb."

```
"Your concern about the routing module is logged and I agree it's a real risk.
Here's the constraint: the desk needs this feature by [date] — not negotiable.

Here's the offer: 20% of this sprint goes to routing module hardening — you
own that scope. Feature tickets move in parallel. This is not a choice between
safety and velocity — we are doing both at reduced scale.

Can you work within that frame? I need a yes or a specific counter-proposal
by end of today."
```

### Archetype 3 — Ownership / CODEOWNERS Friction
**Scenario:** Two engineers both claim ownership of a shared library — conflicting PRs, broken CI builds.

```
"We have a CODEOWNERS gap and that's my failure for not defining it earlier.

Effective today: [Engineer A] owns the API surface and versioning contract.
[Engineer B] owns the performance internals and benchmarking suite.
All PRs touching this library require both approvals.

I'm updating CODEOWNERS now. This is not a discussion — it's a decision.
Bring specific concerns about the boundary to your next 1:1 if they exist."
```

### Archetype 4 — On-Call Fairness Dispute
**Scenario:** Engineers dispute rotation fairness; one claims the other consistently gets the quieter shifts.

```
"Pull the PagerDuty data for the last 3 months: incident count and MTTR by
engineer. We make this decision with data, not perception.

If it shows imbalance, I'll restructure the rotation this week.
If it doesn't, we close this conversation and I expect full engagement on
the current rotation from both of you."
```

---

## Conflict Escalation Threshold — 5-Person Team

| Signal | Your Action | Timeline |
|---|---|---|
| Disagreement in Slack/PR comments | Monitor 24h, then facilitate async | 24–48h |
| Persists into second sprint | 30-min tripartite: you + both engineers | Within 3 days |
| Output affected — blocked PRs, broken builds | Immediate decision call — you own the outcome | Same day |
| Personal friction visible to the team | Private 1:1s with both, then joint session | Within 48h |

---

## The Caution Trap in Conflict

Your Hogan profile will push you toward:
- **Delayed intervention** — waiting until the conflict is visible to the whole team
- **False balance** — treating every technical dispute as 50/50 when one position is clearly stronger
- **Consensus-seeking** — trying to get everyone to agree instead of making the call
- **Avoiding the ego component** — pretending the interpersonal dimension doesn't exist

**The Mandela Override:** Insert structure. Name the shared constraint. Make the call. Write it down. Engineers don't need a manager who makes everyone feel heard indefinitely — they need a decision so they can ship.

---

## Weekly Experiments

1. **This week:** Audit your sprint for unresolved technical disagreements in PR comments or Slack threads older than 48 hours. For each one, intervene with a decision — not a question.
2. **This week:** In your next team meeting, explicitly name the team's shared north star constraint (e.g., "Zero unplanned outages during market hours this quarter"). A named shared constraint defuses most architectural ego battles before they start.
3. **This week:** Update or create a `CODEOWNERS` file for your top 3 most-contested shared modules. Eliminate ownership ambiguity as a structural intervention, not an interpersonal one.

---

*Next: [Pillar 03 — Year-End Reviews](./03-year-end-review-summaries.md) | [Back to README](./README.md)*
