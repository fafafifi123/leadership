# Pillar 05 — Managing Up, Influence & Negotiation
## Aligning Your Tech Roadmap to Business Incentives and MD Priorities

**Layer:** Business | **Great Leader Anchor:** Jamie Dimon (JPMorgan Chase) | **Related:** [Pillar 10](./10-executive-presence-selling-the-team.md) · [Pillar 09](./09-effective-technical-communication.md)

**Hogan Filter — Your Caution Trap:** You treat managing-up as reporting — giving status updates when asked, documenting risks accurately, and waiting for senior stakeholders to pull information from you. This creates a visibility gap where your team's strategic value is consistently underpriced by the business. Passive reporting is not stakeholder management; it is invisibility.

**Anti-Caution Directive:** Lead up — don't just report up. Own the narrative before someone else does. Every MD interaction is a 90-second pitch: commercial headline, trade-off, and one ask.

---

## In 60 Seconds

Your MD does not think in sprints. They think in risk, revenue, and headcount. If you communicate in sprints, you're speaking a language they have to translate before they can value you. Dimon's rule: speak budget, not backlog. If you can't answer "commercial headline, trade-off, what I need from you" before you send the email — you're not ready.

---

## The Core Framework: RATE

```
ROADMAP:          Know your 90-day technical plan in commercial terms
ALIGNMENT:        Map each initiative to a specific MD or desk priority
TENSION:          Surface trade-offs before they surface themselves
EXECUTION SIGNAL: Give stakeholders a weekly proof point — shipped, not planned
```

---

## Dimon's Managing-Up Doctrine

**Rule 1 — Own the Narrative Before Someone Else Does**
If your system had an incident, your MD hears it from you first — with root cause and fix timeline — before the trading desk escalates. A 2-minute heads-up call is worth 2 hours of damage control.

**Rule 2 — Speak Budget, Not Backlog**

| Sprint Language | MD Language |
|---|---|
| "Refactoring the order state machine" | "Eliminating the #1 source of T+0 reconciliation failures — 2–3 manual ops tickets per week" |
| "Upgrading our React visualizer" | "Reducing trading desk end-of-day position reporting latency from 8s to under 1s" |
| "Adding Protobuf schema validation" | "Preventing the silent data corruption mode that cost 3 hours of stale desk data in Q2" |
| "Improving CI/CD pipeline" | "Cutting deployment lead time from 4.2h to 47min — features hit the desk 5x faster" |

**Rule 3 — Pre-wire Decisions Before Meetings**
Before your quarterly roadmap review, have 15-minute bilateral conversations with each key stakeholder. The formal meeting confirms alignment — it does not build it. A meeting where you're still selling is a meeting you lost before it started.

---

## The Stakeholder Map — 5-Person Team Context

| Stakeholder | What They Care About | Your Translation |
|---|---|---|
| Managing Director | Risk, cost, headcount efficiency | Uptime, deployment velocity, cost avoidance |
| Trading Desk Head | Latency, fill rates, tool reliability | P99 latency, zero market-hour outages, fill improvement |
| Risk / Compliance | Audit trails, regulatory adherence | Change management discipline, automated controls |
| Product Owner | Feature delivery speed, roadmap clarity | Sprint predictability, clear scope management |
| Peer Tech Managers | Dependencies, shared infrastructure | Proactive cross-team communication, no surprise blockers |

---

## Managing-Up Scripts

### Script 1 — Proactive Weekly Update
```
Subject: Equities Tech — Week of [Date]

[MD Name],

Three points:

1. SHIPPED: [Feature/fix] — [one-sentence commercial impact]
2. RISK: [Upcoming dependency or constraint] — mitigation: [one sentence]
3. ASK: [One specific decision or resource needed, with deadline]

Full sprint board available if useful.
— [Your name]
```

### Script 2 — Roadmap Trade-off Negotiation
```
"I want to bring you a trade-off before the planning cycle locks.

The desk has asked for [Feature A] by [date]. Achievable, but it requires
deferring [infrastructure work B] — our risk buffer against [the specific
failure mode] we saw in [prior incident].

My recommendation: [Feature A] with a 2-week slip, giving time to harden [B].
But if the desk date is a hard commercial constraint, I need you to acknowledge
the deferred risk so I can manage our on-call posture accordingly.

Which world do you want?"
```

### Script 3 — Pushing Back on Scope Creep
```
"I can take this on. Here's what it means concretely: [New request X] replaces
[Existing commitment Y] in this sprint, or I need one additional engineer-week.

I'm not saying no. I'm saying the current plan has no slack, and I won't
overpromise and underdeliver on either item. Which is the higher priority?"
```

### Script 4 — The Resource Ask (Commercial Case)
```
"I'm making a commercial case, not a technical one.

Current state: [N engineers] covering [X systems, Y trading desks, Z critical
workflows]. Constraint: [specific capability gap — e.g., no dedicated on-call
redundancy, single point of failure on the pricing feed].

Business cost of constraint: [X incidents/year, Y hours manual ops, Z latency
impact on fills].

Ask: [1 engineer / $X tooling budget]. Expected return: [specific: 40%
reduction in P2 incidents, fill-rate improvement on [system], ops cost
avoidance of ~$X/year]. I can model the numbers in more detail if useful."
```

---

## Negotiation Principles

1. **Never negotiate against yourself.** Present one option with clear rationale — don't offer three choices and ask the MD to pick.
2. **Attach a cost to every "yes."** Every new request displaces something. Name what it displaces before agreeing.
3. **Surface constraints in week 1.** A constraint raised in week 1 is a planning input. In week 6 it's a failure.
4. **Use data as authority, not defense.** "Our P99 deployment lead time is 4.2 hours, which is why I need the CI budget" is stronger than "I think we need more CI budget."

---

## The Caution Trap in Managing Up

Your Hogan profile will push you toward:
- **Reporting defensively** — over-explaining technical constraints instead of proposing solutions
- **Waiting to be asked** — assuming your MD will pull information when they need it
- **Softening risks** — burying risk signals in technical jargon to avoid alarming stakeholders
- **Avoiding the ask** — never explicitly requesting resources, decisions, or air cover

**The Dimon Override:** Every interaction with your MD is a 90-second pitch. Commercial headline. Trade-off. What you need from them. If you can't answer all three, you are not ready to send the email.

---

## Weekly Experiments

1. **This week:** Send a proactive update to your MD using Script 1 above — even if nothing dramatic happened. The absence of drama is itself a signal worth sending.
2. **This week:** Identify one roadmap item where you haven't explicitly connected it to a business outcome for your MD. Write the one-sentence commercial translation and include it in your next communication.
3. **This week:** Find one pending decision that has been sitting with a senior stakeholder for more than 2 weeks. Pre-wire it: 10-minute bilateral conversation to align before the next formal meeting.

---

*Next: [Pillar 06 — Situational Leadership](./06-situational-leadership.md) | [Back to README](./README.md)*
