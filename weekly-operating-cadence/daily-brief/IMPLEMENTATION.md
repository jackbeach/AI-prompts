# Implementation guide

How to set up your first daily intelligence brief, from definition to running it daily.

The whole process takes about four hours of focused work spread across two sittings — roughly 30 minutes of setup, then 2–3 hours producing your first brief manually. After that, daily briefs run in 30–60 minutes (or 5–10 minutes if you automate the source scanning).

The brief gets meaningfully sharper after the first 5–7 days, because the forecast section depends on historical pattern data. Plan to run it for a week before judging the output.

---

## Phase 1: Setup (30 minutes)

### Step 1: Define your role and context

Write down four things in plain language:

- **Your role.** What you actually do day-to-day, not your title.
- **Who depends on you.** Team size, stakeholders, manager.
- **The decisions you make daily.** What's actually on your plate to decide.
- **Your biggest pain point.** What keeps you arriving at meetings unprepared.

Example, paraphrased: *Senior Product Manager managing a small engineering and design pod. Daily decisions span sprint scope, stakeholder alignment, and roadmap trade-offs. The pain point is decisions deferred because I show up to meetings without full context.*

The brief is calibrated to this role context. The clearer it is, the more useful the brief.

### Step 2: Map your eleven data sources

The template references eleven generic source categories. Map each to your actual tool:

| Source category | Common tools |
|---|---|
| Calendar | Google Calendar, Outlook, Cron |
| Meeting recaps | Otter, Granola, Fathom, Notion notes, manual notes |
| Analytics or business metrics | Amplitude, Mixpanel, GA, Heap, custom dashboards |
| Team communication | Slack, Teams, Discord |
| Project tracking | Linear, Asana, Monday, Jira, ClickUp |
| Ticket or issue queue | Zendesk, Intercom, Freshdesk, GitHub Issues |
| Prior briefs | Notion database, Google Doc, Confluence space |
| Team availability | Shared calendar, time-off tool, manual list |
| Knowledge base | Notion, Confluence, GitHub Wiki |
| Market or competitive intel | Notion page, Crayon, manual notes |
| Risk register | Notion, Airtable, spreadsheet |

You don't need all eleven. Five solid sources beat eleven thin ones. Map what you have, leave the rest blank for now.

For each source, write down the URL or location and any access notes (login method, what to look for, what to ignore). This goes into the prompt's data source section.

### Step 3: Define your strategic priorities

List 3–7 priorities that every action in your brief should ladder back to. These are the goals that make an action important rather than just urgent.

Example: *Ship the Q2 release on time. Improve free-to-paid conversion. Reduce support ticket volume. Build reliable churn instrumentation. Close three enterprise deals.*

These get used as tags on actions in section 3 of the brief, so a reader (you, mostly) can see at a glance which priority an action serves.

### Step 4: Set up your brief storage

Choose where the briefs live. Notion is the cleanest option — searchable, template-able, supports linking — but Google Docs, Confluence, or a markdown folder in version control all work.

Two requirements:

- **Persistent.** Each daily brief gets its own page or document, not overwritten each day. The forecast section depends on reading the previous 5–7 entries.
- **Template-able.** A consistent structure makes pattern detection easier and writing faster.

In Notion specifically: create a database called "Daily Briefs" with properties for Date (date type) and Status (select with values like "Action Needed" and "All Clear"). Set a template for the page so each day starts with the same skeleton.

---

## Phase 2: First brief (2–3 hours)

The first brief takes the longest. It's mostly because you're learning the rhythm — by the third or fourth one you'll cut the time in half.

### Step 5: Gather data (60 minutes)

Go through each source. For each, ask:

- What changed since yesterday?
- What's trending up or down?
- What requires a decision from me?
- What compounds with signals from other sources?

Take running notes as you go. You're extracting signals, not summarizing. If something feels too detailed for a brief, it probably is.

Set a timer. 60 minutes maximum. The point is to be thorough but bounded.

### Step 6: Write "the situation" (10 minutes)

Two or three sentences. The cross-domain insight that compresses the entire day.

Process: look across all your notes and ask, "What's the highest-stakes intersection of signals?" Write one sentence naming it. Write one sentence about the business or operational implication. Write one sentence on what's resolvable today versus what requires a longer decision.

Test: if a sentence could apply to any day, rewrite it.

### Step 7: Write the forecast (30 minutes)

Three to five short paragraphs covering: sprint or workstream trajectory, risk cascade, stakeholder prediction, measurement trajectory. See the template for the structure of each.

The discipline here is that every prediction has to be grounded in observable data — historical pattern, current state, observed trend. If the history is thin, say so explicitly: "insufficient history for prediction — would need 5+ briefs of data." Don't speculate to fill the section.

For your first few briefs, the forecast section will be light. That's correct behavior. By brief 6 or 7, you'll have enough history for the forecasts to land.

### Step 8: Write today's moves (30 minutes)

Up to five actions. Process:

**Collect candidates.** Open commitments from meetings, blockers needing your decision, actions from the forecast, overdue items from prior briefs, decisions stakeholders are waiting on.

**Tag each.** Strategic priority (1–7) or operational or strategic.

**Prioritize in this order.** Overdue commitments. Actions that unblock others. Actions that break a forecasted risk cascade. Strategic priority items. Strategic decisions.

**Cap at five.** If you have more than five candidates, apply the test: which actions, if left undone today, create the most irreversible damage? Those five are the list.

