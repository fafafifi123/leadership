# Pillar 16 — Cross-Team Dependency Management
## Eliminating Lateral Blockers in a Bank Org Without Creating Political Enemies

**Great Leader Anchor:** Nelson Mandela — building alignment across parties with no formal authority over each other
**Hogan Filter:** Your caution default is to wait passively on other teams — the infra team that owes you prod access, the market-data team with the undocumented API, the risk-systems team in a release freeze. You log the dependency, mark yourself "blocked," and absorb the delay rather than aggressively driving resolution, because pushing feels like creating conflict. In a bank, your biggest delivery risks are almost always *lateral*, not internal — and passivity here is invisible self-sabotage.

---

## The Core Framework: The Dependency Operating Model

```
1. MAP        — Identify every external dependency on your critical path, early.
2. RATE       — Score each: likelihood of slipping × impact if it does.
3. OWN        — Assign a single named owner on YOUR side for each dependency.
4. PULL       — Drive resolution proactively. Never wait to be unblocked.
5. ESCALATE   — Have a pre-agreed escalation path BEFORE you need it.
```

The mindset shift: **a dependency is not someone else's deliverable you wait for. It is a risk you actively manage.** The other team's slip becomes your missed commitment to the desk. You own the outcome regardless of where the work sits.

---

## Mandela — Alignment Without Authority

Mandela negotiated the end of apartheid with no army and no formal power over the other side. His method: **understand the other party's interests so deeply that you can frame your ask as serving *their* goals, not just yours.**

You have zero authority over the infra team or the market-data team. So you cannot command — you must align. For every dependency:

```
| Their Team | What THEY Are Measured On | How to Frame YOUR Ask |
|---|---|---|
| Infra | Stability, ticket SLAs, no unplanned work | "This prevents a P1 that would page YOUR on-call too" |
| Market Data | Feed reliability, schema governance | "Documenting this API reduces YOUR support tickets" |
| Risk Systems | Audit, control, zero compliance gaps | "My change improves YOUR audit trail completeness" |
| Other Eng Teams | Their own roadmap velocity | "This is reusable — it unblocks your Q3 item too" |
```

When your ask serves their metric, you stop being a nuisance and become an ally. That is the Mandela move: their win is the path to your win.

---

## The Dependency Register (Make Lateral Risk Visible)

Cautious leaders track dependencies in their head and hope. Make it a living artifact that forces proactive action — and gives you cover when something slips.

```
| Dependency | Owner (theirs) | Owner (yours) | Need-By | Risk | Status | Escalation Trigger |
|---|---|---|---|---|---|---|
| Prod access for routing svc | Infra (Sam) | You | Sprint 14 | HIGH | At risk | If not granted by D-3, escalate to infra lead |
| Pricing API docs | Mkt Data (Lee) | Eng A | Sprint 13 | MED | On track | If undocumented by D-2, request live walkthrough |
| Compliance sign-off | Risk (Jo) | You | Sprint 15 | HIGH | Not started | If no slot by D-5, escalate to your MD |
```

The **Escalation Trigger column is the anti-caution mechanism.** It pre-decides *when* you stop waiting and act — removing the in-the-moment hesitation your derailer produces.

---

## The Escalation Ladder (Pre-Agreed, Not Emotional)

Your caution makes escalation feel like aggression. Reframe it as *transparency*, pre-negotiated and unemotional.

```
RUNG 1 — Peer to peer (engineer ↔ engineer)
  Direct, friendly, specific. "I need X by Friday or my desk feature slips."

RUNG 2 — Manager to manager (you ↔ their lead)
  "Flagging early: my Sprint 14 desk commitment depends on your team's X.
   Can we align on a date so neither of us gets surprised?"

RUNG 3 — Shared stakeholder (your MD / their MD)
  "Two teams, one dependency, a date risk to a desk commitment. I want
   visibility on this before it becomes a missed deliverable."

RULE: Escalate EARLY and CALMLY, not late and hot. An escalation at D-5 is
risk management. An escalation at D-0 is a fire drill — and reads as failure.
```

---

## The Proactive Pull Tactics

| Tactic | How | Why It Beats Waiting |
|---|---|---|
| Offer to do the work | "I'll write the PR against your API, you just review" | Removes their effort; you control the timeline |
| Co-own the artifact | Pair on the schema doc together, live | No async ping-pong delay |
| Standing dependency sync | 15-min weekly with key dependent teams | Surfaces slips before they're critical |
| Make their ask easy | Pre-fill their ticket template, give exact specs | Lower friction = faster turnaround |
| Bank goodwill first | Help them on something before you need them | Reciprocity when you call in the favor |

---

## The Caution Trap in Dependency Management

Your Hogan profile will push you toward:
- **Passive blocking** — marking a task "blocked" and waiting instead of driving
- **Late escalation** — hoping it resolves itself until it's a crisis
- **Conflict-avoidance** — not pushing because it feels confrontational
- **Absorbing the slip** — quietly missing your own commitment rather than surfacing the lateral cause
- **No pre-agreed triggers** — re-deciding whether to escalate emotionally, every time

**The Mandela Override:** You have no authority over these teams, so build alignment instead. Frame every ask around *their* metrics. Make dependencies visible with pre-set escalation triggers so you act on schedule, not on nerve. Driving a lateral dependency hard is not creating conflict — it's protecting a commitment to the desk, and that's leadership the business sees.

---

## Weekly Experiments

1. **This week:** Build your dependency register for the current sprint. For every external dependency, add a pre-set escalation trigger date. The act of writing the trigger removes the in-the-moment hesitation.
2. **This week:** Pick your highest-risk dependency. Identify the *other team's* metric, and reframe your ask to serve it. Send that reframed ask. Notice the difference in response.
3. **This week:** Find one dependency where you can use a "pull" tactic — offer to write the PR, co-author the doc, or pre-fill their ticket. Remove their friction instead of waiting on their queue.
