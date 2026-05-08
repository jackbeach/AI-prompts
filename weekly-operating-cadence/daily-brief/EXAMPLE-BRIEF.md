# Example brief

A complete brief showing what the framework produces in practice. The names, products, and metrics here are fictional — the structure is real.

The example is written for a Senior Product Manager at a fictional B2B SaaS company called Northwind, working on a product called Atlas. The team is small (four engineers, one designer). The reader's quarter is anchored on shipping a major redesign, improving free-to-paid conversion, and rebuilding their analytics instrumentation.

This is what the brief looks like on a Wednesday in week 3 of a sprint.

---

## The brief

**Today's actions — 5 ready**

1. Decide whether to delay the redesign launch — *decide*
2. Update the redesign launch ticket with the analytics dependency — *update*
3. Send the framing message to your manager about the launch decision — *send*
4. Stage the customer comms draft for Friday morning if launch holds — *stage*
5. Block the 30-minute deep-work window on Thursday — *manual*

Full detail in section 3 below.

---

### The situation

The redesign launches Friday, but Statsig has been dark for four days entering launch week, and two engineers are out Thursday-Friday. We will ship the redesign and be unable to measure whether it worked, with reduced engineering capacity to respond if anything breaks. The launch decision is the day's only strategic call; everything else is communication and prep around it.

### Forecast

**Sprint trajectory.** At current velocity (1.4 tickets/day vs. the 1.7/day required), the sprint will close with two of the seven committed redesign tickets unfinished. The two most likely to slip are the empty-state animations and the onboarding tooltip rewrite — both polish-tier, both deferrable to next sprint without breaking the launch. Confidence: high.

**Risk cascade.** If Statsig stays dark AND the redesign ships Friday AND we see a meaningful conversion drop in the first 72 hours, we will not have the instrumentation to diagnose it or the engineering capacity to respond (Marina and Devang are out, Sam is on the post-launch rotation alone). The compound failure isn't the redesign breaking — it's shipping blind into a thin response window. Earliest intervention: restore Statsig today, OR move the launch to next Tuesday when the team is fully back. Both options are still open this morning; only the second remains open after EOD if Statsig stays down.

**Stakeholder prediction.** Hannah has deferred the "delay launch" conversation twice in the last 10 days, both times citing marketing's calendar pressure. Pre-frame today's ask with the customer-impact angle, not the engineering-readiness angle — she defers on engineering concerns and engages on customer-impact ones based on the last six 1:1s. Confidence: medium.

**Measurement trajectory.** Statsig has now been dark for four consecutive briefs. At current pace of vendor response (their last incident took six days to resolve), there is no realistic scenario where Statsig is operational before Friday's launch. This source has crossed from "inconvenience" to "launch-blocking." The brief will continue to flag it until it's resolved or replaced.

### Today's moves

**Action 1: Decide whether to delay the redesign launch — strategic**

Customer impact of shipping blind is asymmetric: if it works, we gain four days; if it doesn't, we have no instrumentation and no team to triage. The cost of delaying is one cycle of marketing rework. The cost of shipping blind into a degraded response window is potentially weeks of unreversed conversion loss. This decision can't wait past EOD because both alternative paths (restore Statsig, or move the date) require kickoff actions today.

*Type: decide.*

