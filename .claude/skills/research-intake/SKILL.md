---
name: research-intake
description: Initial analysis of multiple research papers - creates paper inventory, clusters papers by theoretical framework, and identifies contradictions
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# Research Intake Protocol

This skill performs the initial comprehensive analysis when you upload multiple research papers on a topic. It creates a structured foundation for deeper analysis by organizing papers, identifying theoretical clusters, and flagging contradictions.

## What This Skill Does

When you provide multiple papers on a topic, this skill will:

1. **Create a paper inventory table** with Author(s), Year, and Core Claim (≤20 words)
2. **Group papers into 2-5 theoretical clusters** based on shared assumptions or frameworks
3. **Flag direct contradictions** where papers make mutually exclusive claims

## When to Use

- At the start of a literature review
- When you have 3+ papers on the same topic
- Before conducting deeper analysis with other research skills
- To quickly orient yourself in a new research domain

## How to Use

Simply invoke this skill and provide:
- The number of papers you're analyzing
- The research topic
- Paths to PDF files, URLs, or text excerpts from each paper

Example:
```
/research-intake

I have 5 papers on neural network interpretability:
1. [path/to/paper1.pdf]
2. [path/to/paper2.pdf]
...
```

## Analysis Instructions

When this skill is invoked, perform the following tasks in order:

### Task 1: Paper Inventory Table

Create a table with these columns:
- **Author(s)**: Last name(s) of author(s)
- **Year**: Publication year
- **Core Claim**: One sentence summary (≤20 words) of the main thesis

If a paper has no explicit thesis, infer the central argument from its conclusions.

### Task 2: Theoretical Clustering

Group the papers into 2–5 clusters based on:
- Shared theoretical assumptions
- Common frameworks or methodologies
- Similar research paradigms

For each cluster:
1. **Name the cluster** (2-4 words)
2. **Explain what unites papers** in 1-2 sentences
3. **List which papers belong** to this cluster

### Task 3: Contradiction Identification

Identify and list any **direct contradictions** where:
- Two or more authors make mutually exclusive claims
- The claims are about the same phenomenon
- The disagreement is substantive (not just methodological)

Format each contradiction as:
- **Paper A vs. Paper B** — [contested claim in one sentence]

## Important Guidelines

- **Focus only on the three tasks above** - do not provide individual paper summaries
- **Be precise** - only flag genuine contradictions, not differences in scope or emphasis
- **Infer when needed** - if a paper's thesis is implicit, derive it from conclusions
- **Keep claims concise** - core claims must be ≤20 words
- **Name clusters meaningfully** - use descriptive names that capture theoretical unity

## Output Format

The skill will use the template file to structure the analysis.

## Next Steps

After completing this intake analysis, consider using:
- `/contradiction-finder` - For deeper analysis of disagreements
- `/citation-chain` - To trace conceptual lineage
- `/gap-scanner` - To identify research gaps
- `/master-synthesis` - To synthesize the entire literature
