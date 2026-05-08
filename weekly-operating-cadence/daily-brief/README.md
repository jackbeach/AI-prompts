# Daily intelligence brief

A daily prompt that puts a leader three to five days ahead of their inbox rather than one day behind it.

## What it does

Most morning reports tell you what happened yesterday. This one tells you what's about to matter today.

The prompt scans a configurable set of operational sources — calendar, project tracking, communication channels, analytics, customer signals, prior briefs — and produces a short brief structured around what changed, what's about to change, and the five actions most worth taking today. It's designed to be read in 90 seconds and acted on in five minutes.

A few things that distinguish it from a standard daily digest:

It looks back to look forward. The last 5–7 days of briefs become the pattern base for forecasting — what's been carrying over, where velocity is tracking, which decisions keep getting deferred. Items that have persisted across three or more briefs are reframed as structural blockers, not routine carry-overs.

It models compound risk, not just individual risk. The forecast section explicitly looks for the cascade: "if A stays unresolved AND B happens by Friday, then C becomes irreversible." Single-source risks rarely change a plan; compound scenarios do.

"All clear" is a valid output. If nothing today earns a full brief, the brief is permitted to be three lines long. The pressure to fill space corrupts every recurring report — this one resists it deliberately.

## How it's structured

Seven sections. Each omits when there's nothing to report. Total length on a normal day runs around 400 words.

1. **The situation** — the cross-domain insight that only emerges from reading every input simultaneously
2. **Forecast** — what happens this week if nothing changes, and what action today most bends the trajectory
3. **Today's moves** — five actions maximum, each with a complete draft ready to execute
4. **Intelligence** — operations signals, measurement reality, competitive and market signals
5. **Customer signals** — patterns from support and research, not individual tickets
6. **Meetings** — today's calendar with the specific outcome to drive in each
7. **Data source status** — which sources worked, which didn't, which have been failing

## What's in this folder

- **[TEMPLATE.md](./TEMPLATE.md)** — the full prompt, ready to customize
- **[INTELLIGENCE-PRINCIPLES.md](./INTELLIGENCE-PRINCIPLES.md)** — the seven writing principles that separate intelligence from status reporting, with examples
- **[DATA-SOURCES.md](./DATA-SOURCES.md)** — how to map the eleven generic source categories to your actual tools
- **[IMPLEMENTATION.md](./IMPLEMENTATION.md)** — step-by-step walkthrough for setting up your first brief
- **[EXAMPLE-BRIEF.md](./EXAMPLE-BRIEF.md)** — an anonymized example showing what the output looks like

## Getting started

Read in this order:

1. This README, then [INTELLIGENCE-PRINCIPLES.md](./INTELLIGENCE-PRINCIPLES.md) — the principles explain why the structure is what it is, and they're the load-bearing claim of the whole framework
2. [EXAMPLE-BRIEF.md](./EXAMPLE-BRIEF.md) — see the output before you commit to setup
3. [DATA-SOURCES.md](./DATA-SOURCES.md) — figure out which of your tools map to which source categories
4. [TEMPLATE.md](./TEMPLATE.md) — drop in your role, sources, and destination
5. [IMPLEMENTATION.md](./IMPLEMENTATION.md) — run your first brief

Plan to run for a week before judging the output. The forecast section is the highest-value part of the brief, and it requires 5–7 days of historical context to work properly. Until that history accumulates, the forecast section will note "insufficient history" — which is the correct behavior. Don't fabricate predictions to fill the space.

## Adapting it

The role context, source list, and output destination are the parts that need to change for your environment. The structure, principles, and constraints are the framework — modifying those is what causes the brief to drift back toward the status reports it's designed to replace.

If you only have access to a few data sources, the brief still works — it just gets shorter. Don't pad with weak sources to fill the structure.

If your role's natural cadence isn't daily, the prompt scales to weekly. The 90-second read and five-action ceiling stay; the source scan window stretches to match the cadence.

## License

MIT. See the root [LICENSE](../LICENSE).
