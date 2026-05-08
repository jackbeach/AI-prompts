# Data sources

How to map the eleven generic source categories in the prompt to your actual tools.

The brief gets its value from cross-domain synthesis — connections between sources that no single source can make on its own. The eleven categories are designed to cover the surface area where most operational signal lives. You don't need all eleven to start; you need enough variety that the synthesis has something to do.

---

## The eleven categories, with common tools

### 1. Calendar

What it tells you: who you're meeting with today and over the next five business days, what conflicts exist, where the holes in your week are.

**Common tools:** Google Calendar, Outlook, Cron, Fantastical.

What to look for in the scan:
- Today's meetings with attendee context
- Prep-required meetings within 24 hours
- Decisions you need to drive in each meeting
- Conflicts and double-bookings
- Holes in the day suitable for deep work

How to access it: most calendar tools support either direct API access (Google Calendar API, Microsoft Graph for Outlook) or browser automation through their web UI.

### 2. Meeting recaps

What it tells you: what was decided in your meetings, what action items came out of them, what's still open from the last 48 hours.

**Common tools:** Otter, Granola, Fathom, Fireflies, Read.ai. Or manual notes in Notion, a Google Doc, or a notebook.

What to look for in the scan:
- Action items assigned to you with deadlines
- Decisions made (and decisions deliberately deferred — those are signals)
- Stakeholder positions on open questions
- Commitments made by others that you depend on

How to access it: most meeting tools email recaps to you. Searching your inbox for the sender is usually faster than navigating their app. The signal is concentrated; the apps tend to bury it.

### 3. Analytics or business metrics

What it tells you: what your numbers are doing right now and how they've moved.

**Common tools:** Amplitude, Mixpanel, Heap, Google Analytics, Looker, Tableau, Statsig, custom dashboards.

What to look for in the scan:
- Metrics that moved significantly (positive or negative) in the last 24 hours
- Multi-day trends where the direction has been consistent for three or more days
- Metrics that are dark, broken, or producing unreliable data
- North-star metrics relative to where they should be

How to access it: most analytics tools support either API access or scheduled report exports. Browser automation works too, though it's brittle if dashboard layouts change.

A note on this one: stable metrics aren't signal. The brief should only flag movement. If a metric hasn't moved meaningfully, it doesn't belong in the brief — that's principle 4 (compress status to signal).

### 4. Team communication channels

What it tells you: what your team is discussing, what's blocked, what needs your input.

**Common tools:** Slack, Microsoft Teams, Discord.

What to look for in the scan:
- Direct messages and mentions you haven't responded to
- Threads where a decision is awaiting your input
- Incidents or escalations from the last 24 hours
- Unresolved technical or product questions in the channels you own
- Patterns where the same topic is appearing across multiple channels

