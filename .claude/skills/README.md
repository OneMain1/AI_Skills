# Research Paper Analysis Skills

A comprehensive suite of 9 Claude Code skills for systematic literature review and research paper analysis.

## Overview

These skills transform how you analyze academic literature by providing structured protocols for every stage of research review - from initial intake to final synthesis.

### What Are These Skills?

Each skill is a specialized analysis protocol that Claude Code can execute on your research papers. They're designed to work individually or as a complete workflow for comprehensive literature review.

### Quick Start

1. Upload or provide paths to your research papers
2. Invoke skills using `/skill-name` commands
3. Receive structured analysis following rigorous academic protocols

---

## The 9 Research Skills

### 1. Research Intake (`/research-intake`)

**What it does**: Initial comprehensive analysis when you upload multiple papers
- Creates paper inventory table (Author, Year, Core Claim)
- Groups papers into 2-5 theoretical clusters
- Identifies direct contradictions between papers

**When to use**:
- Start of any literature review
- When you have 3+ papers on the same topic
- Before deeper analysis with other skills

**Output**: Structured intake report with paper table, clusters, and contradictions

---

### 2. Contradiction Finder (`/contradiction-finder`)

**What it does**: Systematically identifies genuine contradictions across papers
- Finds mutually exclusive claims on the same issue
- Documents opposing positions with citations
- Diagnoses root causes of disagreement (methodology, data, definitions, etc.)

**When to use**:
- After `/research-intake` analysis
- When researchers seem to disagree on key points
- To understand competing theories in a field

**Output**: Detailed contradiction table with root cause analysis

---

### 3. Citation Chain (`/citation-chain`)

**What it does**: Traces intellectual history of key concepts
- Identifies 3 most frequently referenced concepts
- Maps who introduced, challenged, and refined each concept
- Assesses current status (settled, contested, or evolving)

**When to use**:
- After `/research-intake`
- When writing theoretical framework sections
- To understand how ideas developed over time

**Output**: Conceptual genealogy showing evolution of ideas

---

### 4. Gap Scanner (`/gap-scanner`)

**What it does**: Identifies the 5 most significant research gaps
- Documents what's acknowledged, implied, or conspicuously absent
- Diagnoses why gaps exist (methodology, data, ethics, etc.)
- Proposes paths to resolution

**When to use**:
- When designing new research projects
- Before writing "future directions" sections
- To identify dissertation opportunities

**Output**: Ranked gap analysis with resolution pathways

---

### 5. Methodology Audit (`/methodology-audit`)

**What it does**: Compares research methodologies across papers
- Classifies each paper's methodology, data source, sample size
- Identifies dominant and absent methodologies
- Critiques weakest methodology using rigorous criteria

**When to use**:
- After `/research-intake`
- When evaluating methodological rigor
- Before designing your own study methodology

**Output**: Methodology comparison table with critical assessment

---

### 6. Master Synthesis (`/master-synthesis`)

**What it does**: Creates 400-word synthesis of entire literature
- Established consensus (~100 words)
- Active debates (~100 words)
- Strongest evidence (~100 words)
- Key open question (~80 words)

**When to use**:
- After completing most other analyses
- When writing literature review synthesis sections
- To get bird's-eye view of research area

**Output**: Concise academic synthesis writing across all papers

---

### 7. Assumption Killer (`/assumption-killer`)

**What it does**: Identifies untested assumptions most papers share
- Finds 5-8 foundational assumptions never tested
- Assesses risk level (what collapses if assumption is false)
- Predicts consequences of assumption being wrong

**When to use**:
- After `/master-synthesis`
- When critically evaluating a paradigm
- To identify high-impact research opportunities

**Output**: Ranked assumption analysis with risk assessment

---

### 8. Knowledge Map (`/knowledge-map`)

**What it does**: Creates structured knowledge map of the literature
- Central claims (what unifies the field)
- Supporting pillars (3-5 well-established sub-claims)
- Contested zones (2-3 areas of debate)
- Frontier questions (1-2 unanswered questions)
- Newcomer reading list (3 essential papers)

**When to use**:
- After `/master-synthesis` and `/citation-chain`
- When onboarding new team members
- To visualize intellectual structure of field

**Output**: Hierarchical outline of knowledge landscape

---

### 9. So What Test (`/so-what-test`)

**What it does**: Summarizes research in 3 points for non-experts
1. What has been proven (no hedging, stated as fact)
2. What is still unknown (honest about gaps)
3. Why it matters (real-world or theoretical impact)

**When to use**:
- When explaining research to non-specialists
- For grant "broader impacts" sections
- Before presenting to non-academic audiences

**Output**: Plain-language 3-point summary (~150-200 words)

---

## Recommended Workflows

### Complete Literature Review Workflow

For comprehensive literature analysis, use skills in this order:

