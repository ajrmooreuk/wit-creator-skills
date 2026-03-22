---
name: pfc-mkt-monetise-early
description: Builds a personal revenue plan with break-even analysis, 6 revenue streams ranked by readiness, and a monetisation timeline that generates income before hitting 10K subscribers.
argument-hint: "[channel-brief file]"
user-invocable: true
allowed-tools: "Read,Grep,Glob,Write"
---

# PFC-MKT-MONETISE-EARLY: Make Money Before 10K

Build a revenue plan that doesn't wait for subscriber milestones. This skill quantifies your costs, maps 6 revenue streams to your current stage, and produces a personal break-even target.

## Dtree Classification

`SKILL_STANDALONE` — Low autonomy (structured financial planning), no orchestration, single-concern.

## Prerequisites

- Channel Brief from `pfc-mkt-channel-blueprint` (Skill 1) — for niche and audience profile
- Content Idea Bank from `pfc-mkt-content-ideation` (Skill 2) — for content volume planning

## What You Do

When the user invokes `/azlan-github-workflow:pfc-mkt-monetise-early`, follow these 4 sections in order.

---

### Section 1: Cost Baseline

Capture the creator's actual investment:

| Cost Item | Monthly | Notes |
|-----------|---------|-------|
| Time investment (hours/week × 4) | ___ hrs | Creator's most valuable resource |
| Editing software | £___ | Free options exist (DaVinci Resolve, CapCut) |
| Scheduling/SEO tools | £___ | Optional — many free tiers available |
| Hosting (Substack is free to start) | £___ | Only if using paid tools |
| Equipment (amortised monthly) | £___ | Phone camera is fine to start |
| **Total monthly cost** | **£___** | |

Ask the creator: *"What's your hourly rate in your day job?"* — this sets the opportunity cost of content creation time.

**Quality Gate G1 — Costs Captured:**
- [ ] All cost items filled (£0 is valid — acknowledge free alternatives)
- [ ] Time investment is realistic (not "I'll do 40 hours a week")
- [ ] Opportunity cost acknowledged

---

### Section 2: Revenue Stream Mapping

Map 6 revenue streams to the creator's current stage:

| Stream | When to Start | Prerequisites | Realistic Monthly Range |
|--------|---------------|---------------|------------------------|
| **Affiliate links** | Video 1 | Relevant products/services to recommend | £50–500 |
| **Digital product** | After 10 videos | Template, guide, checklist, or mini-course | £10–50 per sale |
| **Consulting/coaching** | When DMs ask for help | Expertise + availability | £50–200/hour |
| **Substack paid tier** | 100+ free subscribers | Consistent newsletter value established | £5–15 × paid subscriber count |
| **Brand deals** | 500+ subscribers, high engagement | Media kit + niche authority | £100–1,000 per video |
| **AdSense** | 1,000 subs + 4,000 watch hours | YouTube Partner Programme threshold | £100–500/month |

For each stream, assess with the creator:
- **Ready now?** Can you activate this today?
- **Ready soon?** What milestone triggers this? (subscriber count, video count, engagement level)
- **Not yet?** What needs to happen first?

**Quality Gate G2 — Streams Assessed:**
- [ ] All 6 streams reviewed
- [ ] At least 2 streams marked "Ready now" or "Ready soon"
- [ ] Each stream has a realistic monthly estimate for THIS creator's niche

---

### Section 3: Break-Even & Revenue Plan

Build the personal financial model:

**Break-even calculation:**
```
Monthly costs (Section 1): £___
First revenue target: cover costs
Break-even point: Month ___ (based on growth trajectory and stream activation)
```

**6-month revenue projection (3 scenarios):**

| Month | Pessimistic | Base | Optimistic |
|-------|-------------|------|------------|
| 1 | £___ | £___ | £___ |
| 2 | £___ | £___ | £___ |
| 3 | £___ | £___ | £___ |
| 4 | £___ | £___ | £___ |
| 5 | £___ | £___ | £___ |
| 6 | £___ | £___ | £___ |

**Assumptions (must be explicit):**

| Assumption | Value | Confidence |
|------------|-------|------------|
| Videos per month | ___ | High (creator controls this) |
| Subscriber growth rate | ___% WoW | Medium (depends on content-market fit) |
| Conversion rate (viewer → subscriber) | ___% | Low (needs PMF validation) |
| Affiliate click-through rate | ___% | Low (niche-dependent) |

**Quality Gate G3 — Model Complete:**
- [ ] Break-even month identified
- [ ] 3 scenarios calculated (pessimistic, base, optimistic)
- [ ] All assumptions are explicit and labelled with confidence level
- [ ] Revenue targets are realistic (not fantasy numbers)

---

### Section 4: Revenue Plan Output

```markdown
# Revenue Plan — [Creator Name]

## Monthly Costs
| Item | Monthly |
|------|---------|
[from Section 1]

**Total: £___/month**

## Revenue Streams (Activation Order)
1. [First stream to activate] — Target: £___/month by Month ___
2. [Second stream] — Target: £___/month by Month ___
3. [Third stream] — Target: £___/month by Month ___

## Break-Even Target
**Month ___** — when revenue ≥ £___/month (total costs)

## 6-Month Projection
[Table from Section 3]

## Key Assumptions
[Table from Section 3]

## Revenue Milestones
- [ ] First £1 earned (any stream)
- [ ] First digital product sale
- [ ] First paid Substack subscriber
- [ ] Monthly revenue covers tool costs
- [ ] Monthly revenue covers full costs (break-even)
- [ ] Monthly revenue exceeds £500

## Monthly Review
Track actual vs. projected on the 1st of each month. If below pessimistic scenario for 2 consecutive months, revisit content-market fit (Skill 2) before investing more in monetisation.
```

Write to user's preferred location (default: `revenue-plan-v1.md`).

**Quality Gate G4 — Plan Actionable:**
- [ ] First revenue stream can be activated this week
- [ ] Break-even target is specific (month + amount)
- [ ] Monthly review cadence built in
- [ ] Fallback plan if projections miss (revisit content-market fit)

---

### Section 5: Pipeline Complete

> Revenue plan ready. You now have the complete Creator Authority toolkit:
>
> 1. Channel Blueprint ✓
> 2. Content Idea Bank ✓
> 3. Title & Thumbnail Pack ✓
> 4. Video Scripts ✓
> 5. Shorts Calendar ✓
> 6. SEO Checklist ✓
> 7. Engagement Routine ✓
> 8. Revenue Plan ✓
>
> Start filming. Revisit Skill 2 every month to refresh your idea bank based on what your audience is telling you.

---

## Output Artefacts

| Artefact | Format | Purpose |
|----------|--------|---------|
| Revenue Plan | Markdown | Personal financial model with break-even, projections, and milestones |
