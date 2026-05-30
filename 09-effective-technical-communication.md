# Pillar 09 — Effective Technical Communication
## Mastering BLUF for Outages, Delays, and Architectural Pivots

**Great Leader Anchor:** Andy Grove (Intel)
**Hogan Filter:** Your caution default is to front-load technical context before delivering the headline — explaining the system architecture, the edge cases considered, and the risk analysis before telling the stakeholder what actually happened or what you need. This pattern reads as defensive, not authoritative, and causes your audience to lose confidence before you reach the point.

---

## The Core Framework: BLUF (Bottom Line Up Front)

```
B — Bottom Line:   State the conclusion or status in sentence 1
L — Level:         Calibrate technical depth to audience knowledge
U — Urgency:       Make the time-sensitivity explicit, not implied
F — Follow-up:     State one clear next action or decision needed
```

Every outage communication, architectural proposal, and project delay message should clear this test: **"If the reader stops after sentence 2, do they have everything they need to act?"**

---

## Andy Grove's Communication Doctrine

Grove's principle from *High Output Management*: **"Noise in the communication channel is not the receiver's problem. It is the sender's problem. Your job is to reduce the noise."**

In equities technology, noise is:
- Unexplained acronyms and internal system names in stakeholder messages
- Passive voice that obscures ownership ("an issue was found" vs. "I found a bug in the feed handler")
- Probability hedging that delays the key message ("it could potentially impact..." vs. "it is impacting")
- Technical root cause explanation before the business impact statement

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

Status: [current state change, if any]
Diagnosis: [one sentence — what you believe the cause is]
Action: [what is being executed right now]
ETA to resolution: [specific time or "unknown — will update at [time]"]
```

**Resolution message:**
```
RESOLVED — [System Name] | [Time EST]

Duration: [X minutes]
Root cause: [one sentence — no technical jargon in this message]
Business impact: [confirmed impact — trades affected, data gaps, etc.]
Immediate fix: [what was done to restore service]
Full post-mortem: [date] — I'll circulate before EOD.
```

---

### Template 2 — Project Delay
**Wrong (Cautious Default):**
> "Due to a number of technical complexities we encountered during the integration phase, including some unexpected schema incompatibilities between the upstream pricing service and our downstream feed handler, which required us to revisit our data transformation layer, the delivery timeline may need to be adjusted..."

**Right (BLUF):**
```
[Feature/Project Name] — Timeline Update

Bottom line: We are 5 business days late. New delivery date: [specific date].

Reason: Upstream pricing service schema changed without notice on [date].
Retrofit required 3 days of unplanned rework.

Impact: [what this delays for the business — one sentence]
Mitigation: [what you're doing to compress remaining timeline]
Decision needed from you: [none / or specific ask]
```

---

### Template 3 — Architectural Change Proposal
```
Proposal: [Migration / Refactor / New System — one-line description]

Recommendation: Proceed with [Option A].

Business case:
- Current state costs: [latency / incidents / manual ops overhead]
- Post-migration benefit: [specific metric improvement]
- Risk if we don't act: [specific system fragility or compliance exposure]

Implementation: [X sprints], [Y engineers], [zero production impact during migration]

Alternative considered: [Option B] — rejected because [one sentence].

Decision needed by: [date] to hit [business milestone].
```

---

### Template 4 — Stakeholder Escalation Response
When an MD or trading desk head escalates directly:
```
"Thank you for flagging this directly.

Here's where we are: [current status — one sentence].
Here's what's being done: [action — one sentence].
Here's when you'll hear from me next: [specific time].

I have this."
```
The last line matters. It is not arrogance — it is the confidence signal that stops an MD from cascading the escalation upward.

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
- **Over-qualifying status updates:** "We believe we may have identified a potential root cause..."
- **Burying the business impact:** Three paragraphs of technical explanation before "trading desk position feed was delayed by 12 minutes"
- **Soft ownership language:** "There appears to have been an issue" vs. "My team's service failed at 14:32"
- **Delaying the first communication** until you have certainty — by which time the desk has already escalated

**The Grove Override:** Communicate before you are certain. An acknowledged "investigating" message sent at minute 3 is worth more than a precise post-mortem sent at minute 45. Stakeholders can tolerate uncertainty. They cannot tolerate silence.

---

## Weekly Experiments

1. **This week:** Take your last project status email or Slack update. Rewrite it with BLUF — headline in sentence 1, no technical context until paragraph 2. Compare the two. Send the BLUF version next time.
2. **This week:** Define your P1 communication SLA with your team: first message within 3 minutes, updates every 10 minutes, resolution message within 30 minutes. Put it in your team's on-call runbook.
3. **This week:** Identify the last time you delivered a technical message to a senior stakeholder. How many sentences before you reached the business impact? Set a personal rule: business impact in sentence 1, always.
