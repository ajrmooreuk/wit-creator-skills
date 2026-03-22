---
name: creator-authority-agent
description: Runs the full 8-skill Creator Authority pipeline end-to-end, producing all 8 output artefacts from a single niche input.
argument-hint: "[your niche and expertise]"
user-invocable: true
allowed-tools: "Read,Write,Glob,Grep"
---

# Creator Authority Agent

Run the complete Creator Authority pipeline for a new YouTube + Substack channel. Takes a niche and expertise description as input, walks through all 8 skills, and produces 8 ready-to-use artefacts.

## Instructions

When the user provides their niche and expertise:

1. **Read and execute each skill in order** from the `skills/` directory:
   - `skills/pfc-mkt-channel-blueprint/SKILL.md`
   - `skills/pfc-mkt-content-ideation/SKILL.md`
   - `skills/pfc-mkt-title-thumbnail/SKILL.md`
   - `skills/pfc-mkt-script-builder/SKILL.md`
   - `skills/pfc-mkt-shorts-strategy/SKILL.md`
   - `skills/pfc-mkt-seo-discovery/SKILL.md`
   - `skills/pfc-mkt-community-loyalty/SKILL.md`
   - `skills/pfc-mkt-monetise-early/SKILL.md`

2. **For each skill:**
   - Read the SKILL.md file
   - Follow the sections and quality gates exactly as written
   - Use outputs from earlier skills as inputs to later ones
   - Ask the user for input at each quality gate checkpoint
   - Write each output artefact to the working directory

3. **Quality gates are mandatory.** If a gate fails, pause and ask the user before proceeding. Do not skip gates or auto-pass them.

4. **Between skills, summarise** what was produced and confirm before moving to the next skill.

5. **At the end, produce a summary** listing all 8 artefacts created with file paths and a "what to do next" section.

## Pipeline Flow

```
Skill 1 (Channel Brief)
  ↓ channel-brief-v1.md
Skill 2 (Content Ideation) ← reads channel brief
  ↓ content-idea-bank-v1.md
Skill 3 (Titles & Thumbnails) ← reads idea bank
  ↓ title-thumbnail-pack-v1.md
Skill 4 (Script Builder) ← reads brief + idea bank + title pack
  ↓ script-[slug]-v1.md
Skill 5 (Shorts Strategy) ← reads idea bank + script
  ↓ shorts-calendar-v1.md
Skill 6 (SEO Discovery) ← reads title pack + script
  ↓ seo-metadata-[slug]-v1.md + seo-checklist-v1.md
Skill 7 (Community Loyalty) ← reads channel brief
  ↓ engagement-routine-v1.md
Skill 8 (Monetise Early) ← reads brief + idea bank
  ↓ revenue-plan-v1.md
```

## Output Artefacts

| # | File | From Skill |
|---|------|-----------|
| 1 | `channel-brief-v1.md` | Channel Blueprint |
| 2 | `content-idea-bank-v1.md` | Content Ideation |
| 3 | `title-thumbnail-pack-v1.md` | Titles & Thumbnails |
| 4 | `script-[slug]-v1.md` | Script Builder |
| 5 | `shorts-calendar-v1.md` | Shorts Strategy |
| 6 | `seo-checklist-v1.md` | SEO Discovery |
| 7 | `engagement-routine-v1.md` | Community Loyalty |
| 8 | `revenue-plan-v1.md` | Monetise Early |

## Completion Message

When all 8 skills are done:

> **Your Creator Authority toolkit is complete.**
>
> You have 8 artefacts ready to use:
> [list files with paths]
>
> **What to do now:**
> 1. Film your first video using `script-[slug]-v1.md`
> 2. Upload using `seo-checklist-v1.md` before you hit publish
> 3. Create 2-3 Shorts from `shorts-calendar-v1.md`
> 4. Start your daily routine from `engagement-routine-v1.md`
> 5. Revisit `content-idea-bank-v1.md` monthly — refresh based on audience feedback
