# Pillar 06 — Situational Leadership in Tech
## Matching Leadership Style to Engineer Task Maturity

**Layer:** Team | **Great Leader Anchor:** Andy Grove (Intel) | **Related:** [Pillar 08](./08-will-skill-matrix.md) · [Pillar 01](./01-performance-feedback.md)

**Hogan Filter — Your Caution Trap:** You over-direct senior engineers on production decisions they should own (compressing their autonomy), and under-direct junior engineers (assuming they'll ask for help rather than struggling silently). Both failure modes are driven by production anxiety. Result: senior architects disengage; junior devs ship bugs you catch too late.

**Anti-Caution Directive:** Leadership style is a task-specific dial, not a personality trait. The same engineer needs D1 on an unfamiliar incident runbook and D4 on the framework they designed. Match to task maturity, not to your anxiety.

---

## In 60 Seconds

Grove's principle: **the appropriate management style is determined by the employee's task-relevant maturity — not their overall seniority.** A 10-year senior engineer who has never run a production incident is a D1 on incident command. Treat them accordingly. The desk's risk exposure doesn't care about anyone's title.

---

## The Core Framework: Task Maturity → Leadership Style

```
                   HIGH SKILL
                       │
         DELEGATE (D4) │ SUPPORT (D3)
         High W + High S│ Variable W + High S
         Own outcome,   │ Collaborate, remove
         step back      │ blockers, encourage
  ───────────────────────┼────────────────────
         COACH (D2)     │ DIRECT (D1)
         Growing skill  │ High W + Low S
         + will         │ Explicit instructions
         Ask questions, │ + close follow-up
         provide structure│
                   LOW SKILL
          LOW WILL ◄──────────────────► HIGH WILL
```

| Style | Profile | Your Role | Equities Tech Example |
|---|---|---|---|
| **D1 — Direct** | High will, low skill | Explicit instructions + close follow-up | Junior dev on first production hotfix |
| **D2 — Coach** | Growing skill, variable will | Explain the why, ask questions, provide structure | Mid-level learning incident command |
| **D3 — Support** | High skill, variable confidence | Collaborate, encourage, remove blockers | Senior engineer on a risky migration |
| **D4 — Delegate** | High skill + will | Set the outcome, step back, hold accountability | Senior architect on core framework rewrite |

---

## Leadership Style Scripts by Context

### D1 — Direct: Junior Dev on Production Hotfix
```
"Stop. Before you touch production, exact sequence:
1. Post in #incidents: 'Investigating [symptom] on [service]'
2. Pull last 15 minutes of logs from [specific service endpoint]
3. Do NOT restart the service until you have a written hypothesis
4. Tag me before any config change — I review first

I'll be on Slack. Ping me every 10 minutes with a status.
Here's the runbook — start at step 3."
```

### D2 — Coach: Mid-Level Learning Incident Command
```
"You've got the technical skills. Here's the gap to close: communication
under pressure. When you're in an incident, narrate your diagnosis to the
channel in real time — not when you've found the answer. The trading desk
needs status, not silence. Even 'still investigating' beats 15 minutes of
nothing.

Walk me through your current read on the failure mode before you act.
I'll ask questions, not give answers."
```

### D3 — Support: Senior Engineer on Risky Migration
```
"You know this system better than I do and the migration plan is solid.
I want to remove every external blocker for you — the budget approval, the
cross-team dependency with infra, the prod access request that's been
sitting for 3 days.

What's the one thing outside your control that could derail the timeline?
That's where I focus. The technical execution is yours."
```

### D4 — Delegate: Senior Architect on Framework Rewrite
```
"This is yours. Own the architecture, own the delivery dates, own the
communication to stakeholders. I want a weekly 5-minute async update and
an immediate flag if you hit a decision that breaks another team's contract.

I won't be reviewing PRs unless you ask me to. That is not abdication —
that is appropriate trust at your level. Tell me what success looks like
in 8 weeks and I'll hold you to it."
```

---

## The Most Common Situational Leadership Errors

| Error | Pattern | Consequence |
|---|---|---|
| Inverse delegation | Delegating D1-level task to an engineer without the skill | Silent failure — junior ships broken code to prod |
| Seniority bias | Directing a D4 because you're anxious about the outcome | Senior engineer disengages, exits, or routes around you |
| Uniform check-ins | Same 30-min weekly 1:1 format for all 5 engineers | Over-coaching high performers, under-supporting struggling ones |
| Risk absorption | Taking D3/D4 decisions yourself to eliminate uncertainty | Engineers don't grow; you become the delivery bottleneck |

---

## Quarterly Calibration Conversation

Ask each engineer directly:
```
"For [specific system or responsibility], on a scale of 1–4:
- How confident are you in your technical ability to handle this solo?
- How motivated are you to own this domain right now?"

Then be transparent:
"Based on what I observe, I think you're at [D-level] on this.
Here's how I'm adjusting how I work with you on it this quarter."
```

Naming your leadership style explicitly builds more trust than any team-building exercise.

---

## The Caution Trap in Situational Leadership

Your Hogan profile will push you toward:
- **Defaulting to D1/D2 for everyone** when production risk is high — even for your most capable engineers
- **Not delegating incidents** because you want control of the outcome
- **Rescuing D1 engineers too quickly** — jumping in before they've had a chance to develop the skill
- **Uniform leadership style** — treating all five engineers the same because differentiation feels risky

**The Grove Override:** Before any leadership interaction, ask: "What is this engineer's task-relevant maturity on *this specific task?*" Match your style to that answer — not to your anxiety about the outcome. The most dangerous failure in equities tech is directing a D4 engineer like a D1. They will leave.

---

## Weekly Experiments

1. **This week:** For each of your 5 engineers, write their D-level for their top 3 current responsibilities. Where you're using D1/D2 for a D3/D4 engineer, identify one concrete place to step back this sprint.
2. **This week:** Identify your highest-maturity engineer. Find one decision you currently make for them that they should own. Transfer it explicitly — name the transfer in your 1:1 this week.
3. **This week:** In the next production incident, resist the impulse to direct immediately. Let your most capable on-call engineer narrate their diagnosis for 5 minutes before you intervene. The gap between their process and best practice is your D2 coaching agenda.

---

*Next: [Pillar 07 — Building High-Performance Teams](./07-building-high-performance-teams.md) | [Back to README](./README.md)*
