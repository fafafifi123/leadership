# Pillar 15 — Blameless Post-Mortem Culture
## Running RCAs That Generate Learning Without Blame or Caution Amplification

**Great Leader Anchor:** Sidney Dekker (Just Culture / Field Guide to Human Error) + the Google SRE model
**Hogan Filter:** This pillar is a specific trap for you. After an incident, your Highly Cautious instinct is to identify exactly what went wrong and build a control to prevent it *ever* happening again. Done reflexively, this turns post-mortems into blame exercises and bolts on so many guardrails that velocity dies. Your caution doesn't just slow you down — left unmanaged, it slows the whole team down through process accretion.

---

## The Core Framework: Blameless RCA Structure

```
1. TIMELINE      — What happened, minute by minute. Facts only, no judgment.
2. IMPACT        — Business consequence. Quantified. Honest.
3. ROOT CAUSE    — The SYSTEMIC condition, not the human who clicked.
4. CONTRIBUTING  — The factors that made the failure possible (and likely).
5. WHAT WORKED   — What detection/response went RIGHT (reinforce it).
6. ACTION ITEMS  — Owned, dated, and PROPORTIONATE to the actual risk.
```

The discipline: **separate the human from the system.** Humans are not the cause of failure — they are the inheritors of systems that made failure possible.

---

## Sidney Dekker — The Second Story

Dekker's foundational insight from *Just Culture*: every incident has two stories.

> **The First Story (blame):** "Engineer X deployed without checking, caused the outage."
> **The Second Story (system):** "The deploy process *allowed* a config push without validation, during market hours, with no automated rollback. Any engineer would eventually trigger this."

**The cautious leader stops at the First Story and adds a control: "All deploys now require my approval."** This is the worst possible outcome — it centralizes a bottleneck, signals distrust, and treats a system flaw as a person flaw.

**The great leader pursues the Second Story:** *Why did the system let a human error become a production incident?* Fix the system, not the human.

```
The reframe for every finding:
  "Given the tools, pressure, and information available at the time,
   why did this action make sense to a competent engineer?"

If the answer is "it didn't, they were negligent" — that's rare and is a
performance conversation (Pillar 01/04), NOT a post-mortem item.
If the answer is "because the system invited it" — that's your action item.
```

---

## The Google SRE Model — Blamelessness as Velocity

Google SRE treats blameless post-mortems as a *speed* tool, not an HR nicety: **engineers who fear blame hide information, delay escalation, and avoid risky-but-necessary changes.** Blamelessness is what makes fast, honest incident response possible.

Three SRE rules to adopt:
1. **Error budgets, not zero-error mandates.** You will have incidents. Budget for them. A team with zero incidents is a team shipping too slowly — which is *your* caution at the team level.
2. **The post-mortem is for learning, not punishment.** The moment it's used for performance management, people stop being honest, and you lose the data.
3. **Action items must be proportionate.** Not every incident deserves a new gate. Ask: "Is the cost of this control less than the cost of the incident recurring?"

---

## The Anti-Caution Action-Item Filter

This is your most important tool in this pillar. For every proposed action item, run it through:

```
| Question | If YES | If NO |
|---|---|---|
| Does this control's cost < expected incident cost? | Consider it | Reject it |
| Does it fix the SYSTEM or just add human vigilance? | Keep it | Redesign it |
| Will it slow EVERY future change to prevent a rare event? | Be very skeptical | OK |
| Could automation replace this human gate? | Automate instead | Manual OK |
| Am I adding this because of real risk or my anxiety? | Be honest | — |
```

**The rule:** Prefer *automated guardrails* over *human approval gates*. An automated pre-deploy validation check is a great action item. "Manager must approve all deploys" is your caution derailer wearing a process costume.

---

## Post-Mortem Facilitation Script

```
OPENING (set the frame):
"This is blameless. We're here to understand how our SYSTEM allowed this,
not to find who to blame. Everyone in this room would have made the same
calls with the same information. Let's find the Second Story."

WHEN BLAME EMERGES ("X should have caught it"):
"Let's reframe. Why did the system let X's action become an incident?
What would have caught it automatically?"

WHEN OVER-CORRECTION EMERGES ("let's require sign-off on everything"):
"Before we add a gate that slows every future deploy — what's the actual
recurrence risk, and can we automate the check instead of gating on a human?"

CLOSING:
"Three proportionate action items, each owned and dated. What went RIGHT
that we want to reinforce? Good response is worth naming too."
```

---

## What Worked — The Forgotten Half

Cautious leaders catalogue failures exhaustively and ignore successes. Every post-mortem must name what the *detection and response* got right — because that's what you want repeated under pressure. Reinforcing good incident behavior builds the team confidence that counteracts everyone's caution, not just yours.

---

## The Caution Trap in Post-Mortems

Your Hogan profile will push you toward:
- **Stopping at the First Story** — blaming the human who clicked
- **Control accretion** — adding a new gate after every incident until velocity dies
- **Centralizing approval** — making yourself the bottleneck "to be safe"
- **Zero-incident fantasy** — treating any incident as unacceptable rather than budgeted
- **Ignoring what worked** — only cataloguing failure, never reinforcing good response

**The Dekker/SRE Override:** Incidents are systemic, not personal. Your job is to fix systems and *remove* friction, not add it. The best post-mortem often *deletes* a fragile process rather than adding a new one. Resist the urge to make every lesson a new rule.

---

## Weekly Experiments

1. **This week:** Take your last incident's action items. Run each through the Anti-Caution Filter. Identify any that add human vigilance where automation would work better — convert at least one.
2. **This week:** In your next post-mortem, open with the blameless frame script verbatim. When the first "X should have" appears, reframe it to the Second Story out loud. Watch the room's honesty change.
3. **This week:** Define your team's error budget for one critical system (e.g., "≤2 P2s/quarter is acceptable for this velocity"). Share it. Naming an acceptable failure rate is the structural cure for zero-incident caution.
