# Pillar 15 — Blameless Post-Mortem Culture
## Running RCAs That Generate Learning Without Blame or Control Accretion

**Layer:** Team | **Great Leader Anchors:** Sidney Dekker (Just Culture) · Google SRE | **Related:** [Pillar 09](./09-effective-technical-communication.md) · [Pillar 11](./11-strategic-decisiveness-under-uncertainty.md)

**Hogan Filter — Your Caution Trap:** After an incident, your Highly Cautious instinct is to identify exactly what went wrong and build a control to prevent it *ever* happening again. Done reflexively, this turns post-mortems into blame exercises and bolts on so many guardrails that velocity dies. Your caution doesn't just slow you down — left unmanaged, it slows the whole team through process accretion.

**Anti-Caution Directive:** The best post-mortem often *deletes* a fragile process rather than adding a new one. Incidents are systemic, not personal. Resist the urge to make every lesson a new rule.

---

## In 60 Seconds

Google SRE treats blameless post-mortems as a *speed* tool, not an HR nicety: engineers who fear blame hide information, delay escalation, and avoid risky-but-necessary changes. Blamelessness is what makes fast, honest incident response possible. Your caution produces the opposite: it adds gates, centralizes approval, and converts every incident into a new mandatory step — until deployment velocity dies death by a thousand controls.

---

## The Core Framework: Blameless RCA Structure

```
1. TIMELINE      Facts only, minute by minute. No judgment, no "should have."
2. IMPACT        Business consequence, quantified and honest.
3. ROOT CAUSE    The SYSTEMIC condition, not the human who clicked the button.
4. CONTRIBUTING  Factors that made failure possible — and likely.
5. WHAT WORKED   Detection and response that went RIGHT. Reinforce it.
6. ACTION ITEMS  Owned, dated, and PROPORTIONATE to actual risk.
```

The discipline: **separate the human from the system.** Humans are not the cause of failure — they are the inheritors of systems that made failure possible.

---

## Sidney Dekker — The Second Story

Every incident has two stories:

> **The First Story (blame):** "Engineer X deployed without checking, caused the outage."
> **The Second Story (system):** "The deploy process *allowed* a config push without validation, during market hours, with no automated rollback. Any engineer would eventually trigger this."

**The cautious leader stops at the First Story and adds a control:** "All deploys now require my approval." This is the worst possible outcome — it centralizes a bottleneck, signals distrust, and treats a system flaw as a person flaw.

**The great leader pursues the Second Story:** *Why did the system let a human error become a production incident?* Fix the system, not the human.

```
The reframe for every post-mortem finding:
  "Given the tools, pressure, and information available at the time,
   why did this action make sense to a competent engineer?"

If the answer is "it didn't — they were genuinely negligent":
  → Rare. Performance conversation (Pillar 01). Not a post-mortem item.

If the answer is "because the system invited it":
  → That is your action item. Fix the system.
```

---

## The Anti-Caution Action-Item Filter

For every proposed action item, run this test before adding it:

| Question | If YES | If NO |
|---|---|---|
| Does this control's cost < expected incident recurrence cost? | Consider it | Reject it |
| Does it fix the SYSTEM or add human vigilance? | Keep it | Redesign it |
| Will it slow EVERY future change to prevent a rare event? | Be skeptical | OK |
| Could automation replace this human gate? | Automate instead | Manual gate OK |
| Am I adding this because of real risk or my anxiety? | Be honest | — |

**The rule:** Prefer *automated guardrails* over *human approval gates*. An automated pre-deploy validation check is a great action item. "Manager must approve all deploys" is your caution derailer wearing a process costume.

---

## Post-Mortem Facilitation Script

```
OPENING (set the frame):
"This is blameless. We're here to understand how our SYSTEM allowed this,
not to find who to blame. Everyone in this room would have made the same
calls with the same information at the time. Let's find the Second Story."

WHEN BLAME EMERGES ("X should have caught it"):
"Let's reframe. Why did the system let X's action become an incident?
What would have caught it automatically?"

WHEN OVER-CORRECTION EMERGES ("let's require sign-off on everything"):
"Before we add a gate that slows every future deploy — what's the actual
recurrence risk, and can we automate the check instead of gating on a human?"

CLOSING:
"Three proportionate action items, each owned and dated. And before we finish:
what went RIGHT in our detection or response that we want to reinforce?"
```

---

## What Worked — The Forgotten Half

Cautious leaders catalogue failures exhaustively and ignore successes. Every post-mortem must name what the *detection and response* got right — because that's what you want repeated under pressure. Reinforcing good incident behavior builds team confidence and counteracts the caution that makes the next incident worse.

---

## The Error Budget Model

Google SRE treats incidents as budgeted, not catastrophic. Adopt this mindset:

```
Error Budget = 100% - SLA Target

Example: 99.9% SLA = 0.1% downtime budget = ~43 minutes/month

ABOVE budget: No incidents this month? You're shipping too slowly.
              The budget is there to be spent on velocity.
WITHIN budget: Operate normally. No emergency gates needed.
BELOW budget:  Freeze non-essential changes. Invest in reliability.
```

Naming an acceptable failure rate is the structural cure for zero-incident caution. A team that never has incidents is a team your caution has paralyzed.

---

## The Caution Trap in Post-Mortems

Your Hogan profile will push you toward:
- **Stopping at the First Story** — blaming the human who clicked
- **Control accretion** — adding a new gate after every incident until velocity dies
- **Centralizing approval** — making yourself the bottleneck "to be safe"
- **Zero-incident fantasy** — treating any incident as unacceptable rather than budgeted
- **Ignoring what worked** — cataloguing failure only, never reinforcing good response

**The Dekker/SRE Override:** Incidents are systemic, not personal. Your job is to fix systems and *remove* friction, not add it. The best post-mortem often deletes a fragile process rather than creating a new one.

---

## Weekly Experiments

1. **This week:** Take your last incident's action items. Run each through the Anti-Caution Filter. Identify any that add human vigilance where automation would work better — convert at least one.
2. **This week:** In your next post-mortem, open with the blameless frame script verbatim. When the first "X should have" appears, reframe it to the Second Story out loud. Watch the room's honesty change.
3. **This week:** Define your team's error budget for one critical system. Share it. Naming an acceptable failure rate is the structural cure for zero-incident caution.

---

*Next: [Pillar 16 — Cross-Team Dependencies](./16-cross-team-dependency-management.md) | [Back to README](./README.md)*
