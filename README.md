# AI-prompts

Production prompts I run on schedules to automate intelligence work. Two here, both designed around signal-over-noise rather than data dumps.

## The prompts

### Daily intelligence brief

[`daily-intelligence-brief/`](./daily-intelligence-brief)

A daily prompt designed to put a leader three to five days ahead of their inbox rather than one day behind it. The shape: scan a configurable set of operational sources (calendar, ticket systems, analytics, comms tools, prior briefs), surface only what changes the plan for today, deliver as five executable actions with a 90-second read budget.

The brief includes a forecast section that uses the last 5–7 days of briefs as a pattern base — what's been carrying over, where velocity is tracking, which decisions keep getting deferred. Predictions grounded in pattern data are the highest-value output; speculation without history isn't allowed.

The opinionated parts: forward-looking signals beat status updates, "all clear" is a first-class output, every action gets a complete draft, omitted sections beat empty headers. Most morning brief tools fail by reporting too much. This one fails — deliberately — by saying less.

### Competitive intelligence brief

[`competitive-intelligence-brief/`](./competitive-intelligence-brief)

A monthly scheduled task that scans eight categories of public signals — pricing pages, hiring postings, integration marketplaces, review sites, regulatory filings, M&A activity, partnership announcements, and product changelogs — and triangulates convergent moves across them. The output is a focused report on what competitors are actually doing, what's likely to change product strategy, and where opportunities for differentiation are opening up.

The trick is the triangulation, not the scanning. Any single signal is noise; the same signal showing up across three sources is structural. The prompt is built to weight convergent evidence, surface confidence levels, and ignore one-off chatter.

## Design philosophy

A few principles shape both prompts.

**Intelligence is prediction, not reporting.** A status update tells you what happened. An intelligence brief tells you what's about to matter.

**Synthesis is the work.** The model can scan and triangulate; it can't tell you what matters in your context. The brief gets you to a decision point faster — it doesn't make the decision.

**Constraints create clarity.** A 90-second read with five actions max forces prioritization. Loosen either constraint and the output devolves into the data dumps these prompts exist to prevent.

**Diffs over state.** Don't tell me what's still true. Tell me what changed.

**"All clear" is a real answer.** If nothing today earns a brief, the brief is permitted to be three lines long. The pressure to fill space corrupts every recurring report.

## How to use

Both prompts are written for Claude with scheduled execution in mind. Drop in your own data sources — Notion databases, calendar accounts, Slack channels, ticket systems — and adjust the role context at the top to match how you work. The structure does the work; the substance is yours.

These are templates, not products. Adapt them.

If you're picking one to start with: the daily intelligence brief is the more foundational of the two. The competitive intelligence brief is more self-contained and easier to drop in if you don't want to commit to daily scheduling.

## Repo structure

```
AI-prompts/
├── README.md                          (this file)
├── LICENSE
├── daily-intelligence-brief/
│   ├── README.md
│   ├── TEMPLATE.md
│   ├── IMPLEMENTATION.md
│   ├── DATA-SOURCES.md
│   ├── INTELLIGENCE-PRINCIPLES.md
│   └── EXAMPLE-BRIEF.md
└── competitive-intelligence-brief/
    ├── README.md
    └── competitive-intelligence.md
```

## License

MIT. Use them, modify them, ship them in your own work. A pointer back is appreciated but not required.
