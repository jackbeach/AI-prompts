---
name: monday-prep
description: Weekly kickoff plan synthesized from the morning brief — week-at-a-glance, decision log, Monday comms drafts, sprint planning prep when applicable
---

# Monday Prep

A Monday-morning prompt that extends the daily intelligence brief into a week-level operating plan. Sets the frame the daily briefs operate within.

## Core idea

The daily brief answers "what's happening today." Monday Prep answers "what does this week look like, and what does today need to do to set it up." It runs on Monday after the daily brief is published, reads from the brief rather than rescanning raw sources, and produces three things: a five-day narrative plan, a decision log for the prior week (what was decided, what got deferred, what needs to land this week), and Monday-specific comms drafts.

The compounding works because Monday Prep doesn't duplicate the daily brief. It reads the brief, extends the time horizon from one day to five days, and does work the daily brief can't — comparing the prior week's plan to what actually happened, surfacing decisions that have been deferred multiple times and need pre-framing, drafting the Monday comms that bookend the week.

## Sources to scan

Read these in this order:

1. **Today's daily brief** — primary source. Most of what Monday Prep needs is already in the brief.
2. **The previous 5 daily briefs** — for week-over-week trajectory: carry-over items, escalated risks, decisions made versus deferred.
3. **Calendar (full week)** — Monday through Friday. What are the prep-heavy meetings? Where are the decision points? Which meetings can be skipped or delegated?
4. **Meeting recap notes (last 7 days)** — for the decision log. What was decided, what was deferred, who committed to what.
5. **Project tracker** — only if today is a sprint boundary. Pull current sprint state for the sprint planning section.
6. **Direct messages and mentions (last 72 hours)** — quick pass for anything that arrived over the weekend.

The daily brief is doing most of the work. Monday Prep is synthesis on top of that, not a parallel scan.

## How to write

The week-level plan should read as narrative, not calendar dump. The test: if a reader executes this week perfectly as described, what does Friday look like? If you can't answer that, the plan is too tactical.

The decision log is where the real value lives. Most decisions don't fail because someone made the wrong call — they fail because the call kept getting deferred until it was made by default. The decision log surfaces deferrals before they harden, including specific pre-framing language for decisions that have been deferred two or more times by the same stakeholder.

The Monday comms are bookends — they close out last week and set up this week's expectations. Draft them as complete messages, not sketches.

## Output structure

Four sections. Omit any with nothing to report.

### 1. The week at a glance

Five paragraphs (one per business day), two to three sentences each. For each day:

- The highest-stakes meeting or decision point that day.
- What the reader should be driving or protecting that day.
- Any dependency or deadline that gates the rest of the week.

Frame the whole thing as a trajectory: by Friday, where should we be? Each day's paragraph contributes to that arc. Don't list meetings; describe the day's role in the week.

### 2. Decision log

Two subsections.

**Decisions made (last 7 days).** For each: what was decided, who decided, when, what follow-through is required this week. Pull from meeting recaps and prior briefs. If nothing material was decided, say so — that's a signal in itself.

**Decisions deferred (last 7 days).** For each: what was deferred, how many times it's been deferred, who owns it, recommended approach to force resolution this week. If a decision has been deferred twice or more by the same stakeholder, include specific pre-framing language designed to prevent another deferral. (The pre-framing should anchor on the dimension the stakeholder engages with, not the dimension they've been deflecting on.)

### 3. Monday comms

Up to three Slack or message drafts, each with a complete draft and a clear target.

**Manager 1:1 prep, if scheduled this week.** A direct message with two or three topics the reader wants to drive. Lead with the topic most likely to be deferred. Include the anchoring data point.

**Team kickoff, if it's a sprint boundary or significant week.** A team channel message naming what's shipping, what's at risk, what the team needs from the reader.

**Stakeholder heads-up, if needed.** A proactive message to a cross-functional partner based on this week's calendar or the daily brief's forecast section.

Each draft is the actual message text in the reader's voice, target specified (DM versus channel, name versus team), executable as-is.

### 4. Sprint planning (conditional)

Only if a sprint planning ceremony is on this week's calendar. Otherwise, skip this section and note "no sprint boundary this week."

When applicable:

- Current sprint state from the project tracker — what's completing, what's carrying over, what's at risk.
- Proposed sprint goal for the upcoming sprint.
- Top three priorities for the new sprint.
- Open scope questions that need resolution in planning.

Draft a planning brief for the team channel with the above, ready to post the morning of sprint planning.

## Output destination

Publish to **[your destination — Notion page, Google Doc, etc.]**. Title format: `Monday Prep — [Day], [Month] [Day], [Year]`. Persistent storage matters here for the same reason as the daily brief: future Monday Preps reference past ones to track decision velocity and stakeholder patterns.

## Constraints

- Read from the daily brief; don't rescan raw sources unless the brief is genuinely missing something at the week level.
- The week-at-a-glance is narrative, not calendar dump. If the section reads as a list of meetings, rewrite it.
- Decisions deferred two or more times by the same stakeholder always get specific pre-framing language. Generic suggestions don't break deferral patterns.
- Comms drafts are complete messages, not sketches. No placeholders.
- Sprint planning section only on sprint boundary weeks. Otherwise note its absence and move on.
- If the daily brief hasn't published yet, wait 10 minutes and retry. If it's still unavailable, build Monday Prep from the previous five briefs and the calendar, and flag the gap.

## Fallback rules

- Daily brief unavailable: build from the previous five briefs and the calendar, flag the gap.
- Meeting recap source empty: skip the decision log and note the gap.
- Project tracker unavailable on a sprint boundary: draft the sprint planning section from the daily brief's sprint signals only, flag what's missing.
- Always produce something. A short Monday Prep is better than no Monday Prep.

## Customization notes

The role context, source list, and output destination are the parts that need to change for your environment. The four-section structure, the decision-log emphasis on deferrals, and the conditional sprint planning section are the framework — modifying those is what causes Monday Prep to drift back toward a generic week-ahead summary.

If your role's natural cadence isn't Monday-to-Friday, shift the prompt's anchor day to whatever your week starts. The structure works for any consistent start-of-period planning rhythm.

Most readers will deploy this only after they've been running the daily brief for two or three weeks. The decision log section in particular requires the daily brief's pattern detection to be working — it pulls from prior briefs to identify the deferral patterns that drive its highest-value output. Adopting Monday Prep before the daily brief has accumulated history produces thin output.
