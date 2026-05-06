# AI Prompts

Production prompts and frameworks I use to automate product management and strategic decision-making with Claude.

**Status:** Open source | MIT License | Production-tested

---

## Frameworks

### 📊 Daily Intelligence Brief

A **daily predictive briefing framework** that prepares leaders for what's coming, not just what happened.

**What it does:**
- Scans 11 data sources (calendar, analytics, Slack, tickets, competitive intel, etc.)
- Extracts forward-looking signals and connects dots across domains
- Forecasts compound risks and identifies intervention points
- Delivers 5 atomic executable actions in 90 seconds
- Operates as a command interface for same-day decision execution

**Best for:** PMs, engineering leaders, founders, operators—anyone managing complexity across multiple sources who needs to stay 3–5 days ahead instead of 1 day behind.

**Includes:**
- Full methodology + 7 intelligence principles
- Step-by-step implementation guide
- Data source configuration for 15+ tools
- Anonymized example brief
- Dispatch workflow for turning insights into actions

→ **[Explore Daily Intelligence Brief](./daily-intelligence-brief/)**

---

### 🎯 Competitive Intelligence Brief

A **monthly scheduled task** that scans 8 data source categories, triangulates convergent signals, and generates a net-new competitive intelligence report automatically.

**What it does:**
- Monitors competitor moves, market shifts, and strategic threats
- Synthesizes intelligence across pricing, features, positioning, partnerships, and hiring
- Identifies which moves create urgency or change product strategy
- Surfaces opportunities for differentiation
- Runs monthly on a schedule with zero manual overhead

**Best for:** Product leaders, founders, strategists who need to stay ahead of competitive landscape without spending hours on research.

→ **[View Competitive Intelligence Brief](./competitive-intelligence-brief/)**

---

## Quick Start

### Daily Intelligence Brief
```bash
1. Read: daily-intelligence-brief/README.md (5 min overview)
2. Understand: daily-intelligence-brief/INTELLIGENCE-PRINCIPLES.md (15 min deep dive)
3. Implement: daily-intelligence-brief/IMPLEMENTATION.md (follow step-by-step guide)
4. Reference: daily-intelligence-brief/EXAMPLE-BRIEF.md (use as template)
```

### Competitive Intelligence Brief
```bash
1. Read: competitive-intelligence-brief/README.md
2. Review: competitive-intelligence-brief/competitive-intelligence.md (the prompt)
3. Customize: Adjust data sources and strategic goals for your market
4. Schedule: Set up daily/weekly/monthly run via Claude scheduled tasks
```

---

## The Philosophy

These frameworks exist because:

1. **Intelligence is prediction, not reporting.** Status updates don't change decisions. Forward-looking insights do.

2. **Synthesis is non-delegable.** No single tool connects dots across domains. Humans must decide what matters.

3. **Command interface beats report.** Insights don't change things; decisions do. Make decisions atomic and immediately executable.

4. **Constraints create clarity.** Forcing 90-second reads + 5 actions maximum eliminates noise and forces prioritization.

5. **Patterns reveal structure.** 5–7 days of historical context reveals what's one-time noise vs. what's a structural blocker.

---

## Use Cases

### Daily Intelligence Brief
- **Product Managers:** Stay aligned across engineering, analytics, customer, competitive signals
- **Engineering Leaders:** Sprint health, dependencies, technical decisions, team capacity
- **Operations:** Multi-team workflows, escalations, process gaps, bottlenecks
- **Founders/Executives:** Company-wide risks, strategic decisions, board readiness
- **Sales Leaders:** Pipeline health, deal risks, competitive threats, closing strategies

### Competitive Intelligence Brief
- **Product Strategy:** What competitors are shipping, positioning changes, feature gaps
- **Pricing Strategy:** Competitor pricing moves, market positioning shifts
- **Go-to-Market:** Partner announcements, market expansion signals
- **Board Prep:** Quarterly competitive landscape updates
- **M&A:** Monitoring acquisition targets and competitive threats

---

## File Structure

