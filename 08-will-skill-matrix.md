# Pillar 08 — Will / Skill Matrix for Engineers
## Diagnosing and Coaching Across All 4 Performance Quadrants

**Great Leader Anchor:** Satya Nadella (Microsoft)
**Hogan Filter:** Your caution default is to avoid the hard diagnostic — labeling an engineer's quadrant feels like a judgment call with insufficient data. This creates a situation where the burned-out senior engineer drifts toward disengagement and the motivated junior engineer plateaus because they are not getting the stretch assignments that their will demands.

---

## The Core Framework: 2×2 Will/Skill Matrix

```
              HIGH SKILL
                  │
   STAR           │    EXPERT (BURNED OUT)
   High Will      │    Low Will / High Skill
   High Skill     │
   (Stretch &     │    (Re-engage or reassign)
    Retain)       │
──────────────────┼──────────────────────────
   DIAMOND        │    DEADWEIGHT
   High Will      │    Low Will / Low Skill
   Low Skill      │
   (Invest &      │    (PIP or exit)
    Accelerate)   │
                  │
              LOW SKILL
     LOW WILL ◄────────────────────────► HIGH WILL
```

---

## Quadrant-by-Quadrant Coaching Blueprint

### Quadrant 1 — STAR (High Will + High Skill)
**Profile:** Owns complex systems, ships reliably, proactively unblocks others. Wants more.

**Risk:** If not stretched, this engineer leaves. Your best engineers are always interviewing.

**Coaching Actions:**
- Assign technical leadership on the highest-visibility project this quarter
- Give them a business stakeholder to own (e.g., they present directly to the trading desk)
- Create a succession path: "Here is what Staff Engineer looks like at this firm — let's build toward it"
- Protect their time ruthlessly from low-complexity tickets that erode engagement

**Script:**
```
"I want to be transparent with you: you're operating above your current title.
I'm building a case for your promotion. In the next 6 months, I need you to
deliver [specific high-visibility outcome] and demonstrate [specific leadership
behavior — e.g., mentoring a junior engineer through a production deployment].

I'm giving you [project/system] as the vehicle for that. I'm in your corner.
What do you need from me to make this happen?"
```

---

### Quadrant 2 — EXPERT / BURNED OUT (Low Will + High Skill)
**Profile:** Deep technical expertise, institutional knowledge. Increasingly withdrawn, resistant to new approaches, skipping team rituals.

**Risk:** This is your highest-knowledge flight risk. If they leave, they take irreplaceable system context. If they stay disengaged, they poison team culture.

**Coaching Actions:**
- Diagnose the source of will erosion: boredom, org friction, personal life, compensation, lack of recognition?
- Do NOT increase accountability pressure first — it will accelerate exit
- Offer a domain pivot: "Is there a different problem in this space that would re-engage you?"
- Consider a temporary architectural advisory role — leverage their knowledge in a less operational way

**Script:**
```
"I want to have a direct conversation. Your technical ability is not the question —
you're one of the strongest engineers I've managed. What I'm observing is
[specific behavioral signal: e.g., disengagement in sprint reviews, slower
response to tickets, shorter PR reviews].

I'm not here to pressure you. I want to understand: what's changed?
And separately — is there a technical problem in this domain that you're
not getting to work on that would re-energize you?"
```

---

### Quadrant 3 — DIAMOND (High Will + Low Skill)
**Profile:** Motivated, asks questions, takes initiative, shows up. But ships bugs, under-scopes complexity, and needs constant direction.

**Risk:** If under-invested, this engineer's will erodes (moves to Quadrant 2 or 4). If over-assigned, they cause production incidents from over-confidence.

**Coaching Actions:**
- Create structured stretch assignments with guardrails: "Own this ticket end-to-end, but run your approach past [senior engineer] before coding"
- Pair them explicitly with a Star — not for mentorship theater, but for genuine transfer
- Build a 90-day skill acceleration plan with concrete milestones
- Give them early wins on contained, lower-risk work to build technical confidence

**Script:**
```
"Your drive is exactly what this team needs. Here's my honest assessment:
your technical foundation is developing, and I want to invest in accelerating that.

Here's the plan: for the next 90 days, you own [specific system/domain].
Your benchmark is [specific measurable outcome — e.g., zero bug escapes on
your tickets, PR merge rate ≥1/day, unassisted runbook execution on [system]].
[Senior engineer] is your technical resource — not your checker, your resource.

At 90 days, I'll tell you exactly where you've landed."
```

---

### Quadrant 4 — DEADWEIGHT (Low Will + Low Skill)
**Profile:** Missing commitments, not improving, disengaged from feedback, impact on team morale visible to peers.

**Risk:** Every day this engineer remains without a formal improvement plan signals to your Stars and Diamonds that underperformance has no consequence.

**Coaching Actions:**
- Do not run an informal improvement conversation for the fourth time. Formalize it.
- Initiate PIP: specific targets, specific timeline, specific consequence
- Pre-brief HR and your MD before the conversation
- Do not protect this engineer from their own performance data — show them the numbers

**Script:** See Pillar 04 — PIP Initiation Script.

---

## Satya Nadella's Growth Mindset Application

Nadella transformed Microsoft by replacing the **"know-it-all"** culture (where admitting a skill gap was career-damaging) with a **"learn-it-all"** culture (where developing skill is the expectation at every level).

For your team, this means:
- Quadrant 3 engineers should never feel embarrassed about being in Quadrant 3
- The question is not "why don't you know this?" but "what is the fastest path to you knowing this?"
- Every engineer should be able to articulate where they are in the matrix and what their next move is

**The anti-Nadella failure mode:** Treating the matrix as a permanent label rather than a current-state snapshot. Engineers move. Your job is to accelerate that movement.

---

## Quarterly Calibration — 5-Person Team

```markdown
| Engineer | Will (1-5) | Skill (1-5) | Quadrant | Current Trajectory | Primary Action |
|---|---|---|---|---|---|
| [Name] | 5 | 5 | STAR | Upward | Stretch + promote path |
| [Name] | 4 | 4 | STAR | Stable | Retain + commercial exposure |
| [Name] | 5 | 3 | DIAMOND | Upward | 90-day acceleration plan |
| [Name] | 2 | 4 | EXPERT | Declining | Re-engagement conversation |
| [Name] | 2 | 2 | DEADWEIGHT | Flat | Formal PIP initiation |
```

---

## Weekly Experiments

1. **This week:** Place each of your 5 engineers in a quadrant based on current-state observation. Identify the one engineer whose quadrant you have been avoiding naming. Name it. Write the coaching action.
2. **This week:** For your burned-out expert (if you have one): schedule a 30-minute exploratory conversation — not a performance conversation. Ask about the technical problem they wish they were working on. Listen.
3. **This week:** For your highest-will engineer: find one assignment that is above their current comfort zone. Give it to them with explicit permission to fail and debrief — not as a test, but as a development investment.
