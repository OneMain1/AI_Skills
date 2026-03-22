---
name: contradiction-finder
description: Identifies and analyzes significant contradictions across research papers - finds mutually exclusive claims and diagnoses root causes of disagreement
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# Contradiction Finder Protocol

This skill systematically identifies genuine contradictions across uploaded research papers and diagnoses why researchers disagree.

## What This Skill Does

When analyzing multiple papers, this skill:

1. **Identifies genuine contradictions** - mutually exclusive claims on the same issue
2. **Documents opposing positions** with specific paper citations
3. **Diagnoses root causes** of disagreement (methodology, data, definitions, etc.)
4. **Excludes false contradictions** - differences in emphasis or scope that aren't true disagreements

## When to Use

- After completing `/research-intake` analysis
- When you notice researchers seem to disagree on key points
- To understand why a field has competing theories
- Before writing a critical literature review section

## How to Use

Invoke this skill with the papers you want to analyze:

```
/contradiction-finder

Analyze contradictions across these 6 papers on [topic]:
[list of papers or paths]
```

## Analysis Instructions

### Step 1: Scan for Genuine Contradictions

Across all papers, identify points where two or more authors make claims that are:
- **Mutually exclusive** - both cannot be true simultaneously
- **About the same phenomenon** - addressing identical research questions or constructs
- **Substantive** - not merely methodological preferences or scope differences

**Exclude**:
- Differences in emphasis (both can be true)
- Different scopes (comparing apples to oranges)
- Methodological preferences without conflicting conclusions
- Nuanced distinctions that don't contradict

### Step 2: Document Each Contradiction

For each genuine contradiction, extract:
1. **Contested Claim** - the specific point of disagreement in one sentence
2. **Position A** - what one paper/author claims (with citation)
3. **Position B** - what the opposing paper/author claims (with citation)
4. **Root Cause** - why they disagree

### Step 3: Diagnose Root Causes

For each contradiction, classify the root cause as one of:

- **Methodology** - different research methods led to different conclusions
- **Dataset** - analyzed different populations, time periods, or samples
- **Time period** - claims true at different historical moments
- **Definition of terms** - using same words for different concepts
- **Other** - specify the unique cause

### Step 4: Prioritize Contradictions

Rank contradictions by significance:
- How central is this to the field's core questions?
- How many papers are involved in the disagreement?
- Does resolving this unlock other questions?

Target: Aim for 5-10 contradictions. If fewer exist, list all you find and note why.

## Important Guidelines

- **Be strict** - only include true contradictions where both positions cannot simultaneously be correct
- **Be specific** - cite exact papers and quote claims when possible
- **Be diagnostic** - identify why researchers reached different conclusions
- **Be comprehensive** - scan the entire paper set, not just abstracts or conclusions
- **Be ranked** - present most significant contradictions first

## Output Format

Use the template to create a structured analysis table.

## Next Steps

After identifying contradictions, consider:
- `/methodology-audit` - Compare research methods that led to contradictory findings
- `/assumption-killer` - Examine if shared assumptions underlie the disagreements
- `/gap-scanner` - Identify what research is needed to resolve contradictions
