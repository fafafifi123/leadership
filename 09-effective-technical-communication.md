# Pillar 09 — Effective Technical Communication
## Mastering BLUF for Outages, Delays, and Architectural Pivots

**Layer:** Business | **Great Leader Anchor:** Andy Grove (Intel) | **Related:** [Pillar 05](./05-managing-up-influence-negotiation.md) · [Pillar 10](./10-executive-presence-selling-the-team.md)

**Hogan Filter — Your Caution Trap:** You front-load technical context before delivering the headline — explaining system architecture, edge cases, and risk analysis before telling the stakeholder what actually happened or what you need. This reads as defensive, not authoritative, and causes your audience to lose confidence before you reach the point.

**Anti-Caution Directive:** Business impact in sentence 1, always. Communicate before you are certain. An "investigating" message at minute 3 is worth more than a precise post-mortem at minute 45.

---

## In 60 Seconds

Grove's principle: **"Noise in the communication channel is not the receiver's problem — it is the sender's problem."** In equities technology, noise is technical jargon before the headline, passive voice that obscures ownership, probability hedging that delays the key message, and root cause explanation before business impact. Your caution produces all four. Strip them.

---

## The Core Framework: BLUF

```
B — Bottom Line:   State the conclusion or status in sentence 1
L — Level:         Calibrate technical depth to audience knowledge
U — Urgency:       Make the time-sensitivity explicit, not implied
F — Follow-up:     State one clear next action or decision needed
```

Test every communication: "If the reader stops after sentence 2, do they have everything they need to act?"

---

## Communication Templates by Scenario

### Template 1 — Production Outage (Market Hours)

**First message — within 3 minutes of detection:**
```
P1 INCIDENT — [System Name] | [Time EST]

Status: [Impacted / Degraded / Investigating]
Business impact: [what trading desk or operation is affected, right now]
Mitigation in progress: [what you're doing — one sentence]
Next update: [specific time, e.g., "14:55 EST"]

Incident commander: [name]
Bridge: [link]
```

**Follow-up — every 10 minutes until resolved:**
```
[Time EST] UPDATE

Status: [current state — any change]
Diagnosis: [one sentence — best current hypothesis on cause]
Action: [what is being executed right now]
ETA to resolution: [specific time or "unknown — next update at [time]"]
```

**Resolution message:**
```
RESOLVED — [System Name] | [Time EST]

Duration: [X minutes]
Root cause: [one sentence — no technical jargon in this message]
Business impact confirmed: [trades affected, data gaps, positions impacted]
Immediate fix: [what was done to restore service]
Full post-mortem: [date] — will circulate before EOD
```

---

### Template 2 — Project Delay

**Wrong (cautious default):**
> "Due to a number of technical complexities encountered during the integration phase, including some unexpected schema incompatibilities between the upstream pricing service and our downstream feed handler, which required revisiting our data transformation layer, the delivery timeline may need to be adjusted..."

**Right (BLUF):**
```
[Feature/Project Name] — Timeline Update

Bottom line: We are 5 business days late. New delivery date: [specific date].

Reason: Upstream pricing service schema changed without notice on [date].
Retrofit required 3 days of unplanned rework.

Impact to business: [what this delays — one sentence]
Mitigation: [what we're doing to compress remaining timeline]
Decision needed from you: [none / or specific ask with deadline]
```

---

### Template 3 — Architectural Change Proposal

```
Proposal: [Migration / Refactor / New System — one-line description]

Recommendation: Proceed with [Option A].

Business case:
- Current state costs: [latency / incidents / manual ops overhead — numbers]
- Post-migration benefit: [specific metric improvement]
- Risk if we don't act: [specific system fragility or compliance exposure]

Implementation: [X sprints], [Y engineers], [zero production impact during migration]

Alternative considered: [Option B] — rejected because [one sentence].

Decision needed by: [date] to hit [business milestone].
```

---

### Template 4 — Stakeholder Escalation Response

When an MD or trading desk head escalates directly to you:
```
"Thank you for flagging this directly.

Here's where we are: [current status — one sentence].
Here's what's being done: [action — one sentence].
Here's when you'll hear from me next: [specific time].

I have this."
```

The last line matters. "I have this" is not arrogance — it is the confidence signal that stops an MD from cascading the escalation upward before you've had a chance to resolve it.

---

## Audience Calibration Matrix

| Audience | Technical Depth | Frame | Length |
|---|---|---|---|
| Trading Desk Head | Zero — business impact only | Revenue / risk | 3 sentences max |
| Managing Director | Minimal — outcome + cost | Commercial value | 1 short paragraph |
| Peer Tech Manager | Moderate — system boundaries | Dependencies + timeline | Half page max |
| Your Team | Full technical depth | Correctness + velocity | As needed |
| Compliance / Risk | Process-focused | Audit trail, controls | Formal memo format |

---

## The Caution Trap in Technical Communication

Your Hogan profile will push you toward:
- **Over-qualifying status:** "We believe we may have identified a potential root cause..."
- **Burying the business impact:** Three paragraphs of technical explanation before "trading desk position feed was delayed by 12 minutes"
- **Soft ownership language:** "There appears to have been an issue" vs. "My team's service failed at 14:32"
- **Delaying the first communication** until you have certainty — by which time the desk has already escalated

**The Grove Override:** Communicate before you are certain. An acknowledged "investigating" message at minute 3 is worth more than a precise post-mortem at minute 45. Stakeholders tolerate uncertainty. They cannot tolerate silence.

---

## Weekly Experiments

1. **This week:** Take your last project status email or Slack update. Rewrite it with BLUF — headline in sentence 1, business impact before any technical context. Compare. Send the BLUF version next time.
2. **This week:** Define your P1 communication SLA with your team: first message within 3 minutes, updates every 10 minutes, resolution message within 30 minutes. Put it in your on-call runbook.
3. **This week:** Identify the last time you delivered a technical message to a senior stakeholder. Count the sentences before you reached the business impact. Set a personal rule: business impact in sentence 1, always.

---

*Next: [Pillar 10 — Executive Presence](./10-executive-presence-selling-the-team.md) | [Back to README](./README.md)*
