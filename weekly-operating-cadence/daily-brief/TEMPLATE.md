---
name: daily-intelligence-brief-template
description: Predictive intelligence brief — pattern-based forecasting, action-ready output, 90-second read
---

# Daily Intelligence Brief Template

A framework for building daily briefs that prepare leaders for what's coming, not just what already happened. Drop your role, data sources, and output destination into the bracketed sections and run on a schedule.

---

## Core philosophy

The goal is not domain awareness — it's prediction. The highest form of intelligence is not knowing the current state, but seeing what's about to happen and deciding what to do before it does.

After reading this brief, the reader should be the most prepared person in any room they walk into today — not because they know the current state, but because they've already seen where it's headed.

The test: can you answer "what breaks this week if I do nothing?" and "which conversation today changes the trajectory?" If not, the brief failed.

---

## Writing standard: predict, don't report

Every data point earns its place by carrying an implication about the future, not just the present.

- Lead with the forecast, not the status.
- Connect dots across domains and across time.
- Compress status to trajectory.
- Write for the reader's next decision, not their next status update.

---

## Action model

The brief produces actions, not just analysis. Each action is written so the reader can execute it without going back to gather more context.

The reader scans the action list, decides which to approve or skip, and either executes themselves or delegates. The brief does the synthesis work; the reader makes the decisions.

---

## Data sources to scan

Scan all of these before writing. The value of the brief is cross-domain synthesis — skipping a source creates a blind spot.

1. **Calendar** — today's meetings plus the next five business days
2. **Meeting recaps** — recordings, action items, decisions from the last 48 hours
3. **Analytics or business metrics** — engagement, activation, conversion, retention
4. **Team communication channels** — standup, technical, product, incidents, escalations, research
5. **Project tracking** — current sprint or workstream, blockers, recent state changes
6. **Ticket or issue queue** — unresolved support escalations, customer-reported issues
7. **Prior briefs** — last 5–7 entries for pattern detection and carry-over analysis
8. **Team availability** — out-of-office, holidays, planned absences for the next five business days
9. **Knowledge base** — comments and mentions directed at the reader in the last 48 hours
10. **Market or competitive intelligence** — recent updates on competitive landscape
11. **Risk register** — current risk flags and watch list

**[Configure for your environment.** Replace each with the specific tool, URL, and what to look for. "Scan Slack" is too broad — "Scan #engineering, #product, and DMs for unresolved questions or incidents from the last 24 hours" is right. Be specific. The brief is only as good as its sources.**]**

---

## The seven intelligence principles

Non-negotiable standards that separate intelligence from status reporting.

### 1. Answer "so what?" at the sentence level

Don't report facts. Interpret them.

Bad: "The sprint is 40% complete."
Good: "The sprint is 40% complete, but at current velocity we're tracking 15% behind the pace required to ship the top three roadmap items by sprint close. Either reduce scope today or accept the slip."

### 2. Lead with the conclusion, not the evidence

State the insight first. Provide supporting data second.

Bad: "Q2 NRR declined 2 points. Customer churn interviews revealed three themes: onboarding, docs, mobile. These issues have been flagged in 6 previous briefs."
Good: "Churn is a structural problem (6 briefs flagged, no resolution), not a quarterly anomaly. The three root causes are fixable this quarter, but require prioritizing infrastructure over feature work. Decision needed by Friday."

### 3. Connect dots explicitly across domains

State compound insights with clarity.

Bad: "Marketing traffic is up 4x. Signups are flat. Churn is rising."
Good: "Marketing traffic grew 4x while signups remained flat, which means conversion collapsed. Churn is rising at the same time, which together tells us the current product experience isn't worth the cost — we're burning through new users faster than we're converting them. Without immediate focus on the conversion blocker, increased spend accelerates losses."

### 4. Compress status to signals

Ticket IDs, sprint day counts, and meeting recaps are reference material, not intelligence.

Bad: "PROJ-1234 is in progress. PROJ-1235 is blocked on PROJ-1236. There are 8 tickets in the to-do column."
Good: "Two high-impact features are blocked on a single decision (API design choice). The decision has been pending four days; similar decisions historically take two — this is twice over. If it stays blocked past tomorrow, the team will context-switch and the sprint slips by two days."

### 5. Write for the reader's next conversation

Test: after reading this, is the reader the most prepared person walking into any meeting, thread, or 1:1 today?

### 6. Predict, don't just report

Use historical patterns to forecast what happens next.

