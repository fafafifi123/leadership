# Pillar 06 — Situational Leadership in Tech
## Dynamically Matching Leadership Style to Engineer Maturity

**Great Leader Anchor:** Andy Grove (Intel)
**Hogan Filter:** Your caution default is to over-direct senior engineers (micromanaging risk decisions that they should own) and under-direct junior engineers (assuming they will ask for help rather than silently struggling). Both patterns are driven by your anxiety about production risk — one compresses autonomy, the other creates invisible failure modes.

---

## The Core Framework: Task Maturity Matrix

Leadership style is not fixed — it is task-specific and engineer-specific. The same engineer may need Direction on an unfamiliar production system and pure Delegation on the framework they designed.

```
        HIGH SKILL
             │
    DELEGATE │ SUPPORT
    (D4)     │ (D3)
─────────────┼─────────────
    COACH    │ DIRECT
    (D2)     │ (D1)
             │
        LOW SKILL
         LOW WILL ◄──────────── ► HIGH WILL
```

| Quadrant | Profile | Your Role | Equities Tech Example |
|---|---|---|---|
| **D1 — Direct** | High will, low skill | Give explicit instructions + close follow-up | Junior dev on their first production hotfix |
| **D2 — Coach** | Some skill, variable will | Explain the why, ask questions, provide structure | Mid-level engineer learning incident command |
| **D3 — Support** | High skill, variable confidence | Collaborate, encourage, remove blockers | Senior engineer leading a risky migration |
| **D4 — Delegate** | High skill, high will | Set the outcome, step back, hold accountability | Senior architect owning a core framework rewrite |

---

## Andy Grove's Task Maturity Principle

Grove's management model from *High Output Management* is precise: **"The appropriate management style for any situation is determined by the employee's task-relevant maturity — not their overall seniority or how long they've been at the company."**

A 10-year senior engineer who has never run a production incident is a D1 on incident command. Treat them accordingly — the risk to the trading desk is too high to treat them as D4 because of their title.

---

## Leadership Style Scripts by Context

### D1 — Direct: Junior Dev on Production Hotfix
```
"Stop. Before you touch production, here's the exact sequence:
1. Post in the #incidents channel: 'Investigating [symptom]'
2. Pull the last 15 minutes of logs from [specific service]
3. Do NOT restart the service until you have a hypothesis
4. Tag me before any config change — I'll review it first

I'll be on Slack. Ping me every 10 minutes with a status."
```

### D2 — Coach: Mid-Level Engineer Learning Incident Command
```
"You've got the technical skills for this. Here's the gap I want you to close:
communication under pressure.

When you're in an incident, narrate your diagnosis to the channel in real time —
not when you've found the answer. The trading desk needs status, not silence.
Tell me: what's your read on the current failure mode? Walk me through it
before you act. I'll ask questions, not give answers."
```

### D3 — Support: Senior Engineer on Risky Migration
```
"You know this system better than I do. The migration plan is solid.
What I want to do is remove every external blocker for you —
budget, cross-team dependencies, the prod access request that's been
sitting with infra for 3 days.

What's the one thing outside your control that could derail the timeline?"
```

### D4 — Delegate: Senior Architect on Framework Rewrite
```
"This is yours. Own the architecture, own the delivery dates, own the
communication to stakeholders. I want a weekly 5-minute async update
and a flag if you hit a decision that affects another team's contract.

I won't be reviewing PRs on this unless you ask me to.
That's not abdication — that's appropriate trust at your level."
```

---

## The Most Common Situational Leadership Errors

| Error | Pattern | Consequence |
|---|---|---|
| Inverse delegation | Delegating to a D1 because you are busy | Silent failure — junior ships broken code to prod |
| Seniority bias | Directing a D4 because of production risk anxiety | Senior engineer disengages, exits, or routes around you |
| Uniform check-ins | Same 30-min weekly 1:1 format for all 5 engineers | Over-coaching high performers, under-supporting struggling ones |
| Risk absorption | Taking D3/D4 decisions yourself to eliminate uncertainty | Engineers don't develop; you become the bottleneck |

---

## Calibration Conversation — Quarterly

Ask each engineer directly:
```
"For [specific system or responsibility], on a scale of 1–4:
- How confident are you in your technical ability to handle this independently?
- How motivated are you to own this domain right now?"

Then tell them:
"Based on what I'm observing, I think you're at [D-level] on this.
Here's how I'm going to adjust how I work with you on it."
```

This conversation alone — naming your leadership style explicitly — builds more trust with engineers than any team-building exercise.

---

## The Caution Trap in Situational Leadership

Your Hogan profile will push you toward:
- **Defaulting to D1/D2 for everyone** when production risk is high — even for your most capable engineers
- **Not delegating incidents** to senior engineers because you want control of the outcome
- **Rescuing D1 engineers too quickly** — jumping in with answers before they've had a chance to develop the skill

**The Grove Override:** Before any leadership interaction, ask: "What is this engineer's task-relevant maturity on *this specific task?*" Then match your style to that, not to your anxiety about the outcome.

---

## Weekly Experiments

1. **This week:** For each of your 5 engineers, write their D-level for their top 3 current responsibilities. Where you are using D1/D2 for a D3/D4 engineer, identify one concrete place to step back this sprint.
2. **This week:** Identify your highest-maturity engineer. Find one decision you currently make for them that they should own. Transfer it explicitly — name the transfer in your 1:1.
3. **This week:** In the next production incident, resist the impulse to direct immediately. Let your most capable on-call engineer narrate their diagnosis for 5 minutes before you intervene. Observe the gap between their natural process and best practice — that gap is your D2 coaching agenda.
