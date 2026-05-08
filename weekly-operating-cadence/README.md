# Weekly operating cadence

Four prompts that compose into one operating system for product leadership work.

Most AI automation in product work is one-off — a script that summarizes a meeting, a prompt that drafts a Slack message, a workflow that updates a ticket. Useful, but each one is an island. The thing that's actually scarce isn't automation; it's coherent attention across a week. What's compounding from yesterday? What's likely to slip by Friday? What did Monday's plan miss?

This folder contains four prompts designed to share that attention across a week, each one anchored at a different point in the cadence. They were built to be used together, but each works on its own.

## The four prompts

**[Daily intelligence brief](./daily-brief/)** — runs every morning. The operating layer. Scans the day's signals, surfaces what changes the plan, delivers five actions ready to execute. Reads in 90 seconds. This is the prompt to start with if you're adopting only one.

**[Monday prep](./monday-prep/)** — runs every Monday morning, after the daily brief. The planning layer. Reads from the daily brief and extends it to a week-level plan: what gets driven Monday-through-Friday, what decisions are pending from last week and need to land this week, what conversations need pre-positioning. Sets the frame the daily briefs operate within.

**[Wednesday review](./wednesday-review/)** — runs Wednesday. The strategic layer. The only one of the four that explicitly zooms out from execution to ask whether work still ladders to strategy, whether metrics are measuring the right things, and whether OKRs are tracking. Catches strategic drift before it becomes a quarter-end surprise.

**[Friday wrap](./friday-wrap/)** — runs Friday morning, after the daily brief. The closing layer. Synthesizes the week — what changed, what shipped, what slipped, what surfaced in support and cross-functional channels — and bookends Monday Prep with a reality check. Closes the loop the week opened on Monday.

## How the cadence works

Each prompt reads from the others rather than rescanning raw sources. Monday Prep reads the daily brief and the prior week's Friday Wrap. Wednesday Review reads three days of daily briefs and Monday Prep. Friday Wrap reads the full week of daily briefs plus Monday Prep and Wednesday Review. The compounding works because each prompt sees the system, not just its own slice.

The output of one becomes input to the next. A risk Monday Prep flags becomes something Wednesday Review tracks; a pattern the daily brief surfaces three times becomes structural in Friday Wrap. The cadence is the unit of value, not any single prompt.

## A note on what this is and isn't

This isn't a productivity system in the lifestyle-design sense. It's a working framework for product leaders managing real complexity — multiple teams, multiple stakeholders, multiple workstreams, all moving on different timelines. The four prompts are the structure that makes the complexity navigable rather than overwhelming. They don't make the work easier; they make the work legible.

They're also opinionated. Predict don't report. Diffs over state. Constraints create clarity. All clear is a real answer. Synthesis is the work. Each prompt enforces the same principles, which is what makes them feel like one system rather than four.

The principles are documented in [daily-brief/INTELLIGENCE-PRINCIPLES.md](./daily-brief/INTELLIGENCE-PRINCIPLES.md) — they apply across all four prompts, so the daily brief folder is also the philosophical core of the cadence.

## Adopting the cadence

Most readers won't deploy all four at once, and shouldn't. The cadence works best when adopted in this order:

**Week 1-2: Daily brief only.** Run it every morning. Get the rhythm. Let 5-7 briefs accumulate so the forecast section has pattern data to work with. Decide whether the daily layer is producing real signal in your context before adding more.

**Week 3-4: Add Monday Prep and Friday Wrap.** Once the daily brief is settled, the bookend prompts add the most leverage with the least new effort, because they read from briefs you're already producing. Monday Prep takes about 10 minutes Monday morning; Friday Wrap takes about 15 minutes Friday morning. Together they create the start-of-week and end-of-week structure that turns the daily briefs into a visible weekly arc.

**Week 5+: Add Wednesday Review.** This one requires the most thought to run well. The strategic-drift detection and the metric-health diagnostic are real frameworks, not checklists — they need a reader's judgment to land. By week five, you'll have enough briefs and weekly patterns to populate the Wednesday Review meaningfully. Adopting it earlier produces thin output.

If you're a founder, head of operations, or fractional executive whose work doesn't follow Monday-to-Friday cadence, the structure scales: shift the bookends to whatever your week starts and ends, and the strategic review can move to whichever day fits your rhythm. The principle of "daily operating + weekly bookends + strategic checkpoint" survives the cadence change.

## What's in each subfolder

Each prompt has its own folder containing the prompt itself, a README that explains it, plus supporting documentation (implementation guide, data source mapping, example output). The daily brief folder is the deepest because it's the foundation; the other three are tighter because their structure derives from the daily brief and inherits its principles.

A reader new to all four should start in the daily brief folder, read its README and INTELLIGENCE-PRINCIPLES file, then come back here and pick the next prompt to add based on adoption order above.

## License

MIT. See the root [LICENSE](../LICENSE).