```
1. /research-intake          → Get organized
2. /methodology-audit        → Understand methods
3. /contradiction-finder     → Identify disagreements
4. /citation-chain          → Trace conceptual history
5. /gap-scanner             → Find research opportunities
6. /assumption-killer       → Examine hidden foundations
7. /master-synthesis        → Write synthesis
8. /knowledge-map           → Visualize structure
9. /so-what-test            → Create public summary
```

**Time investment**: 2-3 hours for 10-15 papers
**Output**: Complete literature review foundation

---

### Quick Review Workflow

For rapid orientation in a new field:

```
1. /research-intake    → Inventory and clusters
2. /knowledge-map      → Structural overview
3. /so-what-test       → Bottom-line takeaway
```

**Time investment**: 30-45 minutes
**Output**: Solid foundation for deeper reading

---

### Critical Analysis Workflow

For evaluating research quality and finding weaknesses:

```
1. /methodology-audit      → Assess rigor
2. /contradiction-finder   → Find disagreements
3. /assumption-killer      → Expose untested assumptions
```

**Time investment**: 1-2 hours
**Output**: Critical evaluation suitable for peer review

---

### Research Design Workflow

For identifying what to study next:

```
1. /gap-scanner           → Find research gaps
2. /assumption-killer     → Identify testable assumptions
3. /contradiction-finder  → Find debates to resolve
```

**Time investment**: 1 hour
**Output**: Multiple research project ideas with justification

---

## Skills That Work Well Together

### Complementary Pairs

- **`/research-intake` + `/knowledge-map`**: Organize then visualize
- **`/contradiction-finder` + `/methodology-audit`**: Understand why researchers disagree
- **`/gap-scanner` + `/assumption-killer`**: Find what to study next
- **`/master-synthesis` + `/so-what-test`**: Academic + public summaries
- **`/citation-chain` + `/knowledge-map`**: Historical + structural views

### Sequential Dependencies

Some skills benefit from being run after others:

- Run `/research-intake` before any other skill
- Run `/master-synthesis` before `/assumption-killer`
- Run `/citation-chain` before `/knowledge-map`
- Run most analytical skills before `/so-what-test`

---

## Tips for Best Results

### Prepare Your Papers

**Supported formats**:
- PDF files (most common)
- Text excerpts
- URLs to papers (if accessible)

**Recommended paper count**:
- Minimum: 3-5 papers (for meaningful patterns)
- Optimal: 8-15 papers (comprehensive without overwhelm)
- Maximum: 20-30 papers (still manageable)

### Invoke Skills Effectively

**Good invocation**:
```
/gap-scanner

Identify research gaps across these 8 papers on transformer interpretability:
1. /path/to/paper1.pdf
2. /path/to/paper2.pdf
...
```

**Also acceptable**:
```
/gap-scanner

I've uploaded 8 papers on transformer interpretability in our previous conversation.
Please identify research gaps across all of them.
```

### Customize Analysis Depth

Most skills can be adapted:
- Ask for more/fewer items (e.g., "identify 10 contradictions instead of 5-10")
- Request focus on specific aspects (e.g., "focus on methodology contradictions")
- Specify output format preferences (e.g., "create a visual diagram")

---

## Understanding Skill Outputs

### File Structure

Each skill generates outputs in this structure:

```
skill-name/
├── SKILL.md          # Skill instructions and protocol
└── template.md       # Output template/structure
```

### Output Locations

Skill outputs are provided directly in the conversation. To save them:
1. Copy the output to a file
2. Use the template as a guide for your own writing
3. Export conversation to preserve analysis

### Interpreting Results

**High-confidence findings**:
- Supported by multiple papers
- Methodologically robust
- Explicitly stated in papers

**Tentative findings**:
- Inferred from implicit evidence
- Based on limited papers
- Requires assumption

Skills will note confidence level when relevant.

---

## Skill Customization

### Modifying Skills

Each skill's `SKILL.md` file can be edited to:
- Adjust analysis criteria
- Change output format
- Add domain-specific requirements
- Modify ranking algorithms

**Location**: `.claude/skills/skill-name/SKILL.md`

### Creating Templates

Each skill's `template.md` can be customized to:
- Match your preferred formatting
- Add institutional requirements
- Include additional sections
- Adjust verbosity

**Location**: `.claude/skills/skill-name/template.md`

---

## Troubleshooting

### Common Issues

**Issue**: Skill doesn't recognize uploaded papers
- **Solution**: Explicitly provide file paths or paste excerpts

**Issue**: Analysis seems shallow or generic
- **Solution**: Ensure papers are on the same specific topic; provide more context

**Issue**: Output doesn't follow template exactly
- **Solution**: Claude adapts templates to available evidence; some sections may be N/A

**Issue**: Skill takes too long
- **Solution**: Reduce number of papers or use Quick Review Workflow

