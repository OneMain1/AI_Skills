# Claude Skills Collection

A comprehensive library of specialized analysis skills for Claude Code, organized by domain.

## Overview

This repository contains two major skill suites:
- **Research Paper Analysis** (9 skills) - Academic literature review and synthesis
- **Investment Analysis** (10 skills) - Financial analysis following institutional frameworks

---

## Skill Categories

### 1. Research Paper Analysis

Systematic protocols for academic literature review, from initial intake to synthesis.

| Skill | Purpose | Output | Use When |
|-------|---------|--------|----------|
| `research-intake` | Initial paper organization | Inventory table + clusters | Starting any literature review |
| `contradiction-finder` | Identify disagreements | Contradiction analysis | Papers seem to conflict |
| `citation-chain` | Trace concept evolution | Conceptual genealogy | Understanding idea development |
| `gap-scanner` | Find research opportunities | Ranked gap analysis | Designing new research |
| `methodology-audit` | Compare research methods | Methodology comparison | Evaluating research rigor |
| `master-synthesis` | Synthesize literature | 400-word synthesis | Writing lit review |
| `assumption-killer` | Expose untested assumptions | Assumption risk analysis | Critical paradigm evaluation |
| `knowledge-map` | Visualize field structure | Hierarchical outline | Onboarding or teaching |
| `so-what-test` | Plain-language summary | 3-point summary | Explaining to non-experts |

**Detailed documentation**: `.claude/skills/README.md`

---

### 2. Investment Analysis

Institutional-grade financial analysis following frameworks from top investment firms.

| Skill | Institution Style | Purpose | Output | Use When |
|-------|------------------|---------|--------|----------|
| `goldman-stock-screener` | Goldman Sachs | Screen stocks by criteria | Top 10 stocks + metrics | Building watchlist |
| `morgan-dcf-valuation` | Morgan Stanley | Value companies via DCF | Intrinsic value estimate | Assessing fair value |
| `bridgewater-risk-analysis` | Bridgewater | Analyze portfolio risk | Risk assessment report | Managing portfolio risk |
| `jpmorgan-earnings-analysis` | JPMorgan | Earnings preview/review | Pre-earnings brief | Before earnings reports |
| `blackrock-portfolio-construction` | BlackRock | Build custom portfolios | Asset allocation plan | Creating new portfolio |
| `citadel-technical-analysis` | Citadel | Technical chart analysis | Trade setup report | Timing entries/exits |
| `harvard-dividend-strategy` | Harvard Endowment | Dividend income portfolio | Dividend stock portfolio | Generating passive income |
| `bain-competitive-analysis` | Bain & Company | Sector competitive analysis | Competitive landscape | Comparing companies |
| `renaissance-pattern-finder` | Renaissance Tech | Find statistical patterns | Pattern analysis | Finding market edges |
| `mckinsey-macro-analysis` | McKinsey | Macro impact assessment | Economic impact report | Understanding macro trends |

**Detailed documentation**: `.claude/skills/INVESTMENT_README.md`

---

## Skill Relationships

### Research Paper Analysis Workflow

```
Entry Point:
  research-intake
      ↓
  ┌───┴────────────────┬─────────────────┐
  ↓                    ↓                 ↓
methodology-audit  citation-chain  contradiction-finder
  ↓                    ↓                 ↓
  └────────┬───────────┴─────────────────┘
           ↓
     gap-scanner + assumption-killer
           ↓
     master-synthesis
           ↓
     ┌────┴────┐
     ↓         ↓
knowledge-map  so-what-test
```

**Key Dependencies:**
- Run `research-intake` first (foundation for all others)
- Run `master-synthesis` before `assumption-killer`
- Run `citation-chain` before `knowledge-map`

---

### Investment Analysis Workflows

