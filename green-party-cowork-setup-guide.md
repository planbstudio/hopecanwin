# Hope Can Win — Cowork Setup Guide

**Automated daily counter-media briefings for Green Party supporters.**

This guide walks you through setting up an automated daily media monitoring briefing using Claude's Cowork mode. Once configured, it will search hostile media coverage, build a full briefing, and prepare an email draft for your review — every day, hands-free.

**You will need:**
- A Claude Pro or Team subscription with Cowork mode enabled
- A Gmail account (for email delivery)
- About 15 minutes for initial setup

**What you'll get:**
- A daily briefing covering hostile Green Party media coverage
- Story-by-story rebuttals with talking points
- A ready-made social media content kit for supporters
- Email delivery to your chosen recipients (with your approval each time)

---

## Part 1: Install the Skill

### Step 1 — Create the skill folder

In your Cowork session, ask Claude:

> "Create a new skill called `hope-can-win`"

Or manually create the folder structure:

```
.claude/skills/hope-can-win/
└── SKILL.md
```

### Step 2 — Add the SKILL.md file

Copy the entire SKILL.md template from **Part 3** of this guide into that file. You can ask Claude to do this for you:

> "Create the file `.claude/skills/hope-can-win/SKILL.md` with the following content..."

### Step 3 — Configure your settings

Before running, edit these placeholders in the SKILL.md:

| Placeholder | Replace with | Example |
|---|---|---|
| `[YOUR_RECIPIENTS]` | Comma-separated email addresses | `media-team@greenparty.org, campaign-lead@greenparty.org` |
| `[YOUR_NAME]` | The sender name for emails | `Hope Can Win` |
| `[LOCAL_CANDIDATE]` | Your local candidate (or delete for national only) | `Zoe Smith, Green candidate for Bristol East` |
| `[LOCAL_ISSUES]` | Key local issues (or delete) | `Air quality, housing, NHS waiting times` |