Options on the table:
- Ship Friday as planned, accept blind launch
- Move launch to Tuesday next week (full team back, Statsig may be restored)
- Ship Friday with a manual instrumentation backup (engineering effort: ~6 hours from Sam, who's already on post-launch rotation alone)

Recommendation: option 2. The marketing rework is recoverable; the conversion data isn't.

**Action 2: Update the redesign launch ticket with the analytics dependency — operational**

PROJ-441 currently shows "ready for launch" with no flag for the Statsig outage. Update the description to include the dependency, link to the Statsig incident, and change the status to "blocked on instrumentation" until Action 1 resolves. This is the artifact the team will reference if there's any confusion Wednesday afternoon.

*Type: update.*

Ticket: PROJ-441
Field change: Status → "Blocked on instrumentation"
Description addition: "Launch dependent on Statsig restoration. See incident #STG-2811. If Statsig remains down, see launch decision in today's brief."

**Action 3: Send the framing message to Hannah about the launch decision — strategic priority**

Hannah is your manager and the decision-maker on launch timing. The pre-framing matters: she defers on engineering concerns and engages on customer-impact ones. Lead with customer impact, attach the data, propose a specific call.

*Type: send.*

Target: DM to Hannah on Slack
Message:
> Hannah — quick read on Friday's launch. Statsig has been dark four days; vendor's not responding fast enough to restore by Friday. If we ship as planned, we'll have no conversion data for the first 72 hours and a thin team (Marina and Devang out Thursday-Friday). The customer risk is asymmetric: a blind launch on a degraded response window is worse than a four-day delay.
>
> I want to recommend moving the launch to Tuesday. Marketing rework is one cycle; lost conversion data isn't recoverable. Can we get 15 minutes today to align? I'll have the rollback plan and the comms draft ready either way.

**Action 4: Stage the customer comms draft for Friday morning if launch holds — operational**

If Action 1 lands as "ship Friday," we'll need customer-facing comms about the redesign by Friday 9 AM. Pre-draft now, hold until trigger. If the launch moves, the draft gets repurposed for Tuesday and the trigger never fires.

*Type: stage.*

Trigger: Friday 8:30 AM if PROJ-441 status is "ready to ship"
Draft: [Full email body — 240 words, ready for review]
- Subject line: "What's new in Atlas this Friday"
- Recipient list: customers on Pro and Enterprise tiers (n=1,847)
- CTA: "Try the redesign and tell us what you think"
- Backup CTA if Statsig is still down: "Reply to this email — we're listening directly while we sort out our analytics"

**Action 5: Block the 30-minute deep-work window Thursday — operational**

Thursday is the only window between now and launch where you can write the post-launch monitoring plan without interruption. Marina and Devang are out, so cross-team escalations should be light. If you don't block it now, the calendar will fill.

*Type: manual.*

Step 1: Block 2:00–2:30 PM Thursday on your calendar
Step 2: Title it "Atlas launch monitoring plan — focus block"
Step 3: Set status to "do not disturb" in Slack for that window

### Intelligence

**Operations and execution.** Sprint is on track for the launch tier (5 of 7 tickets), behind on polish tier (2 of 7 likely to slip). Velocity has been stable for three sprints — this isn't a team capacity problem, it's a scope-versus-time problem. The rate-limiter today is the launch decision (Action 1); nothing else can be sequenced until that resolves. Marina and Devang's absence Thursday-Friday creates a real exposure on incident response, not on shipping.

Blocker requiring your action: PROJ-489 (the empty-state animations) needs a scope call from you. The original spec is more polish than the launch needs. Cutting it to a v1 unblocks the sprint and saves Marina ~6 hours next week.

**Measurement reality.** Statsig: dark, day 4, structural. Mixpanel: operational, no movement worth flagging. Free-to-paid conversion has been trending down for 6 days (currently 1.8%, was 2.1% at start of sprint); if the trend continues, we'll be at 1.5% by the end of next week, which is below the floor we've held for the year. This compounds the launch risk: we may be launching into a conversion environment that's already softer than we realize.

The cross-domain connection: the conversion softness started two days after we shipped the new pricing page. That's correlation, not causation — but Statsig being dark means we can't run the funnel analysis to disambiguate. Add this to the post-launch monitoring plan if the redesign ships Friday.

**Competitive and market.** Linear shipped a Slack-style command bar this week, which puts pressure on our keyboard-first workflow positioning. Their announcement focused on speed and developer experience, which directly overlaps our Atlas redesign messaging. Implication: we should de-emphasize the "fastest interface" angle in launch comms and lead with the workflow integration story instead. Marketing needs to know by Thursday EOD if launch holds for Friday.

### Customer signals

**Pattern: pricing page confusion** (escalating). 8 tickets in the last 24 hours from prospects asking which plan includes API access. This pattern was 3 tickets two weeks ago, 5 last week, 8 this week. The new pricing page moved the API access mention into a tooltip; the data suggests the tooltip isn't getting seen. Product implication: needs a copy fix before the redesign launch makes the issue worse.

**Pattern: onboarding completion drop** (new). Internal data shows new-user onboarding completion at 67%, down from a 74% baseline. Three customer conversations this week independently mentioned "I couldn't figure out where to start." The redesign addresses this in step 2 of the new flow. If launch slips to Tuesday, this pattern will continue for another four days at minimum.

### Meetings

**Team availability.** Marina and Devang out Thursday-Friday. If launch ships Friday, the on-call rotation rests entirely on Sam, with Tomás as backup. Tomás hasn't been in the redesign codebase in six weeks. Exposure: real but manageable for a four-day window; would be material for a longer window.

**1:1 with Hannah, 11:00 AM (30 min).**
Drive: alignment on Friday launch decision. See Action 3 for pre-framing.
Likely deferral risk: she'll want to delay the call until "I have more info from marketing." Pre-empt by sharing the Slack DM (Action 3) before the meeting so she's already engaged with the customer-impact framing.

**Sprint review prep, 2:00 PM (1 hr).**
Drive: alignment with engineering on which polish-tier items move to next sprint. Outcome to push: Marina's empty-state animations cut to v1 (Action see operational blocker above).
Skip assessment: required attendance — this is where the scope call gets made.

**Marketing sync, 3:30 PM (30 min).**
Drive: hold the launch comms timeline open until tomorrow morning, pending the Friday vs. Tuesday call.
Skip assessment: required attendance — your absence here means marketing makes assumptions.

### Data source status

| Source | Status | Trend | Notes |
|---|---|---|---|
| Calendar | Full | Stable | — |
| Meeting recaps (Granola) | Full | Stable | — |
| Statsig | Unavailable | Degrading | Day 4 — STRUCTURAL. Vendor not responding fast enough for Friday launch. |
| Mixpanel | Full | Stable | — |
| Slack | Full | Stable | — |
| Linear | Full | Stable | — |
| Zendesk | Full | Stable | — |
| Prior briefs (Notion) | Full | Stable | — |
| Team availability | Full | Stable | Marina/Devang Thursday-Friday flagged. |
| Confluence | Full | Stable | — |
| Competitive intel (Notion) | Full | Stable | Linear announcement logged. |
| Risk register | Full | Stable | Statsig outage now top entry. |

---

## Notes on this example

A few things worth pointing out about the structure of the brief above.

**The situation is two sentences.** Not three, not five. It compresses the whole brief into the one cross-domain insight that drives everything else: the launch is happening into a measurement-dark, capacity-light week. Every other section flows from that frame.

**The forecast does prediction, not analysis.** Each paragraph ends with the specific action that changes the outcome. The cascade paragraph models a compound scenario and identifies the intervention point — that's principle 7 in action. The stakeholder prediction grounds the recommendation in observed pattern data ("she defers on X, engages on Y, based on the last six 1:1s") rather than speculating.

**Today's moves are five actions, not seven or ten.** The fifth action — blocking a calendar window — is small. It's still in the list because if it doesn't happen today, it doesn't happen at all. That's the test: irreversible damage if undone.

**Each action has a complete draft.** The Slack message in Action 3 is the actual words to send, not a sketch. The ticket update in Action 2 specifies the exact field change and exact addition to the description. This is what makes the brief a command interface rather than a to-do list.

**The intelligence section connects dots.** The conversion-softness paragraph in "measurement reality" pulls together a metric trend, a recent ship event, and a measurement gap into a single forward-looking observation. None of those facts in isolation would change a plan; the synthesis does.

**Customer signals are patterns, not tickets.** Eight tickets about pricing page confusion is summarized in one paragraph with the count, the trend, the inferred cause, and the implication. The brief is not a list of tickets.

**The data source status table catches the structural problem.** Statsig has been down four days; the table flags it as structural. This is the source that closes the loop on principle 6 (predict): the table itself becomes pattern data over time.

**The brief is roughly 1,100 words.** That's slightly longer than a typical day (most briefs land closer to 600–800 words), because there's a real strategic decision in play. On a normal day, several sections would be shorter or absent. "All clear" days produce 200-word briefs.

---

## What to take from this

The example is designed to make the abstract framework concrete. The exact wording isn't the point; the structure and discipline are.

If your brief consistently looks like this — a tight situation paragraph, a forecast that ends in actions, five complete drafts, intelligence sections that connect dots rather than list facts, customer signals as patterns, meetings with specific outcomes, a data source table that catches structural problems — the framework is working.

If your brief drifts into longer prose, more actions, lists of tickets, or vague predictions, return to the principles. They're the discipline that keeps the brief sharp.
