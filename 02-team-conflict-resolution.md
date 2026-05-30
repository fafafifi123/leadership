# Pillar 02 — Team Conflict Resolution
## De-escalating Technical Disputes in High-Stakes Trading Systems

**Great Leader Anchor:** Nelson Mandela
**Hogan Filter:** Your caution default is to avoid conflict by staying neutral for too long, hoping engineers self-resolve. In a 5-person team, unresolved friction metastasizes fast — one architecture dispute left open for two sprints can split the team into factions that slow every subsequent delivery.

---

## The Core Framework: ARIA (Acknowledge → Root Cause → Integrate → Align)

```
ACKNOWLEDGE:   Surface and validate both technical positions without judgment
ROOT CAUSE:    Separate the technical argument from the ego argument
INTEGRATE:     Find the shared constraint (latency, risk, maintainability, timeline)
ALIGN:         Make a decision. Own it. Close the loop in writing.
```

---

## Mandela's Conflict Operating Principle

Mandela's negotiation framework was built on one foundational insight: **"Speak to a man's interests, not his positions."**

In equities technology terms:
- An engineer's **position** is: "We should use Kafka for this."
- Their **interest** is: "I need this system to not page me at 3am."

Conflict resolution in your team is never about who is technically right. It is about surfacing the underlying constraint each engineer is trying to protect — latency, ownership, on-call burden, career visibility — and finding the architectural decision that satisfies those constraints best.

---

## The Three Conflict Archetypes in Equities Tech

### Archetype 1 — Architecture / Tech Stack Dispute
**Scenario:** Two engineers disagree on whether to use gRPC or REST for a new internal pricing service.

**Resolution Script:**
```
"I'm going to stop this debate and reframe it. We are not deciding gRPC vs REST
in the abstract. We are deciding: given our P99 latency budget of 2ms, our
existing Protobuf schema investment, and our team's operational familiarity,
which option reduces production risk for us specifically?

Here's what I need from both of you: one page each, 48 hours,
addressing those three constraints only. I'll make the call Thursday."
```

### Archetype 2 — Tech Debt vs. Feature Velocity
**Scenario:** Senior engineer refuses to take new feature tickets because "the legacy order routing module is a time bomb."

**Resolution Script:**
```
"Your concern about the routing module is logged and I agree it's a real risk.
Here's the constraint I'm operating under: the trading desk needs this feature
by [date] and that is not negotiable.

What I'm offering: we allocate 20% of this sprint to routing module hardening —
you own that scope. In return, the feature tickets move forward in parallel.
This is not a choice between safety and velocity. We are doing both at reduced
scale. Can you work within that frame?"
```

### Archetype 3 — Ownership / Responsibility Friction
**Scenario:** Two engineers both claim ownership of a critical shared library, leading to conflicting PRs and broken builds.

**Resolution Script:**
```
"We have a CODEOWNERS gap. This is my failure to have not defined it clearly.
Effective today: [Engineer A] owns the API surface and versioning contract.
[Engineer B] owns the performance internals and benchmarking suite.

All PRs touching this library require both to approve.
I'm updating the CODEOWNERS file today. This is not up for re-debate."
```

---

## The Caution Trap in Conflict

Your Hogan profile will push you toward:
- **Delayed intervention:** Waiting until the conflict is visible to the whole team before acting
- **False balance:** Treating every technical dispute as 50/50 when one position is clearly stronger
- **Consensus-seeking:** Trying to get everyone to agree rather than making the call yourself
- **Avoiding the ego component:** Pretending the interpersonal dimension doesn't exist

**The Mandela Override:** Conflict is not resolved by waiting for it to cool. It is resolved by inserting structure. Your job is to be the decision-forcing mechanism — not the mediator who helps everyone feel heard indefinitely.

---

## Conflict Escalation Threshold — 5-Person Team

| Signal | Your Action | Timeline |
|---|---|---|
| Two engineers disagree in Slack/PR comments | Monitor 24h, then facilitate async resolution | 24–48h |
| Disagreement persists into second sprint | Schedule 30-min tripartite — you + both engineers | Within 3 days |
| Output is affected (blocked PRs, broken builds) | Immediate decision call — you own the outcome | Same day |
| Personal friction visible to team | Private 1:1s with both parties, then joint session | Within 48h |

---

## Weekly Experiments

1. **This week:** Audit your current sprint for any unresolved technical disagreements sitting in PR comments or Slack threads. For each one older than 48 hours, intervene with a decision — not a question.
2. **This week:** In your next team meeting, explicitly name the team's shared constraint (e.g., "Our north star is zero unplanned production outages this quarter"). A shared constraint defuses most architectural ego battles before they start.
3. **This week:** Update or create a `CODEOWNERS` file for your top 3 most-contested shared modules. Eliminate ownership ambiguity as a structural intervention.