Bad: "PROJ-1234 has been unassigned for three days."
Good: "PROJ-1234 has been unassigned for three days. Items unassigned past day five have a 0% completion rate this sprint based on the last three sprints. If it stays unassigned past tomorrow, it won't ship."

### 7. Model the cascade, not just the risk

Individual risks are less useful than compound scenarios.

Bad: "Server performance is degrading. The monitoring system is dark. We're in launch week."
Good: "Server performance is degrading, but monitoring has been dark for three days entering launch week. The team will ship the feature and be unable to observe whether it worked. If performance issues appear post-launch and aren't caught immediately, customer churn will spike. Earliest intervention: restore monitoring by end of day."

---

## Action format

Every action follows the same pattern. Number them sequentially.

```
Action 1: [Title] — [Goal/operational/strategic tag]

One sentence on why this can't wait today and what the consequence is if it does. Reference the forecast section if applicable.

[Type: send / update / decide / stage / manual / multi-step]
[Specific draft — full message text, exact ticket update, or step-by-step path]
```

**Action types:**

- **Send** — A message to a person or channel. Include target, full message text in the reader's voice, and link to where it gets sent. No placeholders.
- **Update** — A change to a ticket, document, or system of record. Include the ticket ID or link, the field, and the exact content.
- **Decide** — A judgment call the reader needs to make today. Include the options being weighed and the implication of each.
- **Stage** — A pre-drafted action that holds until a trigger condition is met (e.g., "sends Friday morning if no reply by Thursday EOD"). Include the trigger and the full draft.
- **Manual** — Requires the reader's direct action because of judgment, sensitivity, or dependency on a meeting. Explain what makes it manual and the fastest path to execute.
- **Multi-step** — A sequence that requires several actions in order (e.g., "update the ticket, then send the team message"). List steps in order.

**Action rules:**

- Every action has a draft. No exceptions.
- Drafts are complete — full sentences, no placeholders, ready to copy.
- Items carried from prior briefs for three or more consecutive days are flagged as structural and reframed as escalations, not carried again as routine tasks.
- Items completed earlier in the same day are marked with strikethrough and moved to the bottom of the list.

---

## Section structure

### Section 1: The situation (2–3 sentences)

The entire brief compressed into what matters most today — the cross-domain insight only visible when reading every input simultaneously.

Rules:
- One paragraph. No headers, no bullets within this section.
- Lead with the highest-stakes connection.
- Name specific risks and business implications, not categories of risk.
- End with what is resolvable today versus what requires a longer decision.
- If a sentence could apply to any day, rewrite it.

### Section 2: Forecast (3–5 paragraphs)

What the brief sees coming that the reader can't yet see from any single source. Answers: "What happens this week if nothing changes? What single action today most bends the trajectory?"

**Sprint or workstream trajectory.** Using historical throughput from the last 5–7 briefs and current state, project what's likely to ship by close, what's likely to slip, and why. Quantify the gap when behind.

**Risk cascade.** Model the compound scenario — two or three risks that, if they intersect, create an irreversible outcome. State as a conditional: "If A stays unresolved AND B happens by [date], then C becomes true, which means [business impact]." Identify the earliest intervention point — the single action that breaks the cascade.

**Stakeholder prediction.** Based on decision patterns from prior briefs and meeting notes, which of today's asks is most likely to be deferred? Pre-position the reader with the framing or data that prevents the deferral.

**Measurement trajectory.** If a data source has been degraded for several days, project when it becomes a launch-blocking issue rather than an inconvenience. If metrics are trending, state where they'll be in seven days at current rate.

Rules:
- Every prediction grounded in historical data or observed patterns. Never speculate without evidence.
- State confidence level (high / medium / low) where appropriate.
- End each paragraph with the specific action that changes the predicted outcome.

### Section 3: Today's moves (5 actions maximum)

The prioritized action plan and the full action list — one list, presented once.

Prioritization order:
1. Overdue commitments
2. Actions that unblock others
3. Actions that break a forecasted risk cascade
4. Strategic priority items
5. Strategic decisions

If there are more than five candidates, apply the test: which actions, if left undone today, create the most irreversible damage? Those five are the list.

If there are no actions worth taking, write "no actions today" and stop. Padding the list corrupts the brief.

### Section 4: Intelligence (three subsections)

Signals only — no status narratives. If information belongs in a project tracker, compress it to one line with the implication, or omit it.

**Operations and execution.** Three to five sentences on health relative to the goal, with comparison to similar points in recent cycles. What's the next critical dependency? What reader-owned decision is the rate-limiter? List blockers requiring reader action — decisions, stakeholder contacts, approvals, scope calls. Flag technical decisions made without reader input that have product implications.

