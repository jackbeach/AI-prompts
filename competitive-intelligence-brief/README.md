# Competitive intelligence brief

A monthly scheduled prompt that scans public signals about your competitors and produces a focused intelligence report — what's actually moving, what's likely to change product strategy, and where opportunities for differentiation are opening up.

## What it does

Most competitive intelligence reports lean too hard on news aggregation. They tell you what every competitor announced last month and leave you to figure out what matters. This prompt is built differently — it's designed to triangulate convergent signals across multiple sources, weight evidence by how many independent sources confirm it, and surface only the moves likely to change a real decision.

The trick is the triangulation, not the scanning. Any single signal is noise. The same signal showing up across three sources — a pricing change announced on the product page, hinted at in a job posting, and confirmed by a review on G2 — is structural. The prompt is built to find structural signals and ignore the rest.

The output is monthly. The cadence is intentional: weekly produces too much noise (most competitors don't change strategy weekly), quarterly is too slow to act on, monthly catches the rhythm of actual market movement.

## What gets scanned

Eight categories of public signal:

1. **Pricing pages** — changes to price, packaging, tier names, included features, and discount structures
2. **Hiring postings** — what roles competitors are filling, in what disciplines, in what regions
3. **Integration marketplaces** — new integrations launched, integrations deprecated, partnership announcements
4. **Review sites** — recurring themes in customer reviews, particularly recent ones (G2, Capterra, TrustRadius)
5. **Regulatory filings** — for public competitors, what's appearing in earnings calls, 10-Ks, S-1s
6. **M&A activity** — acquisitions, fundraising rounds, executive moves
7. **Product changelogs** — what shipped in the last month, what's been hinted at in roadmaps
8. **Press and partnerships** — major customer wins, partnership announcements, conference presence

The eight categories aren't equal in weight. Pricing changes and hiring patterns tend to be the highest-value signals because they're the hardest to fake — they reveal where competitors are putting actual money. Press and changelogs are useful for confirmation but lower on their own.

## How signals get weighted

The prompt is built around a confidence scale. Every claim in the output gets weighted by the strength of the underlying evidence:

- **High confidence** — three or more independent sources confirm the same direction
- **Medium confidence** — two independent sources, or one strong source (regulatory filing, executive statement)
- **Low confidence** — single source, or signals that could be interpreted multiple ways
- **Speculation** — explicitly flagged when the prompt is connecting dots that aren't fully evidenced

This matters because competitive intelligence consumed without confidence weights tends to over-react to weak signals. The framework forces the brief to be honest about how much it knows.

## What's in this folder

- **[competitive-intelligence.md](./competitive-intelligence.md)** — the prompt itself
- This README — context and customization guidance

## Customizing the prompt

Two things need to change for your environment.

**Your competitor list.** Start with three to seven competitors. More than seven and the brief becomes unfocused; fewer than three and there's not enough cross-comparison signal. Include direct competitors (same buyer, same problem), adjacent competitors (different angle on the same buyer), and at least one indirect competitor (different problem, but could displace yours). Update the list quarterly.

**Your strategic context.** The brief is more useful when it knows what you care about. Tell the prompt your current strategic priorities — for example, *"we're expanding upmarket from SMB to mid-market, which means we care most about how competitors are positioning for mid-market buyers and what their enterprise feature gaps look like."* The brief will weight signals against that context rather than treating all competitor moves as equally interesting.

If you don't customize either of those, the prompt will produce something useful anyway — just less sharp than it could be.

## Patterns worth watching

A few signal patterns that consistently produce high-value intelligence:

**Coordinated pricing moves across competitors.** Two or more competitors changing pricing in the same direction within a quarter usually signals a structural shift in the market — buyer expectations changing, a new entrant pressuring the segment, or a wave of churn forcing repositioning. Single-competitor pricing moves are noisier; coordinated moves matter.

**Hiring patterns that don't match stated strategy.** A competitor positioning publicly as "AI-first" but hiring exclusively for traditional engineering roles is telling you something. So is a competitor announcing they're "doubling down on enterprise" while hiring only SMB sales reps. The gap between stated strategy and hiring strategy is usually the more honest signal.

**Integration marketplace deprecations.** Companies don't deprecate integrations casually — there's almost always a partnership souring or a strategic pivot behind it. A deprecated integration is more informative than a launched one.

**Review themes that shift suddenly.** A competitor whose reviews have been stable for two years suddenly developing a recurring complaint is signal. The signal might be a regression, a culture shift, a key team departure — but it's worth investigating.

**Quiet competitors going louder.** A competitor that's been heads-down on product for a year suddenly increasing PR, content marketing, or conference presence usually means they're preparing for a fundraise, a launch, or both.

## Output destination

The brief publishes to wherever you want it — Notion database, Google Doc folder, Confluence space, internal wiki. The destination matters less than the persistence; you want to be able to look back at what the brief said three months ago and check whether it was right.

Track which predictions came true and which didn't. Over time, this becomes a calibration loop — you'll learn which signal categories tend to lead actual market moves versus which produce false positives in your specific market.

## Cadence and discipline

Run it monthly, on a fixed day. The first Monday of the month is a useful default — it gives you a competitive context check at the start of every month, before the prior month's signals fade.

The discipline is reading the brief and *acting on it*. Most competitive intelligence dies because it gets read and filed. Build a small ritual: 30 minutes after the brief lands to identify what should change in your roadmap, positioning, or pricing — even if the answer is "nothing this month." The exercise of asking is what makes the brief worth running.

## License

MIT. See the root [LICENSE](../LICENSE).