How to access it: Slack and Teams both support APIs, but for daily briefs, browser-based scanning is often more practical because it captures the human signal (tone, urgency, who's involved) that APIs strip out.

Be specific in the prompt about which channels to scan. "Scan Slack" is useless. "Scan #engineering, #product, #incidents, and DMs for unresolved questions or escalations from the last 24 hours" is right.

### 5. Project tracking

What it tells you: state of the work — what's in progress, what's blocked, what changed overnight.

**Common tools:** Linear, Asana, Monday, Jira, ClickUp, GitHub Projects, Trello.

What to look for in the scan:
- Items that changed state since yesterday
- Items that haven't moved in three or more days
- Blockers requiring decisions from you specifically
- Cross-team dependencies that affect your timeline
- Sprint or workstream burn relative to the goal

How to access it: most project tracking tools have APIs. For Jira specifically, the JQL query language makes targeted scans efficient. For Linear, the GraphQL API is clean.

### 6. Ticket or issue queue

What it tells you: what customers are reporting and what your support team is escalating.

**Common tools:** Zendesk, Intercom, Freshdesk, HubSpot Service Hub, GitHub Issues for product issues.

What to look for in the scan:
- Escalations from the last 24 hours
- Patterns across multiple tickets — the same issue, the same workflow breaking, the same confusion
- High-severity tickets requiring product or engineering response
- Customer-reported issues that haven't been triaged

The brief should describe patterns, not individual tickets. Five tickets reporting the same workflow problem is a signal worth a paragraph; five unrelated tickets is noise that belongs in your support tool.

### 7. Prior briefs

What it tells you: pattern history. What's been carrying over, what's been escalating, what predictions came true, what data sources have been consistently broken.

**Common storage:** Notion database, Google Doc folder, Confluence space, markdown folder in version control.

What to look for in the scan:
- Items that have appeared in three or more consecutive briefs (carry-overs that should be reframed as structural blockers)
- Forecasts that came true (signal-validating) and forecasts that didn't (calibration data)
- Data sources that have been unavailable across multiple briefs (structural problems requiring a fix, not a daily retry)
- Decisions that have been deferred multiple times (suggesting framing isn't working)

This source is what makes the forecast section possible. Without prior briefs, the brief produces analysis but not prediction. The first 5–7 days of running the brief will produce shorter forecasts because the history isn't there yet — that's correct behavior, not a problem.

### 8. Team availability

What it tells you: who's out today and over the next five business days, and what dependencies their absence creates.

**Common tools:** A shared team calendar, time-off tracker (Vacation Tracker, Lattice, BambooHR), or manually maintained list.

What to look for in the scan:
- Anyone out today who owns a blocked or in-flight item
- Upcoming absences in the next five business days with dependency exposure
- Holiday or company-wide closures affecting capacity

This is the source most teams underweight. Knowing your tech lead is out Thursday-Friday changes how you sequence decisions on Wednesday. Most planning tools don't surface this naturally; the brief should.

### 9. Knowledge base

What it tells you: comments and mentions directed at you in your team's documentation system.

**Common tools:** Notion, Confluence, Coda, GitHub Wiki, Google Docs.

What to look for in the scan:
- Mentions of you in the last 48 hours
- Comments on documents you own that need a response
- Documents that were updated and require your review

This source is often light — most active discussion happens in chat or meetings. But it catches the slow-moving things that fall through the cracks of faster channels.

### 10. Market or competitive intelligence

What it tells you: what's happening outside your company that should change how you think about strategy this week.

**Common storage:** A dedicated Notion page, Crayon, Klue, Owler, or manual notes from your own monitoring.

What to look for in the scan:
- Specific competitor moves with implications for your positioning, distribution, or roadmap
- Market or regulatory signals that create urgency on a previously-deferred decision
- Partnership announcements that change your competitive landscape

The principle here is the same as everywhere else: don't report that something exists. Report what its existence means for the work in front of you.

If your company runs the competitive intelligence brief on a separate schedule (the other prompt in this repo), the daily brief just needs to flag anything new since the last competitive brief and let the deeper analysis happen there.

### 11. Risk register

What it tells you: known risks the team is tracking, plus any escalations since the last brief.

**Common storage:** A Notion database, Airtable base, spreadsheet, or dedicated risk-tracking tool.

What to look for in the scan:
- Risks that escalated in severity since yesterday
- Risks that resolved (so they can be removed from active tracking)
- Risks that have been on the watch list without movement for an unusually long time (those tend to be the ones that bite)

If you don't have a formal risk register, this category becomes wherever you currently track watch-items — could be a single Notion page, a section of your weekly notes, anything.

---

## Choosing your sources

You don't need all eleven to start. Five solid sources beat eleven thin ones.

The minimum viable set: calendar, project tracking, team communication, prior briefs, and one of (analytics, ticket queue, market intel) depending on your role.

A product manager probably wants: calendar, meeting recaps, analytics, team communication, project tracking, ticket queue, prior briefs, market intel. Eight sources, all relevant.

A founder probably wants: calendar, meeting recaps, business metrics, team communication, prior briefs, risk register, market intel. Seven sources, weighted toward strategic visibility.

An engineering leader probably wants: calendar, project tracking, team communication, prior briefs, plus a custom source for production metrics or incidents. Five or six sources, weighted toward execution health.

Add or drop sources based on whether they actually produce signal. After two weeks, evaluate: which sources kept showing up in the brief versus which ones got mentioned and immediately dismissed? Drop the latter.

---

## Access and authentication

The brief works best when source access is configured once and runs unattended. A few practical patterns:

**API keys** for tools that support them — most analytics, project tracking, and CRM tools do. Store credentials in a password manager, environment variables, or a secrets manager (depending on how you're running the prompt). Don't commit credentials to your prompt file.

**Browser automation** for tools that don't have clean APIs or where the human-readable view carries signal the API doesn't (Slack, certain meeting tools). This requires authenticated browser sessions to persist between runs.

**Manual scan with notes** for tools that are too small or too irregular to automate. Write it down, paste it into the prompt, run the brief.

The right pattern is whichever one you'll actually maintain. Automation that breaks once a week and doesn't get fixed is worse than manual scanning that runs reliably.

---

## Source-specific notes

A few practical observations from running briefs against real source stacks:

**Calendar APIs require time zone discipline.** If your prompt runs at 7 AM Eastern but your calendar is in another zone, "today's meetings" can drift. Specify time zones explicitly.

**Slack channel volume varies wildly.** A channel with 500 messages overnight can't be summarized accurately in a single API call. Either scan only the most-recent N messages, or pre-filter for mentions and DMs only.

**Analytics dashboards drift.** A working scan today can fail tomorrow because the team renamed a chart. Build in graceful failure — note the source as unavailable and continue.

**Prior briefs grow.** After a few weeks, you'll have 30+ briefs. The forecast section only needs the last 5–7. Pull a bounded window, not the full history.

**Meeting recaps from automated tools are often verbose.** A 60-minute meeting can produce 8,000 words of transcript. Strip to action items and decisions before passing to the prompt — the rest is noise.

---

## When sources fail

The fallback rule is simple: if a source is unavailable, note it inline as `[source unavailable]`, scan what's available, and produce the brief anyway. A short brief is better than no brief.

If a source has been unavailable for three or more consecutive briefs, flag it as a structural problem. The fix isn't another retry — it's investigating why the source keeps failing.

The data source status table at the bottom of every brief is the place this gets tracked. Over time, it becomes a useful artifact in its own right: a record of which parts of your stack are reliable, which are flaky, and which need replacement.
