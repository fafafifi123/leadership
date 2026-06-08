# Pillar 16 — Cross-Team Dependency Management
## Eliminating Lateral Blockers in a Bank Org Without Creating Political Enemies

**Layer:** Business | **Great Leader Anchor:** Nelson Mandela | **Related:** [Pillar 05](./05-managing-up-influence-negotiation.md) · [Pillar 11](./11-strategic-decisiveness-under-uncertainty.md)

**Hogan Filter — Your Caution Trap:** You wait passively on other teams — the infra team that owes you prod access, the market-data team with the undocumented API, the risk-systems team in a release freeze. You log the dependency, mark yourself "blocked," and absorb the delay rather than aggressively driving resolution, because pushing feels like creating conflict. In a bank, your biggest delivery risks are almost always *lateral*, not internal — and passivity here is invisible self-sabotage.

**Anti-Caution Directive:** A dependency is not someone else's deliverable you wait for. It is a risk you actively manage. Pre-set your escalation trigger dates. Drive proactively. The other team's slip becomes your missed commitment to the desk — and you own that outcome regardless of where the work sits.

---

## In 60 Seconds

Mandela negotiated the end of apartheid with no army and no formal power over the other side. His method: understand the other party's interests so deeply that you can frame your ask as serving *their* goals, not just yours. You have zero authority over the infra team or the market-data team. So you cannot command — you must align. When your ask serves their metric, you stop being a nuisance and become an ally.

---

## The Core Framework: Dependency Operating Model

```
1. MAP        Identify every external dependency on your critical path, early.
2. RATE       Score each: (likelihood of slipping) × (impact if it does)
3. OWN        Assign a named owner on YOUR side for each dependency.
4. PULL       Drive resolution proactively. Never wait to be unblocked.
5. ESCALATE   Have a pre-agreed escalation path BEFORE you need it.
```

---

## Mandela — Alignment Without Authority

For every lateral dependency, frame your ask around *their* metric:

| Their Team | What THEY Are Measured On | How to Frame YOUR Ask |
|---|---|---|
| Infra | Stability, ticket SLAs, no unplanned work | "This prevents a P1 that would page YOUR on-call too" |
| Market Data | Feed reliability, schema governance | "Documenting this API reduces YOUR support tickets" |
| Risk Systems | Audit, control, zero compliance gaps | "My change improves YOUR audit trail completeness" |
| Other Eng Teams | Their own roadmap velocity | "This is reusable — it unblocks your Q3 item too" |

When your ask serves their metric, you stop being a nuisance and become an ally. That is the Mandela move.

---

## The Dependency Register (Make Lateral Risk Visible)

```
| Dependency | Their Owner | Your Owner | Need-By | Risk | Status | Escalation Trigger |
|---|---|---|---|---|---|---|
| Prod access for routing svc | Infra (Sam) | You | Sprint 14 | HIGH | At risk | If not granted by D-3, escalate to infra lead |
| Pricing API docs | Mkt Data (Lee) | Eng A | Sprint 13 | MED | On track | If undocumented by D-2, request live walkthrough |
| Compliance sign-off | Risk (Jo) | You | Sprint 15 | HIGH | Not started | If no slot by D-5, escalate to your MD |
```

**The Escalation Trigger column is the anti-caution mechanism.** It pre-decides *when* you stop waiting and act — removing the in-the-moment hesitation your derailer produces.

---

## The Escalation Ladder (Pre-Agreed, Not Emotional)

Reframe escalation as *transparency*, pre-negotiated and unemotional. Not aggression — risk management.

```
RUNG 1 — Peer to peer (engineer ↔ engineer)
  Direct, specific. "I need X by Friday or my desk feature slips by 5 days."

RUNG 2 — Manager to manager (you ↔ their lead)
  "Flagging early: my Sprint 14 desk commitment depends on your team's X.
   Can we align on a date so neither of us gets surprised?"

RUNG 3 — Shared stakeholder (your MD / their MD)
  "Two teams, one dependency, a date risk to a desk commitment. I want
   visibility on this before it becomes a missed deliverable."

RULE: Escalate EARLY and CALMLY, not late and hot. An escalation at D-5
is risk management. An escalation at D-0 is a fire drill — and reflects
on your planning, not just theirs.
```

---

## Proactive Pull Tactics

| Tactic | How | Why It Beats Waiting |
|---|---|---|
| Offer to do the work | "I'll write the PR against your API, you just review" | You control the timeline; removes their effort |
| Co-own the artifact | Pair on the schema doc together, live | No async ping-pong delay |
| Standing dependency sync | 15-min weekly with key dependent teams | Surfaces slips before they're critical |
| Make their ask easy | Pre-fill their ticket template, give exact specs | Lower friction = faster turnaround |
| Bank goodwill first | Help them on something before you need them | Reciprocity when you call it in |

---

## The Caution Trap in Dependency Management

Your Hogan profile will push you toward:
- **Passive blocking** — marking a task "blocked" and waiting instead of driving
- **Late escalation** — hoping it resolves itself until it's a crisis
- **Conflict-avoidance** — not pushing because it feels confrontational
- **Absorbing the slip** — quietly missing your own commitment rather than surfacing the lateral cause
- **No pre-agreed triggers** — re-deciding whether to escalate emotionally every time

**The Mandela Override:** You have no authority over these teams, so build alignment instead. Frame every ask around their metrics. Pre-set escalation triggers so you act on schedule, not on nerve. Driving a lateral dependency hard is not creating conflict — it is protecting a commitment to the desk, and that is leadership the business sees.

---

## Weekly Experiments

1. **This week:** Build your dependency register for the current sprint. For every external dependency, add a pre-set escalation trigger date. The act of writing the trigger removes in-the-moment hesitation.
2. **This week:** Pick your highest-risk dependency. Identify the other team's metric and reframe your ask to serve it. Send that reframed ask today. Notice the difference in response.
3. **This week:** Find one dependency where you can use a pull tactic — offer to write the PR, co-author the doc, or pre-fill their ticket. Remove their friction instead of waiting in their queue.

---

*Next: [Pillar 17 — Regulatory Navigation](./17-regulatory-compliance-navigation.md) | [Back to README](./README.md)*
