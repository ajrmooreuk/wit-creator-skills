---
name: pfc-mkt-script-builder
description: Writes a complete video script using Hook-Problem-Solution-Proof-Ask structure. Targets >50% average view duration by frontloading value and maintaining momentum throughout.
argument-hint: "[video title and topic]"
user-invocable: true
allowed-tools: "Read,Grep,Glob,Write"
---

# PFC-MKT-SCRIPT-BUILDER: Script It — Hook, Help, Ask

Write a complete, ready-to-film video script structured to keep viewers watching. Every script follows the same proven pattern: Hook → Problem → Solution → Proof → Ask.

## Dtree Classification

`SKILL_STANDALONE` — Low autonomy (structured template workflow), no orchestration, single-concern.

## Prerequisites

- Channel Brief from `pfc-mkt-channel-blueprint` (Skill 1)
- Selected video idea and title from Skills 2-3

## What You Do

When the user invokes `/azlan-github-workflow:pfc-mkt-script-builder`, follow these 5 sections in order.

---

### Section 1: Script Inputs

Gather from the user or read from existing artefacts:

| Input | Source |
|-------|--------|
| Video title | Title & Thumbnail Pack (Skill 3) |
| Target problem | Content Idea Bank (Skill 2) |
| Ideal viewer | Channel Brief (Skill 1) |
| Target length | Short (5-8 min) / Medium (8-15 min) / Long (15-25 min) |

**Quality Gate G1 — Inputs Complete:**
- [ ] Title confirmed
- [ ] Problem clearly stated
- [ ] Target length chosen
- [ ] Ideal viewer profile available

---

### Section 2: Script Structure

Generate the script in 5 blocks:

**BLOCK 1 — HOOK (0-15 seconds)**
- Pattern interrupt: say something unexpected or counterintuitive
- Establish stakes: why should the viewer care RIGHT NOW?
- Preview the payoff: what will they have by the end?

Template:
> "Here's what nobody tells you about [problem]... [unexpected claim]. By the end of this video, you'll [specific outcome]."

**BLOCK 2 — PROBLEM (15-60 seconds)**
- Name the pain with specificity — make them feel seen
- Use a scenario the ideal viewer has actually experienced
- Bridge to the solution: "Here's why this keeps happening..."

Template:
> "If you've ever [specific scenario], you're not alone. The reason this happens is [root cause]. And once you understand that, the fix is straightforward."

**BLOCK 3 — SOLUTION (bulk of video)**
- Break into 3-5 clear, numbered steps
- Each step: state it → explain it → show an example
- Keep momentum: "Now that you've got [step N], here's where it gets interesting..."

**BLOCK 4 — PROOF (30 seconds)**
- Show it works: personal result, data point, or viewer testimonial
- Be specific: numbers, dates, outcomes

**BLOCK 5 — ASK (15 seconds)**
- ONE call to action only (subscribe, comment, or newsletter)
- Tie the CTA to the value just delivered
- Never beg — position it as a next step for them

Template:
> "If this helped, subscribe — I put out a new video every [day]. And if you want the deeper version, I break this down step-by-step in my newsletter — link in the description."

**Quality Gate G2 — Structure Complete:**
- [ ] All 5 blocks present
- [ ] Hook is under 15 seconds when read aloud
- [ ] Solution has 3-5 distinct steps
- [ ] Only ONE CTA in the Ask block

---

### Section 3: Script Draft

Write the complete script as conversational text (not bullet points). The creator should be able to read it directly to camera or use it as a detailed outline.

Include:
- **Timestamps** for each block (estimated)
- **[B-ROLL]** markers where supporting visuals would help
- **[SCREEN]** markers for screen-share or graphic moments
- **[EMPHASIS]** markers for key phrases to stress

**Quality Gate G3 — Script Quality:**
- [ ] Reads naturally when spoken aloud (no written-English formality)
- [ ] Every step in the Solution block has an example
- [ ] Total estimated runtime matches target length (±20%)

---

### Section 4: Shorts Extraction

Identify 2-3 moments in the script that work as standalone Shorts:

| Moment | Timestamp | Why It Works as a Short |
|--------|-----------|------------------------|
| ... | ... | Self-contained insight in <45 seconds |

These feed into Skill 5 (Shorts Strategy).

---

### Section 5: Output

Write the script to user's preferred location (default: `script-[video-slug]-v1.md`).

**Quality Gate G4 — Output Completeness:**
- [ ] Full script saved
- [ ] Timestamps included
- [ ] Shorts moments identified
- [ ] CTA aligned to newsletter or subscribe

---

### Section 6: Downstream Handoff

> Script ready. Film it. After you've published, run `/azlan-github-workflow:pfc-mkt-shorts-strategy` to build your Shorts calendar, or `/azlan-github-workflow:pfc-mkt-seo-discovery` to optimise your upload metadata.

---

## Output Artefacts

| Artefact | Format | Purpose |
|----------|--------|---------|
| Video Script | Markdown | Complete script with timestamps, B-roll/screen markers |
| Shorts Candidates | Table in script | 2-3 moments pre-identified for Shorts extraction |
