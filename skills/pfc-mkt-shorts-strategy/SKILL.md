---
name: pfc-mkt-shorts-strategy
description: Designs a Shorts content calendar mapped to long-form videos, prioritising Kano Attractive content for discovery. System produces 2-3 Shorts per long-form video targeting completion rate optimisation.
argument-hint: "[content calendar or script file]"
user-invocable: true
allowed-tools: "Read,Grep,Glob,Write"
---

# PFC-MKT-SHORTS-STRATEGY: Shorts — Your Discovery Engine

Build a Shorts content system that brings new viewers to your long-form channel. Every Short is a funnel — not a standalone piece.

## Dtree Classification

`SKILL_STANDALONE` — Low autonomy (structured planning workflow), no orchestration, single-concern.

## Prerequisites

- Content Idea Bank from `pfc-mkt-content-ideation` (Skill 2)
- At least one script from `pfc-mkt-script-builder` (Skill 4) — Shorts candidates section

## What You Do

When the user invokes `/azlan-github-workflow:pfc-mkt-shorts-strategy`, follow these 3 sections in order.

---

### Section 1: Shorts Rules Check

Confirm the creator understands the Shorts format constraints:

| Rule | Why |
|------|-----|
| 30-45 seconds maximum | Completion rate is the primary algorithm signal |
| One idea per Short | Clarity beats density — one takeaway only |
| Hook in first 2 seconds | "The biggest mistake in [topic]..." |
| End with channel reference | "Full breakdown on my channel" — drives long-form views |
| Vertical format (9:16) | Mobile-first — this is how Shorts are consumed |

Anti-patterns:
- Shorts that require context from the long-form video
- Multi-point lists (save those for long-form)
- Shorts longer than 50 seconds (completion rate drops)

**Quality Gate G1 — Format Understanding:**
- [ ] Creator confirms Shorts constraints
- [ ] Creator has vertical filming capability (phone is fine)

---

### Section 2: Shorts Calendar Generation

For each published or planned long-form video, generate 2-3 Shorts:

| Shorts Type | Source | Example |
|-------------|--------|---------|
| **Best Moment** | Strongest 30 seconds from the script | The "aha" insight that makes viewers want the full version |
| **Contrarian Hook** | Bold claim from the video, no resolution | "Stop doing [common advice]..." — resolution is in the long-form |
| **Quick Win** | One actionable tip from the Solution block | A self-contained micro-tutorial that proves your expertise |

For each Short:

| Field | Description |
|-------|-------------|
| `parentVideo` | Which long-form video it maps to |
| `type` | Best Moment / Contrarian Hook / Quick Win |
| `openingLine` | The first 2-second hook |
| `closingLine` | Channel reference CTA |
| `estimatedLength` | Target seconds |
| `publishDay` | Offset from long-form publish date |

**Publishing cadence:**
- Long-form video: Tuesday (or creator's chosen day)
- Short 1: Same day as long-form (boost initial views)
- Short 2: Thursday (maintain mid-week visibility)
- Short 3: Saturday (weekend discovery peak)

**Quality Gate G2 — Calendar Quality:**
- [ ] 2-3 Shorts per long-form video
- [ ] Each Short has an opening hook line
- [ ] Publishing spread across the week (not all on one day)
- [ ] Each Short maps to a parent video

---

### Section 3: Output

Generate a 4-week Shorts calendar:

```markdown
# Shorts Calendar — [Creator Name]

## Week 1
| Day | Type | Parent Video | Opening Hook | Length |
|-----|------|-------------|-------------|--------|

## Week 2
[...]

## Week 3
[...]

## Week 4
[...]

## Repurposing System
For every new long-form video:
1. Extract the "aha moment" → Best Moment Short
2. Pull the boldest claim → Contrarian Hook Short
3. Isolate one quick tip → Quick Win Short
```

Write to user's preferred location (default: `shorts-calendar-v1.md`).

**Quality Gate G3 — Calendar Completeness:**
- [ ] 4 weeks populated
- [ ] 8-12 Shorts total
- [ ] Each mapped to a parent long-form video
- [ ] Repurposing system documented for ongoing use

---

### Section 4: Downstream Handoff

> Shorts calendar ready. Run `/azlan-github-workflow:pfc-mkt-seo-discovery` next to optimise your upload metadata for both long-form and Shorts.

---

## Output Artefacts

| Artefact | Format | Purpose |
|----------|--------|---------|
| Shorts Calendar | Markdown | 4-week publishing schedule mapped to long-form content |
