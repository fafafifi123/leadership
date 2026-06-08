# Pillar 14 — Hiring for Equities Technology
## Screening, Selling, and Closing A-Player Equities Engineers

**Layer:** Trajectory | **Great Leader Anchor:** Steve Jobs (Apple) | **Related:** [Pillar 04](./04-talent-density-stack-ranking.md) · [Pillar 18](./18-career-trajectory-personal-brand.md)

**Hogan Filter — Your Caution Trap:** You over-screen for the absence of red flags rather than the presence of exceptional signal — hiring the "safe, no-objections" candidate over the high-ceiling one. On a 5-person squad, one safe-but-mediocre hire caps your entire team's density for years. You also under-sell during the process because selling feels like over-promising. Caution in hiring is the most expensive caution of all.

**Anti-Caution Directive:** The default answer is no — but when you find an A-player, move with total urgency and sell like a founder. Speed and conviction win A-players. A slow, hedged process signals a slow, hedged team — and the best candidates read that instantly.

---

## In 60 Seconds

Jobs's law: A-players want to work with A-players. The moment you tolerate a B-player who doesn't improve, they hire C-players to feel comfortable, and density collapses. For a 5-person trading technology team, every hire moves your density by 20%. A wrong hire isn't a 1/5 problem — it is a drag on the other four in review load, on-call gaps, and morale. The default is no. Only an enthusiastic yes from multiple signals is a hire.

---

## The Core Framework: 4-Signal Hire

```
SIGNAL 1 — ENGINEERING DEPTH (table stakes)
  Can they actually build it? Data structures, concurrency, systems design.
  Necessary but NOT sufficient. Clear this gate fast, then move on.

SIGNAL 2 — PRODUCTION JUDGMENT (the differentiator)
  Have they owned something that broke at 3am with money on the line?
  Do they think in blast radius, rollback, and reversibility?
  This separates equities engineers from generic developers.

SIGNAL 3 — PRESSURE COMPOSURE (equities-critical)
  How do they reason when the market is moving against them?
  Can they make a 60%-confidence call without freezing?

SIGNAL 4 — COMMERCIAL CURIOSITY (the multiplier)
  Do they care WHY the desk needs the feature, or just WHAT to build?
  Engineers who understand PnL build better systems.
```

---

## Equities-Specific Interview Questions

### Probing Signal 2 — Production Judgment
```
"Tell me about the worst production incident you've personally owned.
Walk me through the first 10 minutes. What did you do BEFORE you understood
the root cause?"

GREEN FLAGS: stabilize first, communicate early, reversible mitigation
             executed, RCA followed resolution.
RED FLAGS:   froze to find perfect root cause, went silent, no rollback
             instinct, blamed others or upstream systems.
```

### Probing Signal 3 — Pressure Composure
```
"You've deployed a change. Fills start looking wrong. The trading desk is
pinging you. Your monitoring is ambiguous — could be your change, could be
upstream data. You have about 90 seconds before the desk escalates.
What do you do?"

GREEN FLAGS: rolls back the reversible change first, sends a holding
             message to the desk, investigates in parallel.
RED FLAGS:   wants to "check a few things first," goes silent under
             ambiguity, waits for certainty before acting.
```

### Probing Signal 4 — Commercial Curiosity
```
"The last feature you built — who used it, and what business outcome did
it drive? How would you know if it was actually valuable?"

GREEN FLAGS: knows the user persona, knows the metric, curious about impact.
RED FLAGS:   "I just built what the ticket said." No idea who used it or why.
```

---

## The Structured Scorecard (Kill the "Nice Person" Bias)

Force independent scoring before the debrief. Your caution will otherwise default to "no strong objections = hire."

```
| Signal | Weight | Score (1–4) | Evidence |
|---|---|---|---|
| Engineering Depth | Gate | _ | Must be ≥3 or auto-reject |
| Production Judgment | 35% | _ | Specific incident story |
| Pressure Composure | 30% | _ | Behavior under the 90-sec scenario |
| Commercial Curiosity | 20% | _ | Did they know their feature's impact? |
| Team Multiplier | 15% | _ | Will A-players want to work with them? |

DECISION RULE:
- Any single score of 1 = no hire
- Average must be ≥3.0
- "On the fence" = no. Ambivalence is the data.
```

---

## Selling the 5-Person Team Against FAANG

Your caution undersells. You list what the role *is* defensively rather than selling the *dream*. A great hire is a sale, and you are the closer.

```
THE PITCH — what a 5-person equities squad beats FAANG at:

1. PROXIMITY TO IMPACT
   "Your code touches live PnL the day it ships. At [BigCo] you'd wait 6
   months to see a feature flag flip for 0.1% of users."

2. OWNERSHIP SURFACE
   "You own a whole system, not a 200th of one. Your blast radius is real —
   that's terrifying and it's how you grow fastest."

3. THE ROOM
   "You'll be in the room with the trading desk and the MD. Most engineers
   your level never get that commercial exposure."

4. THE TEAM
   "We're 5 people, all senior-caliber. No carrying dead weight. No political
   layers. Just high-density engineering where everyone ships."

THE CLOSE:
"I'm not looking for someone to fill a seat. I'm looking for someone who
makes the other four better. I think that's you — here's why: [specific
signal you saw in the interview]. When can you start?"
```

---

## The Caution Trap in Hiring

Your Hogan profile will push you toward:
- **Over-screening for safety** — the no-red-flags candidate over the high-ceiling one
- **Slow processes** — losing A-players to faster-moving firms while you "gather more signal"
- **Consensus-to-no** — letting one lukewarm interviewer veto a strong candidate via conflict-avoidance
- **Underselling** — describing the job instead of selling the mission
- **Settling under pressure** — hiring a B to stop the on-call bleeding (this compounds the problem)

**The Jobs Override:** The default is no — but when you find an A-player, move with total urgency and sell like a founder. Speed and conviction win A-players. A slow, hedged process signals a slow, hedged team — the best candidates read that before they get to the offer stage.

---

## Weekly Experiments

1. **This week:** Write your team's scorecard with the 4 signals weighted for your actual systems and risk profile. Use it on your next interview — score independently *before* the debrief.
2. **This week:** Draft your 60-second "why this team beats FAANG" pitch. Practice it out loud. You should deliver it with genuine conviction, not a feature list.
3. **This week:** Audit your interview loop speed. Time from application to offer. If it's over 2 weeks for a strong candidate, identify the bottleneck — it is almost certainly costing you A-players.

---

*Next: [Pillar 15 — Blameless Post-Mortems](./15-blameless-postmortem-culture.md) | [Back to README](./README.md)*
