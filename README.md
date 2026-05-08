# AI-prompts

Production prompts I run on schedules to automate intelligence work.

The repo has two artifacts: a four-prompt operating cadence designed to share attention across a week of product leadership work, and a standalone monthly competitive intelligence brief.

## What's here

### Weekly operating cadence

[`weekly-operating-cadence/`](./weekly-operating-cadence)

Four prompts that compose into one operating system: a daily intelligence brief, a Monday prep that sets the week's frame, a Wednesday strategic review that catches drift before it becomes a quarter-end surprise, and a Friday wrap that closes the week's loop. Each prompt reads from the others rather than rescanning raw sources, which is what makes them work as a system instead of four parallel automations.

The daily brief is the foundation — read its README and INTELLIGENCE-PRINCIPLES first if you're new to the cadence. The other three prompts inherit its principles and structure.

### Competitive intelligence brief

[`competitive-intelligence-brief/`](./competitive-intelligence-brief)

A monthly scheduled task that scans eight categories of public signals — pricing pages, hiring postings, integration marketplaces, review sites, regulatory filings, M&A activity, partnership announcements, product changelogs — and triangulates convergent moves across them. Built around weighted evidence rather than news aggregation. Single signals are noise; the same signal across three sources is structural.

This one is independent of the weekly cadence. It runs on its own monthly schedule and produces its own output.

## Design philosophy

A few principles shape everything in the repo:

**Intelligence is prediction, not reporting.** A status update tells you what happened. An intelligence brief tells you what's about to matter.

**Synthesis is the work.** The model can scan and triangulate; it can't tell you what matters in your context. The prompt gets you to a decision point faster — it doesn't make the decision.

**Constraints create clarity.** A 90-second read with five actions max forces prioritization. Loosen either constraint and the output devolves into the data dumps these prompts exist to prevent.

**Diffs over state.** Don't tell me what's still true. Tell me what changed.

**"All clear" is a real answer.** If nothing earns a brief, the brief is permitted to be three lines long. The pressure to fill space corrupts every recurring report.

## How to use

The prompts are written for Claude with scheduled execution in mind. Drop in your own data sources — Notion databases, calendar accounts, Slack channels, ticket systems — and adjust the role context at the top to match how you work. The structure does the work; the substance is yours.

These are templates, not products. Adapt them.

If you're picking one to start with: start with the daily intelligence brief inside the weekly operating cadence. It's the most foundational, and the other three cadence prompts depend on briefs accumulating before they produce real signal. The competitive intelligence brief is more self-contained and easier to drop in if you don't want to commit to daily scheduling.

## Repo structure

```
AI-prompts/
├── README.md                           (this file)
├── LICENSE
├── weekly-operating-cadence/
│   ├── README.md
│   ├── daily-brief/
│   │   ├── README.md
│   │   ├── TEMPLATE.md
│   │   ├── IMPLEMENTATION.md
│   │   ├── INTELLIGENCE-PRINCIPLES.md
│   │   ├── DATA-SOURCES.md
│   │   └── EXAMPLE-BRIEF.md
│   ├── monday-prep/
│   ├── wednesday-review/
│   └── friday-wrap/
└── competitive-intelligence-brief/
    ├── README.md
    └── competitive-intelligence.md
```

## License

MIT. Use them, modify them, ship them in your own work. A pointer back is appreciated but not required.
