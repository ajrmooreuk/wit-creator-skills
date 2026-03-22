---
name: pfc-mkt-title-thumbnail
description: Crafts 3 scroll-stopping title variants and thumbnail concepts per video idea, applying CTR principles (curiosity, specificity, viewer language). Targets >8% CTR threshold.
argument-hint: "[content-idea-bank file]"
user-invocable: true
allowed-tools: "Read,Grep,Glob,Write"
---

# PFC-MKT-TITLE-THUMBNAIL: Titles & Thumbnails That Earn the Click

Craft titles that make scrolling past feel like a mistake, paired with thumbnail concepts that stop the scroll. Each video gets 3 variants to test.

## Dtree Classification

`SKILL_STANDALONE` — Low autonomy (structured creative workflow), no orchestration, single-concern.

## Prerequisites

- Content Idea Bank from `pfc-mkt-content-ideation` (Skill 2)

## What You Do

When the user invokes `/azlan-github-workflow:pfc-mkt-title-thumbnail`, follow these 3 sections in order.

---

### Section 1: Title Principles Check

Before generating titles, confirm the creator understands the 4 rules:

| Principle | Test |
|-----------|------|
| **Promise a specific result** | Does the title tell the viewer what they'll get? |
| **Trigger curiosity** | Does it create an open loop the viewer needs to close? |
| **Use viewer language** | Would the ideal viewer actually say these words? |
| **Under 60 characters** | Will it display fully on mobile? |

Anti-patterns to avoid:
- Jargon the viewer wouldn't search for
- Vague titles ("My Thoughts On...")
- ALL CAPS spam
- Misleading promises

**Quality Gate G1 — Principles Acknowledged:**
- [ ] Creator confirms understanding of 4 principles

---

### Section 2: Title & Thumbnail Generation

For each of the top 5 ideas from the Content Idea Bank, generate:

**3 Title Variants:**

| Variant | Style | Example Pattern |
|---------|-------|-----------------|
| A — Direct Promise | Result-focused | "How I [achieved X] in [timeframe] (Step-by-Step)" |
| B — Curiosity Gap | Open loop | "The [topic] Mistake That [consequence]" |
| C — Contrarian/Bold | Pattern interrupt | "Stop [common advice] — Do This Instead" |

**1 Thumbnail Concept per title variant:**

| Element | Specification |
|---------|---------------|
| `facialExpression` | One emotion: surprise, determination, frustration, joy |
| `textOverlay` | Max 3 words — the emotional punch |
| `visualElement` | One prop, background, or graphic that adds context |
| `colourContrast` | High contrast between text and background |

**Quality Gate G2 — Title Quality:**
- [ ] 15 titles total (3 per idea × 5 ideas)
- [ ] Every title is under 60 characters
- [ ] Every title passes at least 2 of the 4 principles
- [ ] No two titles for the same idea use the same style

---

### Section 3: Output Assembly

Output as a markdown file:

```markdown
# Title & Thumbnail Pack — [Creator Name]

## Video 1: [Idea from bank]

### Title Options
| Variant | Title | Style | Characters |
|---------|-------|-------|------------|
| A | ... | Direct Promise | XX |
| B | ... | Curiosity Gap | XX |
| C | ... | Contrarian | XX |

### Thumbnail Concepts
| Variant | Expression | Text Overlay | Visual | Contrast |
|---------|-----------|-------------|--------|----------|
| A | ... | ... | ... | ... |
| B | ... | ... | ... | ... |
| C | ... | ... | ... | ... |

[Repeat for Videos 2-5]
```

Write to user's preferred location (default: `title-thumbnail-pack-v1.md`).

**Quality Gate G3 — Pack Completeness:**
- [ ] 5 videos covered
- [ ] 3 variants each
- [ ] Thumbnail concept for every title

---

### Section 4: Downstream Handoff

> Your title pack is ready. Pick your favourite variant for Video 1 and take it to Skill 4 (Script Builder) — run `/azlan-github-workflow:pfc-mkt-script-builder` to write your first full script.

---

## Output Artefacts

| Artefact | Format | Purpose |
|----------|--------|---------|
| Title & Thumbnail Pack | Markdown | 15 title variants + thumbnail concepts for top 5 videos |
