---
name: pfc-mkt-content-ideation
description: Generates 20 ranked video ideas from the channel brief, scoring each by audience pain severity, search demand signal, and Kano category. Filters out Indifferent/Reverse content before it wastes production time.
argument-hint: "[channel-brief file]"
user-invocable: true
allowed-tools: "Read,Grep,Glob,Write,Bash(gh *)"
---

# PFC-MKT-CONTENT-IDEATION: Find the Problems Worth Solving

Generate a ranked bank of 20 video ideas built from validated audience problems — not guesswork. Each idea is scored, categorised, and ready for title/thumbnail work.

## Dtree Classification

`SKILL_STANDALONE` — Low autonomy (structured ideation workflow), no orchestration, single-concern.

## Prerequisites

- Channel Brief from `pfc-mkt-channel-blueprint` (Skill 1)

## What You Do

When the user invokes `/azlan-github-workflow:pfc-mkt-content-ideation`, follow these 4 sections in order.

---

### Section 1: Problem Extraction

Read the channel brief. For the ideal viewer profile, generate 10 specific problems they face.

For each problem:

| Field | Description |
|-------|-------------|
| `problem` | One-sentence problem statement |
| `painIfIgnored` | What happens if they don't solve it (emotional hook) |
| `gainIfSolved` | What they achieve if they do solve it (promise/benefit) |
| `searchSignal` | Would someone search YouTube for this at 11pm? (Yes/Maybe/No) |

Ask the creator to validate, add, or remove problems. Their lived experience beats generated ideas.

**Quality Gate G1 — Problem Validation:**
- [ ] 10 problems listed
- [ ] Creator has confirmed or edited each one
- [ ] At least 7 have "Yes" search signal

---

### Section 2: Idea Generation

For each validated problem, generate 2 video idea angles (20 total).

For each idea:

| Field | Description |
|-------|-------------|
| `workingTitle` | Draft title (will be refined in Skill 3) |
| `hookAngle` | The emotional or curiosity trigger |
| `format` | Tutorial / Story / Breakdown / Comparison / Behind-the-scenes |
| `estimatedLength` | Short (5-8 min) / Medium (8-15 min) / Long (15-25 min) |

**Quality Gate G2 — Idea Diversity:**
- [ ] 20 ideas generated
- [ ] At least 3 different formats represented
- [ ] No two ideas solve the exact same problem the same way

---

### Section 3: Kano Filter

Classify each idea using simplified Kano categories:

| Category | Keep? | Description |
|----------|-------|-------------|
| **Must-Make** | Yes | Core educational content solving a validated problem |
| **Performance** | Yes | Deep-dives — more depth = more satisfaction |
| **Attractive** | Yes — prioritise | Behind-the-scenes, contrarian takes, exclusive insight — drives sharing |
| **Indifferent** | Drop | Generic listicle anyone could make |
| **Reverse** | Drop | Promotional or clickbait — harms trust |

Remove any idea classified as Indifferent or Reverse. If fewer than 15 remain, generate replacements.

**Quality Gate G3 — Kano Pass:**
- [ ] All remaining ideas are Must-Make, Performance, or Attractive
- [ ] At least 3 ideas are Attractive category (these drive initial growth)
- [ ] Zero Indifferent/Reverse ideas remain

---

### Section 4: Rank and Output

Rank the surviving ideas by priority:

| Rank Factor | Weight |
|-------------|--------|
| Search signal strength | 40% |
| Kano category (Attractive > Performance > Must-Make for early growth) | 30% |
| Creator confidence ("I could film this today") | 30% |

Output the ranked list as a markdown file:

```markdown
# Content Idea Bank — [Creator Name]

## Priority Queue (Top 5 — Film First)
| # | Title | Hook | Format | Kano | Search |
|---|-------|------|--------|------|--------|

## Backlog (Next 10)
| # | Title | Hook | Format | Kano | Search |
|---|-------|------|--------|------|--------|

## Parked (Low Priority)
| # | Title | Hook | Format | Kano | Search |
|---|-------|------|--------|------|--------|
```

Write to user's preferred location (default: `content-idea-bank-v1.md`).

**Quality Gate G4 — Bank Completeness:**
- [ ] 15-20 ranked ideas
- [ ] Top 5 are actionable this week
- [ ] Each idea has title, hook, format, and Kano category

---

### Section 5: Downstream Handoff

> Your idea bank is ready. Take your top 5 ideas to Skill 3 (Title & Thumbnail) — run `/azlan-github-workflow:pfc-mkt-title-thumbnail` to craft scroll-stopping titles for each.

---

## Output Artefacts

| Artefact | Format | Purpose |
|----------|--------|---------|
| Content Idea Bank | Markdown | Ranked, filtered idea backlog for ongoing content production |
