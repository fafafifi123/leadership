# Pillar 05 — Managing Up, Influence & Negotiation
## Aligning Your Tech Roadmap to Business Incentives and MD Priorities

**Great Leader Anchor:** Jamie Dimon (JPMorgan Chase)
**Hogan Filter:** Your caution default is to treat managing-up as reporting — you give status updates when asked, document risks accurately, and wait for senior stakeholders to pull information from you. This creates a visibility gap where your team's strategic value is consistently underpriced by the business.

---

## The Core Framework: RATE (Roadmap → Alignment → Tension → Execution Signal)

```
ROADMAP:          Know your 90-day technical plan in commercial terms
ALIGNMENT:        Map each initiative to a specific MD or desk priority
TENSION:          Surface trade-offs before they surface themselves
EXECUTION SIGNAL: Give stakeholders a weekly proof point — shipped, not planned
```

---

## Dimon's Managing-Up Doctrine

Dimon does not manage up. He **leads up.** His principle: **"I never let my boss be surprised. I tell them the bad news first, fast, and with a solution already attached."**

For equities technology, this translates to three rules:

**Rule 1 — Own the Narrative Before Someone Else Does**
If your system had an incident, your MD hears it from you first — with a root cause and fix timeline — before the trading desk escalates. A 2-minute heads-up call is worth 2 hours of damage control.

**Rule 2 — Speak Budget, Not Backlog**
Your MD does not think in sprints. They think in risk, revenue, and headcount. Translate your roadmap:
- "We're refactoring the order state machine" → "We're eliminating the #1 source of T+0 reconciliation failures that generates 2–3 manual ops tickets per week"
- "We're upgrading our React visualizer" → "We're reducing trading desk latency for end-of-day position reporting from 8s to under 1s"

**Rule 3 — Pre-wire Decisions Before Meetings**
Dimon pre-wires every major decision through bilateral conversations before it hits a committee. Do the same: before your quarterly roadmap review, have 15-minute conversations with your key stakeholders individually. The meeting should confirm alignment, not build it.

---

## The Stakeholder Map — 5-Person Team Context

```markdown
| Stakeholder | What They Care About | Your Leverage |
|---|---|---|
| Managing Director | Risk, cost, headcount efficiency | Uptime, deployment velocity, cost avoidance |
| Trading Desk Head | Latency, fill rates, tool reliability | System performance, zero market-hour outages |
| Risk / Compliance | Audit trails, regulatory adherence | Change management discipline, documentation |
| Product Owner | Feature delivery speed, roadmap clarity | Sprint predictability, clear scope management |
| Peer Tech Managers | Dependencies, shared infrastructure | Proactive cross-team communication |
```

---

## Managing-Up Scripts

### Script 1 — Proactive Business Update (Weekly)
```
Subject: Equities Tech — Week of [Date] Delivery Signal

[MD Name],

Three points this week:

1. SHIPPED: [Feature/fix] — [one-sentence commercial impact]
2. RISK: [Upcoming dependency or constraint] — mitigation: [one sentence]
3. ASK: [One specific decision or resource needed from you, with deadline]

Full sprint board available if you want the detail.

— [Your name]
```

### Script 2 — Roadmap Negotiation
```
"I want to bring you a trade-off before the planning cycle locks.

The desk has asked for [Feature A] by [date]. Technically achievable, but it
requires us to defer [infrastructure work B], which is our risk buffer against
the [specific failure mode] we saw in [prior incident].

My recommendation is [Feature A] with a 2-week slip, giving us time to harden [B].
But if the desk date is a hard commercial constraint, I need you to acknowledge
the deferred risk in writing so I can manage the on-call posture accordingly.

Which world do you want?"
```

### Script 3 — Pushing Back on Scope Creep
```
"I can take this on. Here's what that means concretely: [New request X]
replaces [Existing commitment Y] in this sprint, or I need one additional
engineer-week of capacity.

I'm not saying no. I'm saying the current plan has no slack, and I won't
overpromise and underdeliver on either item. Which is the higher priority?"
```

---

## Negotiation Principles for Equities Tech

1. **Never negotiate against yourself.** Present one option with a clear rationale — don't offer three choices and ask the MD to pick. That's decision-offloading.
2. **Attach a cost to every "yes."** Every new request displaces something. Name what it displaces before agreeing.
3. **Make your constraints visible early.** A constraint surfaced in week 1 is a planning input. A constraint surfaced in week 6 is a failure.
4. **Use data as authority, not defense.** "Our P99 deployment lead time is 4.2 hours, which is why I need the CI infrastructure budget" is stronger than "I think we need more CI budget."

---

## The Caution Trap in Managing Up

Your Hogan profile will push you toward:
- **Reporting defensively:** Over-explaining technical constraints instead of proposing solutions
- **Waiting to be asked:** Assuming your MD will pull information from you when they need it
- **Softening risks:** Burying risk signals in technical jargon to avoid alarm — then getting caught off guard when the risk materializes
- **Avoiding the ask:** Never explicitly requesting resources, decisions, or air cover

**The Dimon Override:** Treat every interaction with your MD as a 90-second pitch. What is the commercial headline? What is the trade-off? What do you need from them? If you can't answer all three, you are not ready to send the email or schedule the meeting.

---

## Weekly Experiments

1. **This week:** Send a proactive update to your MD using the Script 1 template above — even if nothing dramatic happened. The absence of drama is itself a signal worth communicating.
2. **This week:** Identify one item on your current roadmap where you have not explicitly connected it to a business outcome for your MD. Write that one-sentence commercial translation and include it in your next status communication.
3. **This week:** Find one decision that has been pending with a senior stakeholder for more than 2 weeks. Pre-wire it: have a 10-minute bilateral conversation to align before the next formal meeting.
