---
name: pfc-mkt-community-loyalty
description: Builds a daily 15-minute and weekly 30-minute engagement routine that drives YouTube algorithm signals, grows collaborations, and feeds audience insights back into the content ideation loop.
argument-hint: "[channel-brief file]"
user-invocable: true
allowed-tools: "Read,Grep,Glob,Write"
---

# PFC-MKT-COMMUNITY-LOYALTY: Build Your Community — 15 Minutes a Day

Build a loyal audience that watches everything and shares without being asked. This skill creates a sustainable engagement routine — not a grind.

## Dtree Classification

`SKILL_STANDALONE` — Low autonomy (structured routine design), no orchestration, single-concern.

## Prerequisites

- Channel Brief from `pfc-mkt-channel-blueprint` (Skill 1) — for ideal viewer and competitor list

## What You Do

When the user invokes `/azlan-github-workflow:pfc-mkt-community-loyalty`, follow these 3 sections in order.

---

### Section 1: Daily Routine Design (15 minutes)

Build a 3-block daily routine:

**Block 1 — Reply (5 minutes)**

| Action | Why |
|--------|-----|
| Reply to every new comment on your latest video | YouTube treats replies as engagement signals — boosts the video in recommendations |
| Ask a follow-up question in at least one reply | Drives multi-turn conversations — stronger signal than a single reply |
| Heart/like every comment | Acknowledges the viewer — costs nothing, builds loyalty |

**Block 2 — Outreach (5 minutes)**

| Action | Why |
|--------|-----|
| Leave 3 thoughtful comments on channels your audience also watches | Gets your name and face in front of the right viewers |
| Comments must add value (insight, experience, question) — not "great video!" | Value comments get pinned and liked — spam comments get ignored |
| Rotate between the 5 competitors from your Channel Brief | Consistent presence in the same communities builds recognition |

**Block 3 — Signal (5 minutes)**

| Action | Why |
|--------|-----|
| Share one useful thought on Substack Notes, LinkedIn, or X | Stays visible between uploads — reminds your audience you exist |
| Repurpose: a key insight from your latest video or a response to a viewer comment | No new content creation needed — recycle what you've already made |

**Quality Gate G1 — Routine Practicality:**
- [ ] Total daily time is 15 minutes (not more)
- [ ] Each block has a specific, repeatable action
- [ ] No block requires creating new content from scratch

---

### Section 2: Weekly Routine Design (30 minutes)

**Weekly Block 1 — Collaborate (15 minutes)**

| Action | Why |
|--------|-----|
| DM one creator in your niche for a potential collab | Collaborations are the single fastest subscriber growth lever for small channels |
| Template: "Hey [name], loved your video on [topic]. I'm working on [related topic] — would you be up for [specific collab idea]?" | Specific > vague. Reference their work. Propose something concrete. |
| Track outreach in a simple list (Name / Date / Response) | Follow up after 1 week if no response — once only, then move on |

**Weekly Block 2 — Listen (15 minutes)**

| Action | Why |
|--------|-----|
| Ask your audience what they want next (poll, comment question, or newsletter question) | Content they asked for always outperforms content you guessed |
| Review comments from the past week for recurring themes | Patterns in comments = validated content ideas → feed back to Skill 2 |
| Check YouTube Analytics → Audience tab → When your viewers are online | Optimise publish time based on real data, not assumptions |

**Quality Gate G2 — Weekly Routine Practicality:**
- [ ] Total weekly time is 30 minutes (not more)
- [ ] Collaboration outreach has a template and tracking system
- [ ] Audience listening has a clear output (ideas fed back to content ideation)

---

### Section 3: Output

Generate the engagement routine document:

```markdown
# Community Engagement Routine — [Creator Name]

## Daily (15 min — do this every day you upload or the day after)

### Block 1: Reply (5 min)
- [ ] Reply to all new comments on latest video
- [ ] Ask a follow-up question in at least 1 reply
- [ ] Heart/like every comment

### Block 2: Outreach (5 min)
- [ ] Leave 3 value-adding comments on competitor channels:
  1. [Channel from brief]
  2. [Channel from brief]
  3. [Channel from brief — rotate weekly]

### Block 3: Signal (5 min)
- [ ] Share 1 insight on [preferred platform]
- [ ] Source: latest video key point OR viewer comment response

## Weekly (30 min — pick a consistent day)

### Collaborate (15 min)
- [ ] DM 1 creator: [template]
- [ ] Update outreach tracker

### Listen (15 min)
- [ ] Review week's comments for recurring themes
- [ ] Post audience poll or question
- [ ] Check Analytics → Audience → best publish time
- [ ] Feed insights back to Content Idea Bank

## Outreach Tracker
| Creator | Date Sent | Collab Idea | Response | Follow-Up |
|---------|----------|-------------|----------|-----------|
```

Write to user's preferred location (default: `engagement-routine-v1.md`).

**Quality Gate G3 — Routine Complete:**
- [ ] Daily routine fits in 15 minutes
- [ ] Weekly routine fits in 30 minutes
- [ ] Outreach tracker template included
- [ ] Feedback loop to Content Idea Bank documented

---

### Section 4: Downstream Handoff

> Engagement routine set. Run `/azlan-github-workflow:pfc-mkt-monetise-early` to build your revenue plan — the final skill in the pipeline.

---

## Output Artefacts

| Artefact | Format | Purpose |
|----------|--------|---------|
| Engagement Routine | Markdown | Daily + weekly checklist with outreach tracker |
