---
name: wednesday-review
description: Mid-week strategic checkpoint — strategy drift detection, metric health diagnostic, OKR confidence, roadmap progress, risk radar, strategic actions
---

# Wednesday Review

A mid-week strategic checkpoint. The only prompt in the cadence designed to zoom out from daily execution and ask whether work still ladders to strategy, and whether metrics are measuring the right things.

## Core idea

The daily brief answers "what's happening today." Monday Prep answers "what does this week need to do." Friday Wrap answers "what actually happened." Wednesday Review answers a different question: "are we still pointed in the right direction, and would we know if we weren't?"

Most strategic drift isn't dramatic — it's the slow accumulation of execution decisions that each made sense in isolation but together moved the work away from the strategy. By the time the drift is visible at quarter-end, the cost of correcting it is high. Wednesday Review catches drift mid-week, when correction is cheap.

This prompt does its work through two specific frameworks: a ladder audit that traces every active initiative back to a strategic goal, and a seven-type diagnostic that pressure-tests the metrics being tracked. Both are designed to surface drift that's invisible from inside the execution layer.

## Sources to scan

This prompt reads from briefs, not raw sources — the daily briefs have already done the data collection.

1. **This week's daily briefs** — Mon-Wed of the current week, plus the previous five briefs for trend context.
2. **This week's Monday Prep** — to compare what was planned versus what's actually being worked on.
3. **Project tracker** — current sprint state, epic progress, backlog health.
4. **Risk register** — active risks, escalations since the last Wednesday Review.
5. **Market or competitive intelligence** — entries since the last Wednesday Review.
6. **Meeting recap notes (last 3 days)** — decisions and direction shifts from Mon-Wed.

The briefs are the foundation. Wednesday Review does strategic-resolution synthesis on top of them, not a parallel scan.

## Strategic context

Every section in this prompt traces back to a small set of strategic goals. **[Configure for your environment.** The goals are typically the three to seven outcomes the team is committed to delivering this quarter or this half — the things that, if all of them landed, would constitute a successful period. State them explicitly at the top of the prompt; everything below references them by number.**]**

Without explicit strategic goals, the drift detection has nothing to detect drift from. This is the part of customization most teams skip, and the part that most determines whether the prompt produces real value or generic strategic platitudes.

## How to write

Strategic review, not status report. Every sentence carries an implication about whether current direction is right. Lead with the judgment, then the evidence. If a finding could appear in any week's review, rewrite it with this week's specifics.

The ladder audit and metric diagnostic are real frameworks, not checklists. They require the reader's judgment to land — the prompt produces structure and questions, the reader applies them.

## Output structure

Seven sections. Skip any with nothing to report, except the risk radar (always included).

### 1. Strategic verdict

Three to four sentences. The single most important strategic judgment. Not what happened — whether what happened is moving the product in the right direction. The framing question: "if this week's pattern repeats for the rest of the quarter, do we hit goals or miss them?"

Name the biggest strategic risk and the biggest strategic opportunity. End with the one decision that would most change the trajectory.

### 2. Strategy drift detection

This section uses a ladder audit to trace every active initiative back to a strategic goal. The structure of the trace:

> *This work* → addresses *this opportunity* → serves *this objective* → advances *this strategic goal* → moves toward *this vision*

For each active initiative pulled from the project tracker, write a row:

| Initiative | Traces to goal | Chain status | Finding |
|---|---|---|---|
| [name] | Goal [N] | clean / weak / broken | [one-line finding] |

Three sub-checks within drift detection:

**Goal coverage gaps.** Any strategic goal with zero sprint work for two or more weeks. Is the gap intentional sequencing (acceptable) or silent deprioritization (drift)? If it's drift, surface it explicitly — silent deprioritization is the most common form of strategic drift and the hardest to spot from inside execution.

**Initiative graveyard check.** Initiatives that were active two to four weeks ago but have gone silent. Were they completed, paused, or quietly abandoned? If unclear, flag for an explicit call from the reader. Initiatives that "fade" rather than ending cleanly leave residual confusion about what's still committed.

**Shiny object filter.** Anything new in this week's plan that wasn't in the prior week's plan, traced through the ladder. New work in service of an existing goal is learning. New work that requires a different strategy is a decision that needs explicit acknowledgment, not quiet absorption.

Rules for the drift detection section:

- Don't flag normal sprint mechanics (bugs, tech debt, small in-flight work) as drift. The test is discretionary effort versus strategic alignment.
- Drift at the execution layer usually reflects ambiguity higher up. If the ambiguity is upstream, name it.
- If everything traces clean, say so in one sentence and move on. Don't manufacture findings.

### 3. Metric health diagnostic

The seven-type diagnostic. For each metric the team is actively tracking, evaluate against these seven failure modes:

| Type | Definition | Question to ask |
|---|---|---|
| **Detrimental** | The metric improves but customers suffer | Are we hitting green metrics while customer support tells a different story? |
| **Out of reach** | The team owns a metric it can't actually move | Have we missed this for 2+ quarters despite strong execution? |
| **Incomplete** | The metric measures one funnel stage and ignores the rest | Are we celebrating wins at one stage while the next stage is flat? |
| **Pressure** | Short-term urgency crowds out future investment | Are we 100% short-term focused? When was our last exploratory ship? |
| **Inconsequential** | The metric doesn't connect to current priorities | If we 2x'd this metric tomorrow, would anyone notice? |
| **Nonsensical** | Taken to the extreme, the metric destroys value | If we 10x'd this metric, would that actually be terrible? |
| **Incongruent** | Two metrics fight each other | Is one team's win another team's miss? |

