---
name: pfc-mkt-channel-blueprint
description: Builds a one-page channel brief from the creator's expertise, ideal viewer profile, competitive landscape, and unique differentiator. First skill in the Creator Authority pipeline — all downstream skills depend on this output.
argument-hint: "[your niche or expertise area]"
user-invocable: true
allowed-tools: "Read,Grep,Glob,Write,Bash(gh *)"
---

# PFC-MKT-CHANNEL-BLUEPRINT: Know Your Ground

Build a clear, one-page channel brief that defines who you are, who you serve, and what makes you different. This is the foundation — every other skill in the Creator Authority pipeline reads from this output.

## Dtree Classification

`SKILL_STANDALONE` — Low autonomy (structured worksheet workflow), no orchestration, single-concern.

## What You Do

When the user invokes `/azlan-github-workflow:pfc-mkt-channel-blueprint`, follow these 4 sections in order. Each section has a quality gate that MUST pass before proceeding.

---

### Section 1: Expertise Inventory

Ask the creator to identify their top 3 areas of expertise. These become **content pillars**.

For each area, capture:

| Field | Description |
|-------|-------------|
| `expertiseArea` | What you know deeply |
| `proofOfAuthority` | Why you're credible (experience, credentials, results) |
| `contentAngle` | How you'd teach this differently from others |

If the creator struggles, ask: *"What do people already come to you for advice on?"*

**Quality Gate G1 — Expertise Clarity:**
- [ ] 3 expertise areas identified
- [ ] Each has a proof of authority (not self-proclaimed — based on experience or results)
- [ ] Each has a distinct content angle

---

### Section 2: Ideal Viewer Profile

Build a specific profile of the one person this channel serves.

| Field | Description |
|-------|-------------|
| `jobTitle` | Their role (e.g., "Junior cloud engineer", "Career-switching data analyst") |
| `biggestStruggle` | The problem keeping them up at night |
| `desiredOutcome` | What success looks like for them in 6 months |
| `whereTheyHangOut` | Channels, communities, newsletters they already follow |
| `searchBehaviour` | What they type into YouTube at 11pm |

**Quality Gate G2 — Viewer Specificity:**
- [ ] Viewer profile is a specific person, not a demographic
- [ ] Struggle is concrete (not "wants to learn more")
- [ ] Desired outcome is measurable or observable

---

### Section 3: Competitive Landscape

Find 5 channels or newsletters already serving this viewer.

For each competitor:

| Field | Description |
|-------|-------------|
| `channelName` | Name + platform |
| `subscriberCount` | Approximate size |
| `contentStyle` | What they do well |
| `gap` | What they miss or get wrong |

**Quality Gate G3 — Competitive Awareness:**
- [ ] 5 competitors identified with real channels/newsletters
- [ ] At least 2 gaps identified that the creator can fill
- [ ] No competitor is doing exactly what the creator plans

---

### Section 4: Channel Brief Assembly

Assemble the one-page channel brief:

```markdown
# Channel Brief — [Creator Name]

## Who I Am
[1-2 sentences: expertise + proof of authority]

## Who I Serve
[Ideal viewer: job title, struggle, desired outcome]

## Content Pillars
1. [Pillar 1] — [angle]
2. [Pillar 2] — [angle]
3. [Pillar 3] — [angle]

## My Unfair Advantage
[What I can say that competitors can't — and why]

## Competitive Gaps I Fill
1. [Gap 1]
2. [Gap 2]

## Upload Schedule
[Frequency + day/time commitment]
```

Write to user's preferred location (default: `channel-brief-v1.md`).

**Quality Gate G4 — Brief Completeness:**
- [ ] All 6 sections populated
- [ ] Unfair advantage is specific and defensible
- [ ] Upload schedule is realistic given stated time commitment

---

### Section 5: Downstream Handoff

Confirm the brief is saved. Inform the user:

> Your channel brief is ready. This feeds into Skill 2 (Content Ideation) — run `/azlan-github-workflow:pfc-mkt-content-ideation` next to generate your first 20 video ideas from this brief.

---

## Output Artefacts

| Artefact | Format | Purpose |
|----------|--------|---------|
| Channel Brief | Markdown | Foundation doc — all downstream skills reference this |
