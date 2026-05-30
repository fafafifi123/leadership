# Pillar 14 — Hiring for Equities Technology
## Screening, Selling, and Closing A-Player Equities Engineers

**Great Leader Anchor:** Steve Jobs (Apple) — relentless talent density, the founder selling the dream
**Hogan Filter:** Your caution default is to over-screen for the absence of red flags rather than the presence of exceptional signal — hiring the "safe, no-objections" candidate over the high-ceiling one. On a 5-person squad, one safe-but-mediocre hire caps your entire team's density for years. Caution in hiring is the most expensive caution of all.

---

## The Core Framework: The 4-Signal Hire

For equities tech specifically, screen for four signals — not just coding ability.

```
SIGNAL 1 — ENGINEERING DEPTH (table stakes)
  Can they actually build it? Data structures, concurrency, systems design.
  Necessary but NOT sufficient. Every candidate clears this or they're out fast.

SIGNAL 2 — PRODUCTION JUDGMENT (the differentiator)
  Have they owned something that broke at 3am with money on the line?
  Do they think in blast radius, rollback, and reversibility?
  This is what separates equities engineers from generic devs.

SIGNAL 3 — PRESSURE COMPOSURE (equities-critical)
  How do they reason when the market is moving against them?
  Can they make a 60%-confidence call without freezing?

SIGNAL 4 — COMMERCIAL CURIOSITY (the multiplier)
  Do they care WHY the desk needs the feature, or just WHAT to build?
  Engineers who understand PnL build better systems.
```

---

## Steve Jobs — A-Players Hire A-Players; B-Players Hire C-Players

Jobs's iron law: **"A-players want to work with A-players. The moment you tolerate a B-player, they hire C-players to feel comfortable, and your density collapses."** He personally interviewed thousands of hires because talent density was the whole game.

For your squad of 5, the math is brutal and clarifying:
- Every hire moves your team density by **20%**.
- A wrong hire isn't a 1/5 problem — it's a drag on the other four (review load, on-call gaps, morale).
- **The default answer is NO.** Only an enthusiastic yes from multiple signals is a hire. A "probably fine" is a no.

---

## Equities-Specific Interview Questions

### Probing Signal 2 — Production Judgment
```
"Tell me about the worst production incident you've personally owned.
Walk me through the first 10 minutes. What did you do BEFORE you understood
the root cause?"

GREEN FLAGS: stabilize first, communicate early, reversible mitigation,
             RCA after resolution.
RED FLAGS:   froze to find perfect root cause, didn't communicate,
             no rollback instinct, blamed others.
```

### Probing Signal 3 — Pressure Composure
```
"You've deployed a change. Fills start looking wrong. The desk is pinging you.
Your monitoring is ambiguous — could be your change, could be upstream data.
You have about 90 seconds before the desk escalates. What do you do?"

GREEN FLAGS: rolls back the reversible change first, communicates a holding
             message, investigates in parallel.
RED FLAGS:   wants to "check a few things first," goes silent, freezes on
             ambiguity.
```

### Probing Signal 4 — Commercial Curiosity
```
"The last feature you built — who used it, and what business outcome did it
drive? How would you know if it was actually valuable?"

GREEN FLAGS: knows the user, knows the metric, curious about impact.
RED FLAGS:   "I just built what the ticket said." No idea who used it.
```

---

## The Scorecard (Kill the "Nice Person" Bias)

Force structured, independent scoring. Your caution will otherwise default to "no strong objections = hire."

```
| Signal | Weight | Score (1-4) | Evidence |
|---|---|---|---|
| Engineering Depth | Gate | _ | Must be ≥3 or auto-reject |
| Production Judgment | 35% | _ | Specific incident story |
| Pressure Composure | 30% | _ | Behavior under the 90-sec scenario |
| Commercial Curiosity | 20% | _ | Did they know their feature's impact? |
| Team Multiplier | 15% | _ | Will A-players want to work with them? |

DECISION RULE: Any single score of 1 = no hire. Average must be ≥3.0.
"On the fence" = no. Ambivalence is the data.
```

---

## Selling the 5-Person Team Against FAANG

Your caution undersells. You list what the role *is* defensively rather than selling the *dream* Jobs-style. A great hire is a sale, and you are the closer.

```
THE PITCH (what a 5-person equities squad beats FAANG at):

1. PROXIMITY TO IMPACT: "Your code touches live PnL the day it ships. At
   [BigCo] you'd wait 6 months to see a feature flag flip for 0.1% of users."

2. OWNERSHIP SURFACE: "You own a whole system, not a 200th of one. Your
   blast radius is real — that's terrifying and it's how you grow fastest."

3. THE ROOM: "You'll be in the room with the trading desk and the MD. Most
   engineers your level never get that commercial exposure."

4. THE TEAM: "We're 5 people, all senior-caliber. No carrying dead weight,
   no politics layers. Just high-density engineering."

CLOSE: "I'm not looking for someone to fill a seat. I'm looking for someone
who makes the other four better. I think that's you — here's why..."
```

---

## The Caution Trap in Hiring

Your Hogan profile will push you toward:
- **Over-screening for safety** — the no-red-flags candidate over the high-ceiling one
- **Slow processes** — losing A-players to faster-moving firms while you "gather more signal"
- **Consensus-to-no** — letting one lukewarm interviewer veto a strong candidate via your own conflict-avoidance
- **Underselling** — describing the job instead of selling the mission
- **Settling under headcount pressure** — hiring a B to stop the on-call bleeding (this compounds the problem)

**The Jobs Override:** The default is no — but when you find an A-player, move with total urgency and sell like a founder. Speed and conviction win A-players. A slow, hedged process signals a slow, hedged team — and the best candidates read that instantly.

---

## Weekly Experiments

1. **This week:** Write your team's scorecard with the 4 signals weighted for your actual systems. Use it on your next interview — score independently *before* the debrief discussion.
2. **This week:** Draft your 60-second "why this team beats FAANG" pitch. Practice it out loud. You should be able to deliver it with genuine conviction, not a feature list.
3. **This week:** Audit your current interview loop's speed. Time from application to offer. If it's over 2 weeks, identify the bottleneck — it's almost certainly costing you A-players, and it's probably caution-driven.