**A note on scope:** This hostile media monitoring works best for candidates at MP, mayoral, or regional level — where national right-wing outlets are likely to run attack pieces. Ward-level council candidates are unlikely to attract hostile national coverage. For ward candidates, a different kind of toolkit (built from the candidate's policies outward, not against media inward) is a better fit — and is on the roadmap.

---

## Part 2: Set Up the Daily Schedule

### Option A — Scheduled task (recommended)

In your Cowork session, say:

> "Create a scheduled task that runs every morning at 7am using the hope-can-win skill. It should build the full briefing and prepare an email draft for my review — but never send without my confirmation."

Claude will create a scheduled task. You can check on your tasks anytime:

> "List my scheduled tasks"

### Option B — Manual daily run

If you prefer to trigger it yourself each day, just open Cowork and say:

> "Run the Hope Can Win briefing"

---

## Part 3: SKILL.md Template

Copy everything below into your SKILL.md file.

---

````markdown
# Hope Can Win — Daily Counter-Media Briefing (v9)

## Purpose
Produce a comprehensive daily counter-media briefing for the Green Party of England and Wales. Search hostile outlets, build rebuttals, generate talking points, and prepare a supporters content kit — then format as an email for review.

## Critical Rules — Read Before Every Run

1. **FULL BRIEFING ALWAYS** — Never produce a digest, summary, or shortened version. Every section must appear in full. There is no character limit — use editorial discipline only.
2. **5-DAY WINDOW** — Only include stories published within the last 120 hours. Calculate the cutoff date from today's date. Discard anything older.
3. **ANTI-REPETITION** — Before writing, check for previous briefing files saved in this workspace (look for files matching `hope-can-win-briefing-*.md` or similar). Exclude any stories already covered in those files. Every briefing must contain only fresh material. After generating the briefing, save a copy with today's date for future anti-repetition checks.
4. **SOCIAL FALLBACK** — If fewer than 5 genuinely hostile stories are found, activate [GP VOICE] mode: supplement with proactive Green messaging, policy wins, and rebuttal angles on national news. Label clearly.
5. **SUPPORTERS CONTENT KIT** — Mandatory. Always included. Never cut, never reduced. All four platforms every time.
6. **USER CONFIRMS EMAIL** — Never auto-send. Always present the draft and wait for explicit confirmation before sending.

## Search Methodology

Execute ALL 7 searches using web search. Do not skip any.

| # | Query | Target |
|---|---|---|
| 1 | `"Green Party" site:gbnews.com` | GB News |
| 2 | `"Green Party" site:thesun.co.uk` | The Sun |
| 3 | `"Green Party" site:dailymail.co.uk` | Daily Mail |
| 4 | `"Green Party" site:telegraph.co.uk` | The Telegraph |
| 5 | `"Green Party" site:express.co.uk` | Daily Express |
| 6 | `"Green Party" site:spectator.co.uk` | The Spectator |
| 7 | `"Green Party" LBC Politics` | LBC |

**Date filter:** Only results from the last 5 days (120 hours from now).

## Briefing Structure

Produce in this exact order. Do not omit or merge any section.

### Section 1: Today's Media Landscape
Strategic overview (3–5 paragraphs). Current narratives being pushed, overall tone, pressure points, and what's changed since the last briefing.

### Section 2: Story-by-Story Rebuttals
For EACH hostile story:
- **Outlet & headline** (with URL where available)
- **Date published**
- **Summary** of the attack or misrepresentation (2–3 sentences)
- **The facts** — what the story gets wrong or omits
- **Rebuttal line** — clear, quotable, spokesperson-ready
- **Suggested response** — engage, rebut publicly, or monitor only

### Section 3: Talking Points
5–8 crisp talking points for media appearances. Address the stories above AND provide proactive messaging.

### Section 4: Supporters Content Kit
Ready-to-adapt content for ALL FOUR platforms. Never omit any.

**TikTok:**
- Opening hook (first 3 seconds)
- Key message (15–30 seconds)
- Call to action
- Hashtags

**Twitter/X:**
- 3–5 tweet thread (strongest rebuttal of the day)
- Quote-tweet strategy for hostile coverage
- Hashtags

**Instagram:**
- Carousel breakdown (5–7 slides)
- Caption with CTA
- Story poll or question sticker idea

**Facebook:**
- Shareable post (150–250 words) for community groups
- Engagement question
- Image/infographic concept

### Section 5: Today's Priority Action
One specific, achievable action a supporter can take today.

## Party Reference Information

| Role | Name |
|---|---|
| Leader | Zack Polanski |
| Co-Deputy Leader | Rachel Millward |
| Co-Deputy Leader | Mothin Ali |
| Former co-leader | Carla Denyer (reference where historically relevant) |

## Local Focus (Optional)

Candidate: [LOCAL_CANDIDATE]
Key issues: [LOCAL_ISSUES]

Delete this section entirely if running a national-only briefing.

## Email Delivery Method (Gmail via Cowork)

When the briefing is complete, deliver it by email using this exact method:

### Step-by-step:
1. Navigate to the user's Gmail inbox (the tab should already be open or open gmail.com)
2. Click the **Compose** button to open a new message window
3. Fill in the recipients: `[YOUR_RECIPIENTS]`
4. Set the subject line: `Hope Can Win — Daily Briefing — [TODAY'S DATE]`
5. **Inject the briefing body using JavaScript** — use the browser console or DOM manipulation to paste the full HTML-formatted briefing into the compose body
6. **STOP. Do not click Send.**
7. Present the user with a summary: "Your briefing email is drafted and ready. Recipients: [list]. Subject: [subject]. Please review and confirm before I send."
8. Only click Send after the user explicitly confirms.

### Critical email rules:
- **NEVER use URL-based mailto: or Gmail compose links** — these cause 400 errors with long content
- **NEVER auto-send** — always wait for user confirmation
- **Use JavaScript injection** to populate the email body — this is the only reliable method for long-form content
- The sender name should appear as: `[YOUR_NAME]`

## Quality Checklist (Run Before Delivery)

Before presenting the briefing or drafting the email, verify:

- [ ] All 7 searches were executed
- [ ] No stories older than 120 hours are included
- [ ] No stories from previous briefings are repeated (checked against saved briefing files)
- [ ] All 5 briefing sections are present and complete
- [ ] Supporters Content Kit covers all 4 platforms
- [ ] [GP VOICE] fallback activated if fewer than 5 hostile stories
- [ ] Briefing saved to workspace with today's date for future anti-repetition
- [ ] Email is drafted but NOT sent
- [ ] User has been asked to review and confirm
````

---

## Part 4: Troubleshooting

**"The briefing seems cut short"**
Say: *"Continue — complete all remaining sections in full."* The skill rules prohibit truncation, but very long outputs sometimes need a nudge.

**"I'm seeing stories from more than 5 days ago"**
Say: *"Check the dates — only include stories from the last 120 hours. Discard anything older."*

**"The email won't send / I get a 400 error"**
This usually means Claude tried to use a URL-based compose method. Say: *"Use the JavaScript injection method to compose the email — do not use URL-based compose."*

**"Stories are repeating from yesterday's briefing"**
Say: *"Check the saved briefing files in the workspace and exclude any previously covered stories."* If no files are found, the anti-repetition history may have been lost — Claude will start fresh.

**"I want to change the recipients"**
Edit the `[YOUR_RECIPIENTS]` placeholder in your SKILL.md file, or just tell Claude: *"Send today's briefing to these addresses instead: ..."*

**"I want to add more outlets to monitor"**
Tell Claude: *"Add a search for 'Green Party' site:newtarget.co.uk to the methodology."* For a permanent change, add a row to the search table in your SKILL.md.

**"I want to stop the daily schedule"**
Say: *"Pause the Hope Can Win scheduled task"* or *"Delete the Hope Can Win scheduled task."*

---

## Part 5: Sharing This With Others

This guide is designed to be self-contained. To share it with another Green Party supporter:

1. Send them this file.
2. They need their own Claude Pro/Team subscription with Cowork enabled.
3. They configure their own email addresses and local focus.
4. Each person's setup is independent — no shared accounts or credentials needed.

No personal data, email addresses, or account details are included in this template. Each user configures their own.

---

*Hope Can Win is a supporter-made toolkit, not an official Green Party product. Built to help Green supporters fight back against hostile media — because hope can win when we show up prepared.*