For each metric:

- Current status and trajectory.
- Diagnostic flags with evidence (only when evidence supports the flag — speculative diagnosis corrupts the framework).
- Recommended action if flagged.

Two additional checks:

**Metric pair check.** Any two metrics pulling in opposite directions? When found, recommend one of three resolutions: subordinate one metric to the other, replace both with a shared metric, or write explicit rules for the tension.

**Guardrail audit.** For each north-star metric, does it have a paired guardrail that prevents the worst version of optimizing for it? If not, recommend one.

Rules for the metric diagnostic:

- Only flag with evidence from this week's data. Speculative diagnosis is worse than no diagnosis.
- If all metrics are healthy, say so and move on.
- The first Wednesday of each month: full diagnostic on all tracked metrics. Other weeks: focus only on metrics that moved or that were flagged in prior reviews.

### 4. OKR confidence assessment

For each strategic goal:

- **Confidence level:** on track / at risk / off track.
- **Evidence:** one or two sentences citing specific data from this week.
- **Trajectory versus last week:** improving / stable / declining.
- **Key dependency or blocker:** the single thing most determining whether the goal lands.
- **Recommended action if at risk or off track:** one specific move this week.

Rules:

- Ratings grounded in data, not vibes. If the data isn't there to support a rating, say "insufficient data" and state what would be needed.
- A goal rated "at risk" for three or more reviews in a row is effectively "off track" — trajectory is the signal. Surface this explicitly.

### 5. Roadmap and release readiness

**Epic progress.** For each active epic: completion ratio, trajectory toward target date, the single highest-risk ticket.

**Release readiness, conditional.** Only if a release is scheduled in the next two weeks. Cover: completeness, testing status, blockers, and a go/no-go assessment with reasoning.

**Backlog health.** Is the backlog a prioritized queue or a graveyard? How many tickets are unassigned? How many have gone 30 or more days without movement? The answers are signals about planning discipline, not just backlog state.

### 6. Risk radar update

A table of currently tracked risks:

| Risk | Severity | Trend | Owner | Status | Action needed |
|---|---|---|---|---|---|

Flag escalations from this week. Flag any risk that's been open for four or more weeks without movement — those are usually risks that have implicitly been accepted but never explicitly decided on.

If the daily brief's forecast section identified a compound risk cascade, restate it here with updated probability based on this week's evidence.

### 7. Actions and decisions

**Decisions needed.** Decisions that surfaced this week (in briefs, meeting notes, channels) but haven't been made. For each: what the decision is, the deadline, the cost of further deferral.

**Recommended actions.** Up to three strategic actions for the rest of the week. Each one with a complete draft (full message text, specific ticket update, or step-by-step path). Strategic actions only — operational items belong in the daily brief's today's-moves section, not here.

## Output destination

Publish to **[your destination — Notion page, Google Doc, etc.]**. Title format: `Wednesday Review — [Month] [Day], [Year]`. Persistent storage matters here more than for any other prompt in the cadence — the OKR confidence trajectory, the strategic verdict history, and the recurring metric flags compound across weeks into pattern data that Friday Wrap and the next Monday Prep both reference.

## Top summary block

At the top of the published review, before the strategic verdict:

```
Wednesday Review — Week of [Month] [Day]
Verdict: [one sentence]
Drift signals: [count] found / none detected
Metric flags: [count] flagged / all healthy
OKR confidence: [count] on track / [count] at risk / [count] off track
Actions: [count] ready
```

This gives the reader (and any stakeholders the review is shared with) a 10-second summary of strategic state.

## Constraints

- Read from briefs and the project tracker; don't rescan raw sources unless something is genuinely missing at strategic resolution.
- Every OKR rating cites specific evidence. If the evidence isn't there, say "insufficient data."
- Metric flags are evidence-based, never speculative.
- Drift findings trace to specific initiatives and specific goals.
- All recommended actions include complete drafts, not sketches.
- Don't duplicate the daily brief or Friday Wrap. Wednesday Review synthesizes at strategic resolution; the others operate at execution and tactical resolution.

## Fallback rules

- Fewer than three daily briefs this week: note the gap and work with available briefs. Don't skip the review.
- Data source unavailable: note the gap inline and continue.
- Project tracker unavailable: rely on what's in the daily briefs and flag what's missing.
- Risk register unavailable: build the risk radar from the daily briefs' risk callouts and flag the gap.
- Never fabricate confidence ratings, drift findings, or metric flags. If the evidence isn't there, say so.
- Always produce a review.

## Customization notes

The role context, source list, output destination, and strategic goals are the parts that need to change for your environment. The seven-section structure, the ladder audit framework, the seven-type metric diagnostic, and the OKR-trajectory-as-signal pattern are the framework — modifying those is what causes Wednesday Review to drift back toward a generic mid-week status report.

The strategic goals are the most important customization. Without explicit, named goals at the top of the prompt, the drift detection has nothing to detect drift from, the OKR confidence section is generic, and the actions section can't prioritize. Most teams have these goals; few have them written down clearly enough for an AI prompt to use them. Writing them down is part of the work.

Wednesday Review is the most demanding of the four cadence prompts. It expects the reader to engage the frameworks rather than skim outputs. The output is highest-leverage when the reader actually pressure-tests the ladder audit findings and the metric flags rather than accepting them at face value.

Most readers will deploy Wednesday Review only after the daily brief, Monday Prep, and Friday Wrap are all running smoothly — typically four to six weeks after first adoption. Adopting it earlier produces thin output because the historical pattern data isn't there yet, and because the reader is still calibrating against the simpler prompts.
