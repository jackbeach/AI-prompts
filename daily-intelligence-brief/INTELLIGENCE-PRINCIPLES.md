# Intelligence principles

The seven writing standards that separate intelligence from status reporting.

These aren't guidelines. They're the rules that make the brief worth reading at all. A brief that violates them isn't a worse intelligence brief — it's a status report wearing the wrong label.

Every sentence in the brief should pass the test of these principles. If it doesn't, rewrite it or cut it.

---

## 1. Answer "so what?" at the sentence level

Don't report facts. Interpret them.

Most morning reports stop at the data: "Sprint is 40% complete." "Q2 NRR declined 2 points." "Three customers escalated this week." Each statement is true. None of them tell you what to do.

Intelligence finishes the sentence. It connects the data to the implication. *Why does this matter? What's the consequence? What changes because of this?* If a fact in the brief doesn't have a "so what" attached to it, the fact isn't earning its place.

**Bad:** "The sprint is 40% complete."

**Good:** "The sprint is 40% complete, but at current velocity we're tracking 15% behind the pace required to ship the top three roadmap items by close. Either reduce scope today or accept the slip."

The bad version requires the reader to do the interpretation work. The good version does it for them. The reader's time is the scarce resource the brief is built around.

---

## 2. Lead with the conclusion, not the evidence

State the insight first. Provide supporting data second.

This is structural, not stylistic. Most writing teaches the reverse — build the case, then deliver the verdict. That's fine for an essay. It's wrong for a brief, because briefs get scanned. The reader needs to know what's happening before they decide whether to read the supporting evidence.

If the reader stops at the section header, the header should tell them something. If they stop at the first sentence, the first sentence should give them the conclusion. The evidence is for readers who want to verify; the conclusion is for everyone.

**Bad:** "Q2 NRR declined 2 points. Customer churn interviews revealed three themes: onboarding, documentation, and mobile experience. These issues have been flagged in six previous briefs without resolution."

**Good:** "Churn is a structural problem — six briefs flagged, no resolution — not a quarterly anomaly. The three root causes are fixable this quarter, but it requires prioritizing infrastructure over feature work. Decision needed by Friday."

The bad version makes the reader assemble the conclusion. The good version delivers it and lets the evidence support it.

---

## 3. Connect dots explicitly across domains

State compound insights with clarity.

This is the work that only the brief can do. Your analytics dashboard sees one signal. Your project tracker sees another. Your support queue sees a third. Each one is useful in isolation. The compound insight — *what does it mean that A and B and C are all happening at the same time?* — lives in the intersection.

Don't leave the connection implicit. The reader can't be expected to perform the synthesis themselves; that's why they're reading a brief. Spell it out.

**Bad:** "Marketing traffic is up 4x. Signups are flat. Churn is rising."

**Good:** "Marketing traffic grew 4x while signups remained flat, which means conversion collapsed. Churn is rising at the same time, which together tells us the current product experience isn't worth the cost — we're burning through new users faster than we're converting them. Without immediate focus on the conversion blocker, increased spend accelerates losses."

The bad version is three facts. The good version is one insight built from three facts.

---

## 4. Compress status to signals

Ticket IDs, sprint day counts, and meeting recaps are reference material, not intelligence.

A brief is not a status update. The information that lives in your project tracker should stay there. The reader can click through if they want detail. What the brief should surface is the *meaning* of that detail — the trend, the risk, the inflection point.

If a sentence in the brief could be lifted directly from a tracker column or a dashboard cell, the brief is failing. Compress to the signal that underlies the data, with the implication attached.

**Bad:** "PROJ-1234 is in progress. PROJ-1235 is blocked on PROJ-1236. There are eight tickets in the to-do column."

**Good:** "Two high-impact features are blocked on a single decision (API design choice). The decision has been pending four days; similar decisions historically take two — this is twice over. If it stays blocked past tomorrow, the team will context-switch and the sprint slips by two days."

The bad version is a status report you could screenshot from your project tracker. The good version is what the project tracker can't tell you on its own.

---

## 5. Write for the reader's next conversation

