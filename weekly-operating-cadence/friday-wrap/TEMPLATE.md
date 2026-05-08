---
name: friday-wrap
description: End-of-week synthesis built from the week's daily briefs — week-in-review trajectory, weekly support patterns, cross-functional signals, Friday comms drafts
---

# Friday Wrap

A Friday-morning prompt that closes the week the Monday Prep opened. Synthesizes the week's daily briefs into the patterns and signals no single brief could see on its own.

## Core idea

The daily brief sees one day at a time. Friday Wrap sees the week — patterns that took five days to emerge, support trends that only become visible at weekly resolution, the gap between what Monday Prep planned and what actually happened. It runs Friday morning after the daily brief is published, reads from the week's briefs plus Monday Prep and Wednesday Review, and produces three things: a trajectory narrative for the week, a weekly support synthesis, and Friday comms drafts that bookend Monday Prep.

The cadence loop closes here. Monday Prep set the frame; the daily briefs operated within it; Wednesday Review checked whether the strategy was still right; Friday Wrap synthesizes what actually happened, surfaces what carries into next week, and seeds the prior-week context that next Monday's prep will read.

## Sources to scan

Read these in this order:

1. **This week's daily briefs** — primary source. Mon-Fri briefs from this week.
2. **This week's Monday Prep** — to compare what was planned versus what actually happened.
3. **This week's Wednesday Review** — for OKR confidence ratings and risk status to carry forward into the week-close framing.
4. **Ticket queue (full week)** — for weekly-resolution support pattern analysis. Daily briefs see escalations; Friday Wrap sees the patterns those escalations cluster into across the week.
5. **Cross-functional channels (last 5 days)** — marketing, sales, support-to-product channels. Signals the daily briefs may have compressed or skipped because they didn't meet daily-resolution thresholds.
6. **Meeting recap notes (last 7 days)** — for week-close decision capture.

The daily briefs are the foundation. Friday Wrap is doing weekly-resolution synthesis on top of them, not a parallel scan.

## How to write

The week-in-review is a trajectory statement, not a recap. The test: a reader who didn't read any of the daily briefs should understand from the week-in-review how the week moved the company forward (or didn't), what surprised, and what carries into next week. If the section reads as a summary of the week's events, rewrite it.

The support synthesis is patterns, not tickets. A daily brief might surface "three escalations about pricing page confusion." Friday Wrap looks at the full week and asks "is this a 12-ticket pattern, has the rate accelerated, what does the volume tell us about a product gap?" Patterns at weekly resolution are higher-signal than escalations at daily resolution.

The cross-functional radar is the part most product readers under-invest in. Marketing, sales, and support each generate signals about the product that the product team rarely sees because the signals don't surface in product channels. Friday Wrap's job is to surface those before they become surprises.

## Output structure

Four sections. Omit any with nothing to report.

### 1. Week in review

Three to five sentences. Trajectory narrative answering: what changed this week that matters for next week? Compare what Monday Prep planned to what actually happened — name the biggest gap, the biggest surprise, and the biggest win. End with what's resolved versus what's carrying into next week.

The test: if a reader hasn't read any of the daily briefs and reads only this section, do they understand where the company is now versus where it was Monday morning?

### 2. Support synthesis

Three subsections.

**Patterns.** For each pattern: a descriptive name, the scale (ticket count, user count, trend over the week), how many weeks it's been showing up, the product implication, and the status (new, escalating, stable, resolving). Three to five patterns maximum. Don't list individual tickets unless they're high-severity.

**Gaps and workarounds.** Where are support agents creating workarounds that point to missing product functionality? Where is engineering time getting pulled into support work that should be in the product? Cross-reference with the project tracker — are the right bugs filed and prioritized?

**High-severity incidents.** For each P1 or P2 incident this week: ticket ID, summary, resolution status, customer impact, whether a post-mortem is needed.

### 3. Cross-functional radar

Three subsections, each surfacing signals from outside product that need product attention next week.

**Marketing signals.** Campaigns, launches, content, or messaging shifts that intersect with product work. Things the product team should know about but probably hasn't been told.

**Sales signals.** Deal blockers, feature requests from prospects, competitive losses where the loss reason was a product gap rather than a price or relationship issue.

**Support-to-product signals.** Escalation patterns that point to product gaps, not support gaps. The framing question: is support solving problems the product should solve?

For each signal: what it is, why it matters for product, whether it requires action next week.

### 4. Friday comms

Up to three drafts that close the week.

**Manager week-close.** A direct message: what shipped, what's at risk, any decision the manager needs to make before Monday. Lead with the win.

**Team acknowledgment, if warranted.** A team channel message recognizing a specific accomplishment by name. Only if there's a genuine accomplishment to acknowledge — generic "great week, team!" messages corrupt the signal.

**Stakeholder update, if needed.** A proactive message to a cross-functional partner based on the cross-functional radar signals.

Each draft is the actual message text in the reader's voice, target specified, executable as-is.

## Output destination

Publish to **[your destination — Notion page, Google Doc, etc.]**. Title format: `Friday Wrap — [Month] [Day], [Year]`. Persistent storage matters because next week's Monday Prep reads this Friday Wrap as part of its prior-week context.

## Constraints

- Read from this week's daily briefs, Monday Prep, and Wednesday Review. Don't rescan raw sources unless those are genuinely missing something at the weekly resolution.
- Week-in-review is trajectory, not recap. If it reads as a list of what happened, rewrite it.
- Support synthesis is patterns, not tickets. Three to five patterns maximum.
- Comms drafts are complete messages, not sketches. Team acknowledgments only when warranted.
- If the daily brief hasn't published yet, wait 10 minutes and retry. If still unavailable, build Friday Wrap from the week's available briefs and flag the gap.

## Fallback rules

- Daily brief unavailable: build from available briefs and flag.
- Monday Prep or Wednesday Review missing: skip the comparison subsections and note the gap.
- Ticket queue unavailable: build the support synthesis from customer signals already present in the week's daily briefs and flag the gap.
- Cross-functional channel access limited: surface only the signals available and note the gaps.
- Always produce something. A short Friday Wrap is better than no Friday Wrap.

## Customization notes

The role context, source list, and output destination are the parts that need to change for your environment. The four-section structure, the patterns-not-tickets discipline in support synthesis, and the cross-functional radar framing are the framework — modifying those is what causes Friday Wrap to drift into a generic week-recap that doesn't earn its place.

If you don't have direct access to support tools or cross-functional channels, the prompt scales — work from whatever signals appear in the daily briefs themselves. The weekly resolution still produces value even with reduced source access; it just produces less of it.

Most readers will deploy Friday Wrap alongside Monday Prep, after the daily brief has been running for a few weeks. The two together create the start-of-week and end-of-week structure that turns daily briefs into a visible weekly arc — neither alone produces the same effect.
