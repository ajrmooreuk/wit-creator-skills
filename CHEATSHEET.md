# Creator Authority Skills — Cheatsheet

**How to use this skill chain + deploy as a standalone agent**

---

## QUICK START (5 minutes)

### 1. Install

```bash
# Clone the skills
git clone https://github.com/ajrmooreuk/wit-creator-skills.git

# Or unzip from the download
unzip wit-creator-skills-v1.0.0.zip
```

### 2. Tell Claude Code where to find them

Add this to your project's `CLAUDE.md` (or `~/.claude/CLAUDE.md` for global):

```markdown
## Custom Skills

Creator Authority Toolkit skills are at: /path/to/wit-creator-skills/skills/

Available skills (run in order):
1. /wit-creator-skills:pfc-mkt-channel-blueprint
2. /wit-creator-skills:pfc-mkt-content-ideation
3. /wit-creator-skills:pfc-mkt-title-thumbnail
4. /wit-creator-skills:pfc-mkt-script-builder
5. /wit-creator-skills:pfc-mkt-shorts-strategy
6. /wit-creator-skills:pfc-mkt-seo-discovery
7. /wit-creator-skills:pfc-mkt-community-loyalty
8. /wit-creator-skills:pfc-mkt-monetise-early
```

### 3. Run Skill 1

Open Claude Code and type:

```
Read the skill at /path/to/wit-creator-skills/skills/pfc-mkt-channel-blueprint/SKILL.md and run it. My niche is Women in Tech.
```

---

## WORKED EXAMPLE: Women in Tech YouTube Channel

Here's exactly what each skill produces, step by step.

---

### SKILL 1: Know Your Ground

**You say:**
> Run the channel blueprint skill. I'm a senior cloud engineer who mentors junior women in tech. I want to start a YouTube channel about breaking into cloud/DevOps roles.