The brief is written for what comes after the reader puts it down.

Test: after reading this, is the reader the most prepared person walking into any meeting, thread, or 1:1 today? If yes, the brief did its job. If no, it didn't.

This principle changes what gets included and what gets cut. A historically interesting fact that doesn't connect to anything happening today gets cut. A small signal that sets up tomorrow's hard conversation gets included. The brief is forward-positioning, not backward-summarizing.

A useful sub-test: read each item and ask, *what conversation today does this prepare me for?* If the answer is "no specific conversation, but it's interesting context," the item probably belongs in your background reading, not the brief.

---

## 6. Predict, don't just report

Use historical patterns to forecast what happens next.

Reporting tells you what is. Prediction tells you what's about to be. The second is more valuable, because the reader can still influence the future. They can't influence the past.

Predictions in the brief are grounded in pattern data — the previous 5–7 briefs, observed trends, historical throughput. Speculation without evidence isn't allowed. If the data doesn't support a prediction, the brief should say so explicitly: "insufficient history for prediction — would need [X] more data points." Honest absence beats fabricated certainty.

**Bad:** "PROJ-1234 has been unassigned for three days."

**Good:** "PROJ-1234 has been unassigned for three days. Items unassigned past day five have a 0% completion rate this sprint based on the last three sprints. If it stays unassigned past tomorrow, it won't ship."

The bad version describes a current state. The good version uses the current state plus pattern history to project an outcome — and identifies the inflection point where the outcome can still be changed.

---

## 7. Model the cascade, not just the risk

Individual risks are less useful than compound scenarios.

Most risks, on their own, don't change a plan. A degraded server in isolation is a problem to fix. A deferred decision in isolation is a problem to escalate. What changes a plan is the scenario where multiple risks intersect — where one problem becomes irreversible because a second problem also showed up at the wrong moment.

The brief's highest-value output is the cascade: the conditional forecast that names how individual risks compose into something worse than the sum of their parts. Stated as a conditional ("if A stays unresolved AND B happens by [date], then C becomes true, which means [business impact]"), the cascade tells the reader where to intervene before the compound scenario hardens.

**Bad:** "Server performance is degrading. The monitoring system is dark. We're in launch week."

**Good:** "Server performance is degrading, but monitoring has been dark for three days entering launch week. The team will ship the feature and be unable to observe whether it worked. If performance issues appear post-launch and aren't caught immediately, customer churn will spike. Earliest intervention: restore monitoring by end of day."

The bad version lists three risks. The good version composes them into a scenario, names the consequence, and identifies the single action that breaks the chain.

---

## How the principles work together

The seven principles aren't independent. They reinforce each other.

Principle 1 (so what?) and Principle 2 (lead with conclusion) are about *what each sentence does*. Principle 3 (connect dots) and Principle 7 (cascade) are about *how facts combine into insight*. Principle 4 (compress status) and Principle 5 (next conversation) are about *what the brief includes and excludes*. Principle 6 (predict) is about *time orientation* — pulling the reader's attention from what happened to what's about to happen.

Together, they describe a single thing: a brief that respects the reader's time, surfaces meaning rather than data, and points forward rather than backward.

Drift on any one principle and the brief gets a little worse. Drift on several and the brief becomes a status report.

---

## Using the principles to revise

The principles are most useful as a revision checklist, not a writing prompt.

Write the brief first. Then read it through, principle by principle:

- *Does every sentence carry an implication?* If not, rewrite or cut.
- *Does each section lead with the conclusion?* If not, restructure.
- *Are connections across domains explicit?* If not, write the connecting sentence.
- *Is status compressed to signal?* If not, delete the status and keep the signal.
- *Does each item prepare a specific conversation?* If not, ask why it's there.
- *Are predictions grounded in pattern data?* If not, mark as insufficient history.
- *Are compound risks named?* If not, model the cascade.

The first few briefs will fail several of these on the first pass. That's expected. The discipline of revising against the principles is how the brief gets sharp — and over time, how the writing changes upstream so the first draft starts hitting them by default.