### Getting Better Results

**Improve analysis quality**:
1. Use papers on focused topics (not broad surveys)
2. Provide 8-15 papers (not too few, not too many)
3. Include diverse perspectives (different authors, years, methods)
4. Give context about your research goals

**Improve output formatting**:
1. Specify desired format in your invocation
2. Ask for revisions if output doesn't meet needs
3. Customize templates for consistent formatting

---

## Advanced Usage

### Combining Skills with Other Tools

These research skills integrate well with:

**Git workflows**:
- Commit analysis outputs to version control
- Track how literature understanding evolves
- Collaborate with team on interpretations

**Writing workflows**:
- Export outputs to Markdown files
- Use synthesis sections in draft papers
- Generate literature review outlines

**Research workflows**:
- Link gaps to project proposals
- Use contradiction analysis in grant motivation
- Reference assumption analysis in methods sections

### Automating Workflows

Create custom slash commands that chain multiple skills:

Example `.claude/commands/full-review.md`:
```markdown
---
description: Complete literature review workflow
---

Run these skills in sequence:
1. /research-intake
2. /methodology-audit
3. /contradiction-finder
4. /master-synthesis
5. /knowledge-map
```

---

## Best Practices

### For Literature Reviews

1. **Start with `/research-intake`** - Always organize first
2. **Use multiple perspectives** - Run 3-4 complementary skills
3. **Document as you go** - Save outputs immediately
4. **Iterate** - Re-run skills as you add papers

### For Research Design

1. **Identify gaps early** - Run `/gap-scanner` first
2. **Check assumptions** - Use `/assumption-killer` to find high-impact questions
3. **Understand methods** - Use `/methodology-audit` to avoid past mistakes
4. **Test feasibility** - Ensure gaps are actually resolvable

### For Teaching & Mentoring

1. **Onboard students** - Use `/knowledge-map` and `/so-what-test`
2. **Critical thinking** - Use `/assumption-killer` to teach questioning
3. **Methodology** - Use `/methodology-audit` to teach research design
4. **Writing** - Use `/master-synthesis` as model synthesis

---

## Skill Comparison Matrix

| Skill | Analysis Type | Output Format | Time | Depth | Audience |
|-------|--------------|---------------|------|-------|----------|
| research-intake | Organizational | Tables + lists | 15 min | Surface | Researchers |
| contradiction-finder | Critical | Table + analysis | 30 min | Deep | Researchers |
| citation-chain | Historical | Timeline outline | 30 min | Deep | Researchers |
| gap-scanner | Opportunity | Ranked list | 45 min | Deep | Researchers |
| methodology-audit | Evaluative | Comparison table | 45 min | Deep | Researchers |
| master-synthesis | Synthetic | Prose (400 words) | 30 min | Medium | Researchers |
| assumption-killer | Critical | Ranked analysis | 45 min | Very deep | Researchers |
| knowledge-map | Structural | Hierarchical outline | 30 min | Medium | All |
| so-what-test | Communicative | 3-point summary | 15 min | Surface | Non-experts |

---

## Contributing

### Improving Skills

To enhance these skills:
1. Edit `SKILL.md` files to refine protocols
2. Update `template.md` files for better outputs
3. Add examples in `examples/` folders
4. Document improvements in this README

### Sharing Enhancements

If you improve these skills:
- Commit changes to git
- Share with collaborators
- Document why changes improve analysis

---

## Credits

These research analysis protocols are based on established academic literature review methodologies, adapted for systematic execution by Claude Code.

**Skill developers**: [Your name/team]
**Created**: [Date]
**Last updated**: [Date]

---

## Getting Help

### Documentation

- Each skill's `SKILL.md` contains detailed instructions
- Templates show expected output format
- This README provides workflow guidance

### Support

For issues or questions:
1. Check individual skill documentation
2. Review troubleshooting section above
3. Consult Claude Code documentation: https://code.claude.com/docs

---

## Version History

**v1.0** - Initial release
- 9 core research analysis skills
- Complete workflow support
- Template-based outputs

---

## License

[Specify license if applicable]

---

## Quick Reference Card

```
QUICK SKILL REFERENCE

Initial Organization:
  /research-intake        → Inventory, clusters, contradictions

Deep Analysis:
  /methodology-audit      → Compare research methods
  /contradiction-finder   → Identify disagreements
  /citation-chain        → Trace concept evolution
  /gap-scanner           → Find research opportunities
  /assumption-killer     → Expose hidden assumptions

Synthesis & Communication:
  /master-synthesis      → 400-word academic synthesis
  /knowledge-map         → Structural outline
  /so-what-test          → Plain-language summary

Recommended first use: /research-intake
Recommended for grants: /gap-scanner + /so-what-test
Recommended for critical review: /methodology-audit + /assumption-killer
```
