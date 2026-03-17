# Full Eval

**Evaluate any idea from every angle -- 6 business evaluators + 8 life advisors in parallel, cross-referenced, delivered as PDF.**

No other tool combines business evaluation with personal life assessment. Most decision frameworks look at the opportunity *or* the person -- never both at the same time. Full Eval runs 14 specialist agents in parallel, cross-references their outputs, and produces a unified verdict that tells you not just "is this a good idea?" but "is this a good idea *for you, right now*?"

## What It Does

```
You: "Should I quit my job to build an AI meal planning app?"

Architect (strategic):
  Opportunity Score: 7.5/10
  Market: Growing, $4B TAM
  Technical: Feasible, proven stack
  Risk: Competitive but defensible

Council (personal):
  Finance: Only 3 months runway -- insufficient
  Health: Burnout indicators from current role
  Career: Strong alignment with ML trajectory
  Relationships: Startup hours strain family time

Meta-Synthesis:
  VERDICT: CONDITIONAL GO
  "Validate for 3 months while employed. Secure 9 months runway.
   Hit 50 beta users and $500 MRR before giving notice."
```

One command. Complete assessment. Professional PDF.

## The Flow

```
                          +-----------+
                          |   INPUT   |
                          | idea/path |
                          +-----+-----+
                                |
                     +----------+----------+
                     |                     |
               +-----v-----+        +-----v-----+
               |  ARCHITECT |        |  COUNCIL  |
               | 6 business |        | 8 life    |
               | evaluators |        | advisors  |
               +-----+-----+        +-----+-----+
                     |                     |
               +-----v-----+        +-----v-----+
               |  Strategic |        |  Personal |
               | Synthesizer|        | Synthesizer|
               +-----+-----+        +-----+-----+
                     |                     |
                     +----------+----------+
                                |
                     +----------v----------+
                     |  META-SYNTHESIZER   |
                     |  Cross-reference    |
                     |  Unified verdict    |
                     +----------+----------+
                                |
                     +----------v----------+
                     |     PDF REPORT      |
                     +---------------------+
```

## What Gets Evaluated

### Strategic (Architect -- 6 Evaluators)

| Evaluator | Analyzes |
|-----------|----------|
| Risk Assessor | Critical risks, failure modes, regulatory concerns |
| Technical Architect | Feasibility, architecture, stack, scalability |
| Market Analyst | TAM/SAM/SOM, competition, monetization, timing |
| Impact Evaluator | Social, educational, community value |
| Resource Strategist | Cost, timeline, team, bootstrapping viability |
| Innovation Scout | Tech readiness, first-mover advantage, adjacent opportunities |

**Output:** Value Matrix (6 dimensions scored 1-10), Opportunity Score, GO/NO-GO recommendation

### Personal (Council -- 8 Advisors)

| Advisor | Analyzes |
|---------|----------|
| Life Coach | Values alignment, life balance, holistic direction |
| Finance | Runway, budget impact, cash flow, investment risk |
| Health | Burnout risk, physical/mental sustainability |
| Career | Trajectory fit, skill development, positioning |
| Learning | Skill gaps, learning curve, knowledge investment |
| Systems | Time management, workflow impact, capacity |
| Relationships | Family/social impact, collaboration dynamics |
| Creative | Creative fulfillment, innovation satisfaction |

**Output:** Life Impact Assessment, Prioritized Action Plan, Watch List

### Cross-Reference (Meta-Synthesizer)

Maps strategic dimensions to personal dimensions, identifies where they align and where they conflict, and produces:

- **Combined Verdict**: GO / CONDITIONAL GO / NOT NOW / NO-GO
- **Combined Score**: Weighted blend of strategic + personal + alignment
- **Conditions**: Specific, measurable prerequisites for proceeding
- **Narrative**: Mentor-quality advice connecting opportunity to personal reality

## Install

### Via the Marketplace

```
/plugin marketplace add JuanMarchetto/agent-skills
/plugin install full-eval@agent-skills
```

### Via skills.sh

```bash
npx skills add JuanMarchetto/full-eval-skill
```

### Manual

```bash
git clone https://github.com/JuanMarchetto/full-eval-skill.git
cp -r full-eval-skill ~/.claude/skills/full-eval
```

## Dependencies

This skill composes three existing systems. Install them first:

| Dependency | Purpose | Install |
|-----------|---------|---------|
| [architect](https://github.com/JuanMarchetto/architect) | Strategic evaluation (6 evaluators) | Built-in (see architect repo) |
| [council](https://github.com/JuanMarchetto/council) | Personal evaluation (8 advisors) | Built-in (see council repo) |
| pdf-presentation | PDF report generation | Required for PDF output |

The skill degrades gracefully -- if PDF generation is unavailable, results are displayed as formatted text in the terminal.

## Example Verdicts

### GO (Score 8.5/10)
> "Both the market opportunity and your personal situation are strongly aligned. You have 18 months of runway, the technical skills to build an MVP in 6 weeks, and your career trajectory points directly at this space. Proceed with full commitment."

### CONDITIONAL GO (Score 6.8/10)
> "The opportunity scores 7.5/10 but your personal readiness is 5.5/10. Validate for 3 months while employed. Conditions: secure 9 months runway, hit 50 beta users, establish a hard stop date."

### NOT NOW (Score 4.5/10)
> "The idea has merit (6/10) but your current situation makes this the wrong time. Health advisor flags active burnout, Finance shows 2 months runway, and Career advisor notes you are mid-promotion cycle. Revisit in Q3 after addressing personal constraints."

### NO-GO (Score 2.1/10)
> "The market is saturated (Commercial: 3/10), the technology is immature (Technical: 4/10), and your financial situation cannot absorb the risk (Finance: critical). The Innovation Scout found no defensible angle. Redirect energy toward alternatives identified in the Architecture Proposal."

## Files

```
full-eval-skill/
├── SKILL.md                        # Complete guide and protocol
├── agents/
│   └── meta-synthesizer.md         # Cross-references architect + council outputs
├── .claude-plugin/plugin.json      # Plugin metadata
├── README.md                       # This file
├── LICENSE                         # MIT License
└── .gitignore
```

## License

[MIT](LICENSE)