#### Complete Stock Research Workflow
```
Fundamental Analysis:
  goldman-stock-screener → morgan-dcf-valuation
                              ↓
  bain-competitive-analysis → Investment Decision
                              ↓
Technical Analysis:
  citadel-technical-analysis → Entry/Exit Timing
                              ↓
Risk Management:
  bridgewater-risk-analysis → Position Sizing
```

#### Earnings Season Workflow
```
jpmorgan-earnings-analysis (pre-earnings)
          ↓
citadel-technical-analysis (options positioning)
          ↓
[Earnings Report]
          ↓
goldman-stock-screener (re-screen if needed)
```

#### Portfolio Construction Workflow
```
mckinsey-macro-analysis (understand environment)
          ↓
goldman-stock-screener (find candidates)
          ↓
morgan-dcf-valuation (value each candidate)
          ↓
bain-competitive-analysis (compare alternatives)
          ↓
blackrock-portfolio-construction (build allocation)
          ↓
bridgewater-risk-analysis (assess portfolio risk)
          ↓
harvard-dividend-strategy (if income focus)
```

#### Income Investing Workflow
```
harvard-dividend-strategy (build dividend portfolio)
          ↓
goldman-stock-screener (screen for safety)
          ↓
bridgewater-risk-analysis (check concentration risk)
          ↓
mckinsey-macro-analysis (assess rate environment)
```

---

## Cross-Domain Applications

While designed for separate domains, these skill suites can complement each other:

### Analyzing Investment Research Papers
Use **research skills** to analyze financial research:
- `research-intake` → Organize sell-side research reports
- `contradiction-finder` → Find conflicting analyst opinions
- `methodology-audit` → Compare valuation approaches
- `master-synthesis` → Synthesize investment thesis

### Academic Study of Investment Strategies
Use **investment skills** on academic finance papers:
- Run `morgan-dcf-valuation` on companies studied in papers
- Use `bain-competitive-analysis` to validate paper findings
- Apply `renaissance-pattern-finder` to test academic hypotheses

---

## Quick Start Guide

### For Academic Research
1. Upload 5-15 papers on a topic
2. Run `/research-intake` to organize
3. Choose specialized skills based on your goal:
   - Writing lit review → `master-synthesis` + `knowledge-map`
   - Finding research gaps → `gap-scanner` + `assumption-killer`
   - Critical analysis → `methodology-audit` + `contradiction-finder`

### For Investment Analysis
1. Identify your analysis goal (stock pick, portfolio, timing, etc.)
2. Choose appropriate workflow from above
3. Customize prompts with your specific:
   - Investment amount
   - Risk tolerance
   - Time horizon
   - Sector preferences

---

## Skill Invocation Format

All skills use consistent invocation:

```
/skill-name

[Your specific request and parameters]
```

Example:
```
/goldman-stock-screener

Screen for technology stocks with:
- Market cap > $10B
- P/E < sector average
- Revenue growth > 15%
- Strong balance sheet
```

---

## Customization

### Modifying Existing Skills

Each skill can be customized by editing:
- `SKILL.md` - Analysis protocol and instructions
- `template.md` - Output format structure

Location: `.claude/skills/[skill-name]/`

### Creating New Skills

To add a new skill:
1. Create folder: `.claude/skills/new-skill-name/`
2. Add `SKILL.md` with frontmatter and instructions
3. Add `template.md` with output structure
4. Update this file and relevant README

---

## Skill Metadata

### Research Paper Analysis Skills
- **Total**: 9 skills
- **Domain**: Academic research
- **Input**: PDF papers, text excerpts
- **Output**: Structured analysis reports
- **Typical workflow time**: 30 min - 3 hours
- **Best for**: Graduate students, researchers, academics

### Investment Analysis Skills
- **Total**: 10 skills
- **Domain**: Financial markets
- **Input**: Ticker symbols, portfolio holdings, financial goals
- **Output**: Investment research reports
- **Typical workflow time**: 15 min - 2 hours
- **Best for**: Individual investors, analysts, portfolio managers

---

## File Structure