**Claude walks you through:**
- Your 3 expertise areas (cloud certs, interview prep, career switching)
- Your ideal viewer (junior woman, 6 months into first tech role, struggling with imposter syndrome)
- 5 competitor channels (TechWithLucy, CloudGuru, etc.)
- Your unfair advantage (you've mentored 40+ women through career transitions — real stories, not theory)

**You get:** `channel-brief-v1.md`

**Then Claude says:** *"Run Skill 2 next."*

---

### SKILL 2: Find Problems Worth Solving

**You say:**
> Run the content ideation skill using my channel brief.

**Claude walks you through:**
- 10 problems your viewer faces ("Nobody will hire me without experience", "I don't know which cert to start with", "I freeze in technical interviews")
- 20 video ideas with hooks and formats
- Kano filter — kills the generic "Top 10 Cloud Tools" idea (Indifferent), keeps "How I Failed 3 Interviews Before Landing My Dream Role" (Attractive)
- Ranked priority queue

**You get:** `content-idea-bank-v1.md`

**Your top 5 ideas might look like:**

| # | Title | Hook | Category |
|---|-------|------|----------|
| 1 | "I Failed 3 Cloud Interviews — Here's What Finally Worked" | Personal story + specific fix | Attractive |
| 2 | "The Only Cloud Cert You Need in 2026 (Stop Wasting Money)" | Contrarian — challenges the "collect all certs" advice | Attractive |
| 3 | "AWS vs Azure vs GCP — Which One Gets You Hired Fastest?" | Comparison with real hiring data | Performance |
| 4 | "Your First 90 Days as a Cloud Engineer (Week by Week Plan)" | Specific result + actionable | Must-Make |
| 5 | "The Interview Question That Trips Up 90% of Junior Devs" | Curiosity gap + high search demand | Attractive |

---

### SKILL 3: Titles & Thumbnails

**You say:**
> Run the title thumbnail skill on my top 5 ideas.

**Claude generates 3 variants per idea. For Idea #1:**

| Variant | Title | Style |
|---------|-------|-------|
| A | "I Failed 3 Cloud Interviews — Here's What Finally Worked" | Direct Promise |
| B | "Why Junior Cloud Engineers Keep Failing Interviews" | Curiosity Gap |
| C | "Stop Prepping for Cloud Interviews Like This" | Contrarian |

**Thumbnail concept for Variant A:**
- Face: determination (slight smile, eyebrows up)
- Text overlay: "3 FAILS"
- Visual: laptop with rejection emails blurred in background

**You get:** `title-thumbnail-pack-v1.md`

---

### SKILL 4: Script It

**You say:**
> Script my first video — "I Failed 3 Cloud Interviews — Here's What Finally Worked". Target: 10 minutes.

**Claude writes a full script:**

```
[0:00] HOOK
"I failed three cloud engineering interviews in a row. The third one,
I literally went blank when they asked me to explain a VPC. But six
weeks later, I got an offer from a company I didn't even think would
call me back. Here's exactly what changed."

[0:15] PROBLEM
"If you're prepping for cloud interviews right now, you're probably
doing what I did — grinding LeetCode, memorising service names, and
watching 4-hour YouTube courses at 2x speed. And then you walk into
the interview and they ask you to DESIGN something, and your brain
just... stops."

[1:00] SOLUTION
Step 1: Stop memorising, start building
[explains with real example — a mini-project she built]
[B-ROLL: screen recording of the project]

Step 2: The "explain it to your manager" test
[explains the technique]
[SCREEN: whiteboard diagram]

Step 3: Mock interviews with real feedback
[explains where to find practice partners]

[8:00] PROOF
"Using exactly this approach, I went from 0/3 to getting offers from
two companies in the same week. And 12 of the women I've mentored
have used the same system."

[9:00] ASK
"If you're prepping for cloud interviews right now, subscribe — I put
out a new video every Tuesday. And I break down the exact mock interview
framework step by step in my newsletter — link in the description."
```

**Shorts candidates identified:**
1. The "VPC blank" story (0:00–0:15) — pattern interrupt
2. Step 2: "explain it to your manager" technique — quick win
3. "0/3 to two offers" result — proof clip

**You get:** `script-cloud-interview-fails-v1.md`

---

### SKILL 5: Shorts Strategy

**You say:**
> Build my Shorts calendar from my content plan.

**Claude generates a 4-week calendar:**

| Week | Tue (upload day) | Thu | Sat |
|------|-----------------|-----|-----|
| 1 | Long-form #1 + "I went blank on VPC" Short | "Explain it to your manager" Quick Win | "0/3 to 2 offers" Proof Short |
| 2 | Long-form #2 + Best Moment | Contrarian Hook | Quick Win |
| 3 | Long-form #3 + Best Moment | Contrarian Hook | Quick Win |
| 4 | Long-form #4 + Best Moment | Contrarian Hook | Quick Win |

**You get:** `shorts-calendar-v1.md`

---

### SKILL 6: SEO

**You say:**
> Optimise my first video for search.

**Claude produces:**

**Primary keyword:** "cloud interview preparation" (confirmed — 3+ results, manageable competition)

**Optimised description:**
```
Failed cloud engineering interviews? Here's the 3-step prep system
that took me from 0/3 to two offers in 6 weeks.

Join 500+ women in tech getting interview prep tips weekly:
[newsletter link]

Timestamps:
0:00 — I went blank on a VPC question
0:15 — Why traditional prep doesn't work
1:00 — Step 1: Stop memorising, start building
3:30 — Step 2: The "explain it to your manager" test
6:00 — Step 3: Mock interviews with real feedback
8:00 — Results: 0/3 → 2 offers
9:00 — Next steps

#cloudinterview #womenintech #devops
```

**You also get:** `seo-checklist-v1.md` — reusable for every future upload.

---

### SKILL 7: Community Routine

**You say:**
> Set up my daily engagement routine.

**Claude produces your personalised routine:**

**Daily (15 min):**
- Reply to all comments on latest video (5 min)
- Leave 3 thoughtful comments on: TechWithLucy, CloudGuru, ForrestKnight (5 min)
- Share one insight on LinkedIn (5 min)

**Weekly (30 min):**
- DM one creator for collab (this week: TechWithLucy — propose "Women in Cloud" joint video)
- Review comments for recurring questions → feed back into Idea Bank

**You get:** `engagement-routine-v1.md`

---

### SKILL 8: Revenue Plan

**You say:**
> Build my revenue plan.

**Claude walks you through:**

**Costs:** £0/month (phone camera, DaVinci Resolve free, Substack free)
**Opportunity cost:** 8 hrs/week × your hourly rate

**Revenue activation order:**
1. Affiliate links (Video 1) — recommend Cantrill courses, A Cloud Guru → £100/month by month 3
2. Digital product (Month 2) — "Cloud Interview Prep Checklist" PDF → £25 × 10 sales = £250
3. Coaching (Month 4) — £100/hour mock interviews → 2 sessions/week = £800/month

**Break-even:** Month 2 (costs are £0, so first affiliate sale = profit)
**6-month target:** £500–1,500/month (base scenario)

**You get:** `revenue-plan-v1.md`

---

## DEPLOY AS A STANDALONE AGENT

If you want to run the full 8-skill chain as an automated agent (not step-by-step), create this orchestrator file:

### `agent-creator-authority.md`

Save this in the same directory as the skills:

```markdown
---
name: creator-authority-agent
description: Runs the full 8-skill Creator Authority pipeline end-to-end, producing all 8 output artefacts from a single niche input.
argument-hint: "[your niche and expertise]"
user-invocable: true
allowed-tools: "Read,Write,Glob,Grep"
---

# Creator Authority Agent

Run the complete Creator Authority pipeline for a new YouTube + Substack channel.

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
   - Read the SKILL.md
   - Follow the sections and quality gates exactly
   - Use outputs from earlier skills as inputs to later ones
   - Write each output artefact to the working directory

3. **Quality gates are mandatory.** If a gate fails, pause and ask the user
   before proceeding.

4. **At the end, produce a summary** listing all 8 artefacts created with
   file paths.

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
```

### Run the agent:

```
Read and run the agent at /path/to/wit-creator-skills/agent-creator-authority.md

My niche: Women in Tech. I'm a senior cloud engineer who mentors
junior women through career transitions. I want to build a YouTube
channel and Substack newsletter about breaking into cloud/DevOps roles.
```

Claude will run all 8 skills end-to-end and produce all 8 artefacts in one session.

---

## SHARE VIA GOOGLE DOCS

The file `WIT-Creator-Authority-Skills-Complete-v1.0.0.md` is a single document containing all 8 skills as fillable worksheets. To share:

1. Open Google Docs → New Document
2. Paste the contents of `WIT-Creator-Authority-Skills-Complete-v1.0.0.md`
3. Format → Convert markdown (or just paste — tables render cleanly)
4. Share with your WIT Power Group

No Claude Code needed — the GDocs version works as a standalone workbook.

---

## FILE INVENTORY

```
wit-creator-skills/
├── README.md                                          ← Overview + install
├── CHEATSHEET.md                                      ← This file
├── manifest.json                                      ← Skill metadata
├── agent-creator-authority.md                         ← Full pipeline agent
├── WIT-Creator-Authority-Skills-Complete-v1.0.0.md    ← GDocs-friendly single doc
└── skills/
    ├── pfc-mkt-channel-blueprint/SKILL.md             ← Skill 1
    ├── pfc-mkt-content-ideation/SKILL.md              ← Skill 2
    ├── pfc-mkt-title-thumbnail/SKILL.md               ← Skill 3
    ├── pfc-mkt-script-builder/SKILL.md                ← Skill 4
    ├── pfc-mkt-shorts-strategy/SKILL.md               ← Skill 5
    ├── pfc-mkt-seo-discovery/SKILL.md                 ← Skill 6
    ├── pfc-mkt-community-loyalty/SKILL.md             ← Skill 7
    └── pfc-mkt-monetise-early/SKILL.md                ← Skill 8
```

---

*Built by PF Core for the Women in Tech Power Group. v1.0.0 — 2026-03-22*
