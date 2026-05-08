# Monday Prep

A Monday-morning prompt that extends the daily intelligence brief into a week-level operating plan.

This prompt sits in the [weekly operating cadence](../). It runs Monday after the daily brief is published, reads from that brief plus the previous five days of briefs, and produces a five-day plan, a decision log for the prior week, and Monday-specific comms drafts.

## What it does

Three things the daily brief doesn't:

**Sets the week-level frame.** The daily brief operates within a week; Monday Prep designs the week. A five-day narrative plan that frames Tuesday through Friday in terms of what each day contributes to where the week needs to land by close of business Friday.

**Surfaces decision drift.** A decision log of what was decided versus deferred in the prior seven days, with specific pre-framing language for any decision deferred twice or more by the same stakeholder. Most decisions don't fail because someone made the wrong call — they fail because the call kept getting deferred until it was made by default.

**Drafts the Monday comms.** The proactive messages that bookend the week — manager 1:1 prep, team kickoff if it's a sprint boundary, stakeholder heads-up when the calendar warrants it. Each draft is a complete message, not a sketch.

## What's in this folder

- **[TEMPLATE.md](./TEMPLATE.md)** — the full prompt

Monday Prep inherits its principles, data source mappings, and structural philosophy from the [daily brief](../daily-brief/). It doesn't have its own implementation guide because the daily brief's IMPLEMENTATION.md covers the patterns that apply to all four cadence prompts.

## When to add this to your cadence

After two or three weeks of running the daily brief alone. Monday Prep depends on the daily brief's pattern detection to produce its strongest output — the decision log section in particular pulls from accumulated briefs to identify deferral patterns. Adopting Monday Prep before the daily brief has history produces thin output.

Once added, Monday Prep takes about 10 minutes Monday morning. It runs after the daily brief, not in place of it.

## License

MIT. See the root [LICENSE](../../LICENSE).