**Measurement reality.** Top insight from analytics with its implication for active initiatives. Metrics that moved significantly with a "so what?" attached. Any measurement system that's dark, broken, or producing unreliable data — and specifically what question can't be answered as a result. One cross-domain connection if a metric connects to engineering, marketing, or support.

**Competitive and market.** Specific competitor moves with implications for the reader's product positioning, distribution, or strategic decisions. Market or regulatory signals that create urgency. No "X exists" statements — only items where the implication is explicit.

### Section 5: Customer signals

Patterns from support escalations, research notes, and user-facing channels. For each pattern:
- Name it descriptively (e.g., "Pattern: onboarding knowledge gap").
- State the scale (how many, how often).
- State the product implication.
- Note the trend if the pattern appeared in prior briefs (new, escalating, stable).

Don't list individual tickets unless they're high-severity. Three to five patterns maximum.

### Section 6: Meetings

**Team availability.** Surface anyone out today or in the next five business days from team calendar. If someone out owns a blocked item or active initiative, name the exposure. If nobody is out, omit this subsection.

**For each meeting today:**
- Time, title, attendees.
- What the reader should drive or be ready to answer — not a recap of last time, the specific outcome to push for.
- Prediction: based on historical patterns, which agenda item is most likely to be deferred? Include the pre-framing that prevents it.
- Skip assessment: if attendance isn't required, write "skip — [reason]" and suggest declining, sending a delegate, or asking for async notes.

For scrum ceremonies within 24 hours: include specific prep — the decision or outcome to drive, not a list of what to review.

### Section 7: Data source status (table)

| Source | Status | Trend | Notes |
|---|---|---|---|

Every source scanned appears. Status: full / partial / unavailable / in progress. Trend: improving / stable / degrading / new issue. If a source has been unavailable for three or more consecutive briefs, flag as structural — needs a fix, not a daily retry.

---

## Output format

### Section order

The situation → forecast → today's moves → intelligence → customer signals → meetings → data source status.

The situation is always first. Forecast always second. Today's moves always third. Data source status always last. Omit any section with nothing to report (except data source status, which is always included). Completed today's moves items use strikethrough and sit at the bottom of the list — they're not removed until the next day's brief.

### Action summary at the top

Before "the situation," include a scannable list of the day's actions:

```
Today's actions — [N] ready

1. [Action title] — [type]
2. [Action title] — [type]
3. [Action title] — [type]

Full detail in section 3.
```

Gives the reader a command palette at the top of the brief.

### Output destination

Publish to **[your destination — a Notion page, a Google Doc, an email to yourself, a Slack DM]**. Persistent storage is required; future briefs reference prior ones for pattern detection. If publishing fails, output the brief inline and flag the publish failure clearly.

---

## Constraints

- Every item appears exactly once, in its highest-value location. Zero duplication across sections.
- Every claim cites its source inline.
- Every action in today's moves has a draft. No exceptions.
- Intelligence principles apply to every sentence. If a sentence doesn't carry an implication, rewrite or cut it.
- Predictions must be grounded in historical data — never speculate without evidence.
- The brief must be readable at the section-summary level in under 90 seconds.
- The action summary block must be scannable in under ten seconds from a phone screen.
- Be thorough on substance, tight on language. No filler — drop "notably," "importantly," "it's worth mentioning."
- "All clear" is a valid output. Never pad.

---

## Fallback rules

- Source unavailable: note inline and continue with the rest. Don't abandon the brief.
- Never fabricate data or predictions. If history is insufficient for a forecast, state that explicitly and note what would be needed.
- Most sources fail: produce a minimal brief listing what failed and why.
- Historical briefs unavailable (first run or empty database): skip the forecast section and note "forecast: insufficient history — will activate after 5+ briefs."
- Always produce something. A short brief is better than no brief.

---

## Customization notes

The role context, source list, action types, and output destination are the parts that need to change for your environment. The structure, principles, and constraints are the framework — modifying them is what causes the brief to drift back toward the status reports it's designed to replace.

If you only have access to a few data sources, the brief still works — it just gets shorter. Don't pad with weak sources to fill the structure.

If your role's natural cadence isn't daily, the prompt scales to weekly or twice-weekly. The 90-second read and five-action ceiling stay; the source scan and historical pattern window stretch to match the cadence.

The first 5–7 days of briefs will lack the historical context for the strongest predictions. The brief gets sharper as the history accumulates — give it a week before judging it.