```
.claude/
├── claude.md                          # This file - master index
├── skills/
│   ├── README.md                      # Research skills documentation
│   ├── INVESTMENT_README.md           # Investment skills documentation
│   │
│   ├── research-intake/               # Research skills
│   │   ├── SKILL.md
│   │   └── template.md
│   ├── contradiction-finder/
│   ├── citation-chain/
│   ├── gap-scanner/
│   ├── methodology-audit/
│   ├── master-synthesis/
│   ├── assumption-killer/
│   ├── knowledge-map/
│   ├── so-what-test/
│   │
│   ├── goldman-stock-screener/        # Investment skills
│   │   ├── SKILL.md
│   │   └── template.md
│   ├── morgan-dcf-valuation/
│   ├── bridgewater-risk-analysis/
│   ├── jpmorgan-earnings-analysis/
│   ├── blackrock-portfolio-construction/
│   ├── citadel-technical-analysis/
│   ├── harvard-dividend-strategy/
│   ├── bain-competitive-analysis/
│   ├── renaissance-pattern-finder/
│   └── mckinsey-macro-analysis/
```

---

## Best Practices

### General Guidelines
1. **Read documentation** - Each skill has detailed usage instructions
2. **Follow workflows** - Use recommended sequences for best results
3. **Customize freely** - Adapt skills to your specific needs
4. **Iterate** - Re-run skills as you gather more information

### Research Skills
- Always start with `/research-intake`
- Use 8-15 papers for optimal results
- Papers should be on focused topics
- Save outputs as you go

### Investment Skills
- Never invest based solely on AI analysis
- Verify all financial data independently
- Understand your risk tolerance first
- Use multiple skills for complete picture
- Consult licensed financial advisors for major decisions

---

## Limitations & Disclaimers

### Research Skills
- Analysis quality depends on paper quality and quantity
- Cannot access paywalled content without provided access
- Interpretations may miss domain-specific nuances
- Not a replacement for expert human review

### Investment Skills
- **Not financial advice** - For educational purposes only
- Cannot predict future market performance
- Relies on historical data and public information
- Cannot replace professional financial advisors
- Past performance does not guarantee future results
- You are responsible for your investment decisions

---

## Version History

**v2.0** - Current
- Added 10 investment analysis skills
- Created master claude.md index
- Added cross-domain workflows
- Updated documentation structure

**v1.0** - Initial
- 9 research paper analysis skills
- Research-focused documentation

---

## Getting Help

### Documentation
- Master index: `.claude/claude.md` (this file)
- Research skills: `.claude/skills/README.md`
- Investment skills: `.claude/skills/INVESTMENT_README.md`
- Individual skills: `.claude/skills/[skill-name]/SKILL.md`

### Support
- Claude Code docs: https://code.claude.com/docs
- Skill customization: Edit SKILL.md files
- Issues: Check troubleshooting in README files

---

## Contributing

To add or improve skills:
1. Follow existing skill structure (SKILL.md + template.md)
2. Add proper frontmatter metadata
3. Document in relevant README
4. Update this master index
5. Test thoroughly before committing

---

## Quick Reference

```
RESEARCH SKILLS          INVESTMENT SKILLS
━━━━━━━━━━━━━━━━━━━━━   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Start Here:              Screening & Valuation:
  /research-intake         /goldman-stock-screener
                           /morgan-dcf-valuation
Analysis:
  /methodology-audit     Risk & Portfolio:
  /contradiction-finder    /bridgewater-risk-analysis
  /citation-chain          /blackrock-portfolio-construction
  /gap-scanner
  /assumption-killer     Trading & Timing:
                           /citadel-technical-analysis
Synthesis:                 /jpmorgan-earnings-analysis
  /master-synthesis
  /knowledge-map         Strategy & Research:
  /so-what-test            /harvard-dividend-strategy
                           /bain-competitive-analysis
                           /renaissance-pattern-finder
                           /mckinsey-macro-analysis
```

---

*Last updated: March 2026*