```
AI-prompts/
├── README.md (this file)
├── LICENSE (MIT)
├── daily-intelligence-brief/
│   ├── README.md
│   ├── TEMPLATE.md
│   ├── IMPLEMENTATION.md
│   ├── DATA-SOURCES.md
│   ├── INTELLIGENCE-PRINCIPLES.md
│   ├── EXAMPLE-BRIEF.md
│   └── LICENSE (reference only, uses root license)
└── competitive-intelligence-brief/
    ├── README.md
    ├── competitive-intelligence.md
    └── LICENSE (reference only, uses root license)
```

---

## How These Work

### Daily Intelligence Brief

**Workflow:**
1. Run daily (7 AM recommended)
2. Claude scans your 11 configured data sources
3. Brief publishes to Notion/Docs with 5 proposed actions
4. You read brief (90 seconds)
5. You approve/edit actions: "proceed M1, M2, M5"
6. Claude executes actions immediately

**Output:** A brief that answers:
- What breaks this week if I do nothing?
- Which conversation today changes the trajectory?
- What 5 actions should I take right now?

### Competitive Intelligence Brief

**Workflow:**
1. Run monthly (or weekly, depending on your market pace)
2. Claude scans your 8 competitive data sources
3. Report publishes to Notion/Docs with patterns + implications
4. You share with leadership + product team
5. Informs roadmap, positioning, and go-to-market decisions

**Output:** An intelligence brief that answers:
- What are competitors doing?
- Which moves create urgency?
- Where are we losing positioning?
- What opportunities exist?

---

## Getting Started

Choose your framework:

**Want a daily briefing that keeps you 3–5 days ahead of risks?**
→ Start with [Daily Intelligence Brief](./daily-intelligence-brief/)

**Want automated monthly competitive intelligence reports?**
→ Start with [Competitive Intelligence Brief](./competitive-intelligence-brief/)

**Want both?**
→ Read the Daily Brief README first (it's more foundational), then add the Competitive Brief after you've run 5–7 daily briefs.

---

## Real-World Results

Users of these frameworks report:

**Daily Intelligence Brief:**
- 3–5 day lead time on emerging risks
- 90% reduction in daily intake time (3 hours → 15 minutes)
- Same-day decision execution (vs. weekly follow-up)
- Compound risk detection (catching cascades before collisions)

**Competitive Intelligence Brief:**
- Strategic clarity on competitive landscape
- Faster board-ready competitive updates
- Reduced time spent on manual research
- Better informed roadmap prioritization

---

## FAQ

**Q: Can I use these frameworks with [my tool]?**
A: Yes. Both are tool-agnostic. See the DATA-SOURCES.md or competitive-intelligence.md for configuration examples.

**Q: How long does a brief take to generate?**
A: Daily Intelligence Brief: 45–90 min for manual run (60 sec for leader to read). Can be automated with Claude API for 5–10 min runtime. Competitive Intelligence Brief: 2–3 hours monthly.

**Q: Can I run these weekly instead of daily/monthly?**
A: Yes. The framework scales. Daily is recommended for maximum intelligence value, but weekly works if that's your bandwidth.

**Q: Do I need to share these briefs?**
A: No. They're for your decision-making. But many leaders share them with their team/leadership for alignment. See each framework's README for sharing recommendations.

**Q: Can I customize these?**
A: Absolutely. These are templates. Adapt the data sources, strategic goals, section structure, and writing style to your role and organization.

---

## Contributing

These frameworks are open source. Contributions welcome:

- **Domain-specific examples** (PM, sales, engineering, founder, etc.)
- **Tool integration guides** (Asana, Linear, GitHub Projects, Salesforce, HubSpot, etc.)
- **Scheduling solutions** (cron templates, GitHub Actions, Make workflows)
- **Real-world brief examples** (anonymized, full samples from your domain)
- **Tool configurations** (auth setup, API integration, browser automation)

See each framework's README for contribution guidelines.

---

## License

MIT License — use freely, adapt, share. Credit appreciated.

See [LICENSE](./LICENSE) for full details.

---

## Author

**Jack Beach**  
jackwingood@gmail.com
[@jackbeach](https://x.com/jack_beach) on X

These frameworks are built with Claude (Anthropic). Extracted from 12+ months of production use at [companies], open-sourced to help other leaders and operators stay ahead.

---

**Last updated:** May 5, 2026  
**Status:** Production-tested, actively maintained  
**Questions?** Open an issue or start a discussion.
