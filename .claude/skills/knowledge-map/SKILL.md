---
name: knowledge-map
description: Creates a structured knowledge map of the literature - identifies central claims, supporting pillars, contested zones, frontier questions, and essential reading list
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# Knowledge Map Builder Protocol

This skill creates a structured visual map of the knowledge landscape in your literature set, organizing it into central claims, well-supported pillars, areas of debate, open questions, and essential papers for newcomers.

## What This Skill Does

When analyzing your paper collection, this skill produces:

1. **Central Claim** - The core proposition unifying the field (or competing centers if divided)
2. **Supporting Pillars** - 3-5 well-established sub-claims with strong evidence
3. **Contested Zones** - 2-3 areas of genuine debate
4. **Frontier Questions** - 1-2 questions the field raises but can't yet answer
5. **Newcomer Reading List** - 3 essential papers with rationale

## When to Use

- After completing `/master-synthesis` and `/citation-chain`
- When onboarding new team members or students to a research area
- Before teaching a seminar or writing a textbook chapter
- To visualize the intellectual structure of a field
- When preparing comprehensive exam materials

## How to Use

Invoke this skill with your papers:

```
/knowledge-map

Create a knowledge map across these papers on [topic]:
[list of papers or paths]
```

## Analysis Instructions

### Presentation Format

**CRITICAL**: Present as a **clean outline**, not prose paragraphs.

Use hierarchical structure:
- Main headings
- Sub-points with bullets
- Citations inline: [Author, Year]
- No narrative paragraphs

### Section 1: Central Claim

**Identify the single proposition that most of this field's work tries to support, challenge, or refine.**

**If there is one unifying center**:
- State it clearly as a declarative proposition
- Note what percentage of papers engage with it
- Explain what makes it central

**If there are competing centers (field is divided)**:
- Name 2 competing central propositions
- Explain the fundamental division
- Note which papers align with which center

**Format**:
```
CENTRAL CLAIM: [Single proposition]
- Engaged by: [X]% of papers
- Why central: [Brief explanation]

OR

COMPETING CENTERS:
  Center A: [Proposition]
    - Supported by: [Paper 1], [Paper 2]
  Center B: [Alternative proposition]
    - Supported by: [Paper 3], [Paper 4]
  Fundamental division: [What they disagree about]
```

### Section 2: Supporting Pillars (3-5)

**Identify well-established sub-claims with strong evidentiary support across multiple papers.**

These are:
- Widely accepted findings
- Robustly supported by evidence
- Treated as building blocks by other research
- Not seriously contested in this literature

**For each pillar**:
- State the claim (one sentence)
- Cite 2+ supporting papers
- Briefly note evidence type (experimental, observational, meta-analytic, etc.)

**Format**:
```
PILLAR 1: [Sub-claim statement]
  - Supported by: [Paper 1], [Paper 2], [Paper 3]
  - Evidence type: [Experimental / Meta-analytic / etc.]

PILLAR 2: [Sub-claim statement]
  - Supported by: [Paper 1], [Paper 2]
  - Evidence type: [Type]
```

### Section 3: Contested Zones (2-3)

**Identify areas of genuine, active disagreement.**

These are:
- Questions where researchers take incompatible positions
- Debates that appear across multiple papers
- Unresolved empirical or theoretical disputes

**For each contested zone**:
- Name the issue being debated
- State Position A vs. Position B (no paper citations here)
- Briefly note what the disagreement hinges on

**Format**:
```
CONTESTED ZONE 1: [Issue being debated]
  - Position A: [What one side argues]
  - Position B: [What the other side argues]
  - Hinge point: [What they fundamentally disagree about]

CONTESTED ZONE 2: [Issue]
  - Position A: [Argument]
  - Position B: [Counter-argument]
  - Hinge point: [Core disagreement]
```

### Section 4: Frontier Questions (1-2)

**Questions this literature raises but cannot yet answer.**

These are:
- Explicitly posed as open questions in papers
- Implied by limitations or gaps in current work
- Represent the boundaries of current knowledge

**Format as explicit questions**:
```
FRONTIER QUESTION 1: [Specific question that papers raise but don't answer?]
  - Why unanswered: [Methodological / empirical / theoretical barrier]

FRONTIER QUESTION 2: [Specific question?]
  - Why unanswered: [Barrier]
```

### Section 5: Newcomer Reading List (3 papers)

**The 3 papers a newcomer should read first to understand this field.**

**Selection criteria**:
- Foundational to the field (not just most cited)
- Covers essential concepts or methods
- Accessible and well-written
- Provides necessary background for other papers

**For each paper**:
- Full citation: [Author, Year] - [Title]
- Why to read this first (one sentence)

**Format**:
```
NEWCOMER READING LIST:

1. [Author, Year] - [Paper title]
   - Why read this: [One sentence explaining its foundational role]

2. [Author, Year] - [Paper title]
   - Why read this: [One sentence]

3. [Author, Year] - [Paper title]
   - Why read this: [One sentence]
```

## Important Guidelines

- **No prose paragraphs** - use outline format throughout
- **Be hierarchical** - use clear visual structure
- **Be selective** - 3-5 pillars, not 10; 2-3 contested zones, not 7
- **Cite evidence** - every pillar needs 2+ paper citations
- **Be newcomer-focused** - reading list should be genuinely accessible, not exhaustive
- **Be structural** - map the intellectual architecture, not every detail

## Output Format

Use the template to create the knowledge map outline.

## Next Steps

After creating the knowledge map:
- Use it to orient new researchers or students
- Identify where your work fits in the map
- Use contested zones and frontier questions to motivate new research
- Share with colleagues to validate or debate the structure
