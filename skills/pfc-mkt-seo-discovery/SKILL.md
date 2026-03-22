---
name: pfc-mkt-seo-discovery
description: Optimises video title, description, tags, and chapter markers for YouTube and Google discoverability. Includes a reusable pre-upload SEO checklist targeting top-10 search ranking for niche terms.
argument-hint: "[video title and topic]"
user-invocable: true
allowed-tools: "Read,Grep,Glob,Write"
---

# PFC-MKT-SEO-DISCOVERY: Get Found — Simple SEO

Make every video searchable. This skill produces optimised metadata and a reusable checklist you run before every upload.

## Dtree Classification

`SKILL_STANDALONE` — Low autonomy (structured optimisation workflow), no orchestration, single-concern.

## Prerequisites

- Video title from `pfc-mkt-title-thumbnail` (Skill 3)
- Script from `pfc-mkt-script-builder` (Skill 4) — for chapter timestamps

## What You Do

When the user invokes `/azlan-github-workflow:pfc-mkt-seo-discovery`, follow these 4 sections in order.

---

### Section 1: Keyword Research

For the video topic, identify:

| Field | Description |
|-------|-------------|
| `primaryKeyword` | The exact phrase the ideal viewer would type into YouTube search |
| `secondaryKeywords` | 3-5 variations and related terms |
| `longTailPhrases` | 2-3 question-format searches ("how to...", "why does...", "best way to...") |
| `competitorGap` | Terms competitors rank for but don't cover well |

**Demand Validation Test:**
Search the primary keyword on YouTube. Check:
- 3+ results with similar titles → demand confirmed
- 0 results → nobody's searching for this — rethink the keyword
- 100+ results from big channels → too competitive for a new creator — add a modifier to narrow

**Quality Gate G1 — Keyword Validation:**
- [ ] Primary keyword has confirmed search demand
- [ ] 3-5 secondary keywords identified
- [ ] Competition level is manageable for the creator's current size

---

### Section 2: Metadata Optimisation

Generate optimised metadata for the video:

**Title** (already from Skill 3, now SEO-refined):
- Primary keyword in the first half of the title
- Under 60 characters
- Still passes curiosity/promise test from Skill 3

**Description** (structured template):
```
[Line 1-2: What this video solves — include primary keyword naturally]

[Line 3: Newsletter CTA with link]

[Timestamps/Chapters:]
0:00 — Hook
0:15 — [Problem section title]
1:00 — [Solution step 1]
...

[Links section:]
Newsletter: [link]
Related videos: [links]

[Tags section — invisible to viewers but helps search:]
#keyword1 #keyword2 #keyword3
```

**Tags** (5-8):
- Primary keyword
- 2-3 secondary keywords
- Channel name
- Niche identifier
- 1 broad category tag

**Chapters** (from script timestamps):
- Timestamp every major section
- Use descriptive labels (not "Part 1", "Part 2")
- First chapter must be `0:00`

**Quality Gate G2 — Metadata Complete:**
- [ ] Title contains primary keyword
- [ ] Description first 2 lines include keyword naturally
- [ ] 5-8 tags, no duplicates
- [ ] Chapters match script structure

---

### Section 3: SEO Checklist

Generate a reusable pre-upload checklist:

```markdown
# Pre-Upload SEO Checklist

## Before Upload
- [ ] Primary keyword identified and demand-validated
- [ ] Title under 60 characters with keyword in first half
- [ ] Thumbnail saved (from Skill 3 concepts)

## During Upload
- [ ] Description: first 2 lines state what video solves
- [ ] Description: newsletter link included
- [ ] Description: timestamps/chapters added
- [ ] Tags: 5-8 tags including primary keyword and channel name
- [ ] Category: set to most relevant YouTube category
- [ ] Playlist: added to relevant playlist (create one if needed)

## After Upload
- [ ] Pinned comment: question related to video topic
- [ ] Community post or Substack Note announcing the video
- [ ] Shorts from this video scheduled (from Skill 5 calendar)

## Weekly SEO Check
- [ ] Review Analytics → Traffic sources → YouTube search
- [ ] Note which keywords are driving views
- [ ] Update future video ideas based on search data
```

Write to user's preferred location (default: `seo-checklist-v1.md`).

**Quality Gate G3 — Checklist Usable:**
- [ ] Checklist is practical (can be completed in 5 minutes)
- [ ] All items are actionable (not vague)

---

### Section 4: Output & Downstream Handoff

Write optimised metadata to `seo-metadata-[video-slug]-v1.md`.

> Metadata optimised. Run `/azlan-github-workflow:pfc-mkt-community-loyalty` to set up your daily engagement routine, or `/azlan-github-workflow:pfc-mkt-monetise-early` to build your revenue plan.

---

## Output Artefacts

| Artefact | Format | Purpose |
|----------|--------|---------|
| SEO Metadata | Markdown | Optimised title, description, tags, chapters per video |
| SEO Checklist | Markdown | Reusable pre-upload checklist for every video |
