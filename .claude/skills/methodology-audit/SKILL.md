---
name: methodology-audit
description: Compares research methodologies across papers - classifies approaches, identifies dominant methods, spots absent methodologies, and finds weakest designs
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# Methodology Audit Protocol

This skill systematically compares and evaluates the research methodologies used across your uploaded papers, identifying patterns, gaps, and weaknesses in how the field conducts research.

## What This Skill Does

When analyzing your paper collection, this skill:

1. **Classifies each paper's methodology** in a structured table
2. **Identifies the most frequent methodology type** and explains why
3. **Spots absent or rare methodologies** that could benefit the field
4. **Critiques the weakest methodology** using rigorous evaluation criteria

## When to Use

- After completing `/research-intake` analysis
- When evaluating the methodological rigor of a research area
- Before designing your own study methodology
- When writing a methods-focused literature review
- To understand why `/contradiction-finder` revealed disagreements

## How to Use

Invoke this skill with your papers:

```
/methodology-audit

Compare methodologies across these papers on [topic]:
[list of papers or paths]
```

## Analysis Instructions

### Step 1: Classification Table

Create a table with these columns for each paper:

| Paper (Author, Year) | Methodology Type | Data Source | Sample Size | Key Limitation |
|---------------------|------------------|-------------|-------------|----------------|

**Methodology Type** - Use the best-fitting category:

Common types include:
- Survey
- Experiment (RCT - Randomized Controlled Trial)
- Quasi-experiment
- Simulation / Computational modeling
- Meta-analysis
- Case study
- Machine learning / Computational
- Literature review / Systematic review
- Ethnography / Qualitative fieldwork
- Secondary data analysis
- Mixed methods

**Important**: Don't force papers into these categories. Add new methodology types as needed.

**Data Source**:
- Where did the data come from? (e.g., "Online survey, MTurk," "Clinical trial participants," "Public dataset: ImageNet," "Archival records")

**Sample Size**:
- Report if stated (e.g., "N=347," "50 interviews," "1.2M images")
- If not applicable or not stated, write "N/A" or "Not reported"

**Key Limitation**:
- What limitation did the authors explicitly acknowledge?
- If they noted multiple limitations, choose the most methodologically significant one

### Step 2: Synthesis Analysis

Answer these questions based on the classification table:

#### A. Most Frequent Methodology

**Which methodology type appears most often?**
- Count occurrences
- Identify the dominant approach

**Why is this method dominant?**
Suggest reasons based on papers' stated rationale, such as:
- Nature of research questions (exploratory vs. confirmatory)
- Practical constraints (access to populations, ethical issues)
- Field conventions or traditions
- Technological availability
- Cost and resource efficiency

#### B. Absent or Rare Methodologies

**Which methodologies are missing or rare despite being relevant?**

Consider:
- Are there questions being asked that would benefit from experiments, but everyone uses surveys?
- Could qualitative methods complement the quantitative work?
- Would simulations help test theories that are hard to study empirically?
- Are there newer computational methods not yet adopted?

Explain:
- What methodology is absent
- Why it would be useful for the research questions in this field
- Potential reasons it hasn't been used

### Step 3: Weakest Methodology Critique

Identify the paper whose methodology is most vulnerable to criticism.

**Evaluation criteria**:

1. **Sample size adequacy**
   - Is the sample large enough for statistical power?
   - Is it sufficient for the claims being made?

2. **Control for confounds**
   - Are alternative explanations ruled out?
   - Are there obvious confounding variables not addressed?

3. **Replicability**
   - Could another researcher replicate this study?
   - Is the procedure described in sufficient detail?

4. **Transparency of reporting**
   - Are methods clearly documented?
   - Are data and materials available or described?

**Identify**:
- Which paper has the weakest methodology
- Which criterion it fails most clearly
- Specific evidence of the weakness
- How this weakness affects the validity of conclusions

**Be fair**: Focus on methodological design issues, not just resource constraints.

## Important Guidelines

- **Be accurate** - classify methodologies based on actual design, not paper titles
- **Be comprehensive** - include all papers in the classification table
- **Be specific** - vague critiques like "small sample" need context (small for what purpose?)
- **Be constructive** - identify weaknesses to improve future research, not to dismiss work
- **Be evidence-based** - cite specific features of methods when evaluating

## Output Format

Use the template to create a structured methodology comparison.

## Next Steps

After auditing methodologies, consider:
- `/contradiction-finder` - Check if methodological differences explain contradictions
- `/gap-scanner` - Identify if absent methodologies create research gaps
- Use insights to design a methodologically stronger study