**Write each one.** Title, priority tag, one sentence on why this can't wait today, type label (send / update / decide / stage / manual / multi-step), and a complete draft. No placeholders. If it's a Slack message, write the actual words. If it's a ticket update, specify the ticket ID and exact field change.

If there are no actions worth taking today, write "no actions today" and stop. Padding the list corrupts the brief.

### Step 9: Write the intelligence section (30 minutes)

Three subsections: operations and execution, measurement reality, competitive and market.

For each, write in signals not status. If a fact belongs in your project tracker, compress it to one line with its implication or omit it.

**Operations and execution.** 3–5 sentence narrative on health relative to your goals. Compare to similar points in recent cycles where you have the data. Name the next critical dependency. Name the decision that's the rate-limiter. Then list any blockers requiring your action specifically.

**Measurement reality.** Top insight from your metrics with the implication for active work. Metrics that moved significantly with a "so what?" attached. Any measurement system that's dark or unreliable, and what question you can't answer because of it.

**Competitive and market.** Specific competitor moves with explicit implications for your product, distribution, or strategy. No "X exists" statements — only items where the implication is named.

### Step 10: Write customer signals (15 minutes)

Patterns from support and research, not individual tickets. For each pattern: name it descriptively, state the scale, state the product implication, note the trend (new, escalating, stable). Three to five patterns maximum. If nothing significant, write "no patterns this period."

### Step 11: Write meetings (15 minutes)

For each meeting today: time, title, attendees, the specific outcome you should drive (not a recap of last time), and a prediction of which agenda item is most likely to be deferred with a pre-framing line that prevents the deferral.

Skip assessment: if your presence isn't required for a meeting, write "skip — [reason]" and suggest declining, sending a delegate, or asking for async notes. Skipping meetings is a feature.

If teammates are out today or in the next five business days and they own a blocked item, name the exposure here too.

### Step 12: Write data source status (10 minutes)

A four-column table: source, status, trend, notes.

Status values: full / partial / unavailable / in progress.
Trend values: improving / stable / degrading / new issue.

Every source you scanned appears. If a source has been unavailable for three or more consecutive briefs, flag it as structural — needs a fix, not a daily retry.

---

## Phase 3: Publish and review (30 minutes)

### Step 13: Assemble in section order

The situation → forecast → today's moves → intelligence → customer signals → meetings → data source status.

Add an action summary at the top — a scannable list of today's actions with titles and types — so the reader gets a command palette before reading the full brief.

### Step 14: Review against the principles

Read through and check:

- Does every sentence carry an implication, not just a fact?
- Does each section lead with the conclusion before the evidence?
- Are compound scenarios named explicitly, not implied?
- Is status reporting compressed to signals?
- Would the reader be the most prepared person walking into any meeting today?
- Are predictions grounded in history rather than speculation?
- Are compound risks identified, not just individual ones?

If a section fails any of these, rewrite it.

### Step 15: Publish

Save to your storage location. Read it once on your phone — the brief is designed to be readable on a phone screen.

---

## Phase 4: Run it for two weeks

Two weeks is the minimum window to evaluate the framework. Each day, after you read the brief and act on it, ask yourself:

- Did this help me make better decisions today?
- Did I execute the actions, or did they sit?
- Did any forecasts come true?
- Which sections added the most value?
- What signal did I miss that would have helped?

Keep the answers brief — a paragraph in a notebook, not a formal log.

After two weeks, refine based on what you learned:

- **Sources.** Add the ones that produced signal. Drop the ones that didn't.
- **Strategic priorities.** Update if your priorities shifted.
- **Section depth.** Expand sections that mattered. Compress the ones that didn't.
- **Voice.** Adapt the language to how you actually write.
- **Cadence.** If daily isn't sustainable, scale to twice-weekly. Don't quit; reduce.

---

## Optional: automating it

The manual brief works. Automation is optional and only worth doing once the manual rhythm is settled.

A few things you can automate progressively:

- **Source scanning.** A Claude scheduled task can read your sources and produce a draft brief at a fixed time each day.
- **Brief publishing.** The draft can publish straight to your Notion database or Google Doc folder.
- **Action execution.** Once you trust the brief, individual actions (sending a message, updating a ticket) can be automated based on your approval.

Build automation in that order. Source scanning first, because it cuts the most time. Action execution last, because it requires the highest trust in the brief's quality.

---

## Troubleshooting

**The brief takes too long to write.** Start with five sources instead of eleven. Aim for 2–3 sentences per subsection. Reuse yesterday's structure and update only what changed. Set a timer.

**There isn't enough history for the forecast.** Run for 5–7 days first, then activate the forecast section. Until then, note "insufficient history" and move on. Don't fabricate.

**Sources are down.** Use whatever fallback sources you have (DMs, email, memory). Note it in data source status. Publish the brief anyway. Something is better than nothing.

**The actions sit instead of getting executed.** The actions probably aren't actually high-impact. Re-test against the question: "If I leave this undone today, what irreversibly breaks?" If the answer is "nothing much," the action shouldn't have been in the list. Over time, this is how you calibrate which work truly is urgent.

**The brief isn't producing value yet.** Two weeks minimum. The pattern detection and forecast quality both improve with history.

---

## What "working" looks like

After two weeks of consistent use, a few things should be true:

- The brief reads in 90 seconds at the section-summary level.
- You produce roughly five actions per day, most of which you actually execute.
- The forecast section catches at least one risk cascade per week before it becomes a fire.
- You walk into meetings more prepared than you used to.
- Decisions that previously waited a week now happen the same day.

If those things aren't happening, return to the principles and check which one the brief is drifting away from. The framework's job is to enforce them; the discipline is yours.
