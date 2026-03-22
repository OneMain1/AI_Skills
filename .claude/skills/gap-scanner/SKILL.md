---
name: gap-scanner
description: Identifies the 5 most significant research gaps that papers acknowledge, imply, or fail to address - diagnoses why gaps exist and paths to resolution
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# Gap Scanner Protocol

This skill systematically identifies the most significant research gaps across your uploaded papers, diagnoses why those gaps exist, and proposes paths to resolution.

## What This Skill Does

When analyzing your paper collection, this skill:

1. **Identifies the 5 most significant research gaps** from the literature
2. **Diagnoses why each gap exists** (methodological, data, ethical constraints, etc.)
3. **Identifies which paper came closest** to addressing each gap
4. **Proposes paths to resolution** - what's needed to close the gap
5. **Ranks gaps** from most to least significant

## When to Use

- After completing `/research-intake` and `/contradiction-finder`
- When designing a new research project
- Before writing a literature review's "future directions" section
- To identify dissertation or thesis opportunities

## How to Use

Invoke this skill with your papers:

```
/gap-scanner

Identify research gaps across these papers on [topic]:
[list of papers or paths]
```

## Analysis Instructions

### Step 1: Scan for Research Gaps

Based only on the uploaded papers, identify gaps that are:
- **Explicitly acknowledged** - authors state "future research should..."
- **Implicitly suggested** - authors' conclusions raise unanswered questions
- **Conspicuously absent** - obvious questions that no paper addresses

Focus on gaps that are **significant** to the field's development.

### Step 2: Characterize Each Gap

For each of the 5 most significant gaps, document:

#### A. The Gap Statement
- **Unanswered question**: State clearly in 1-2 sentences
- **Why it matters**: Theoretical importance, practical impact, or foundational significance

#### B. Why It Exists
Classify using one of these categories:

- **Methodological barrier** - current methods can't answer it
- **Lack of data** - required data unavailable or uncollected
- **Topic too niche** - insufficient researcher interest or resources
- **Assumed but untested** - taken for granted, never empirically examined
- **Ethical/logistical constraint** - difficult or impossible to study directly
- **Other** - specify unique reason

Provide brief explanation (2-3 sentences) of the specific barrier.

#### C. Closest Paper
- **Which paper came closest** to addressing this gap?
- **Where did it fall short?** (specific limitation that prevented full resolution)

If no paper attempted this, state: "No paper in this set attempted to address this gap."

#### D. Path to Resolution
What would be needed to close this gap?

Specify:
- **Methodology**: What research design or method would work?
- **Data**: What kind of data collection is needed?
- **Resources**: What funding, access, or tools are required?
- **Conceptual work**: What theoretical development needs to happen first?

### Step 3: Rank the Gaps

Order the 5 gaps from most to least significant.

**Ranking criteria** (explain which you're using):
- **Theoretical importance** - resolving it would advance foundational understanding
- **Practical impact** - addressing it would have real-world consequences
- **Feasibility of resolution** - it's solvable with current or near-future methods
- **Bottleneck effect** - it blocks progress on multiple other questions

State your chosen ranking criterion clearly.

### Step 4: Note if Fewer Than 5 Gaps Exist

If the literature reveals fewer than 5 genuine gaps:
- List all you can identify
- Explain why the set is limited (mature field, narrow scope, recent comprehensive review, etc.)

## Important Guidelines

- **Use only uploaded papers** - base gaps on what this specific literature reveals
- **Be specific** - vague gaps like "more research needed" don't count
- **Be honest about feasibility** - some gaps may be fundamentally unresolvable
- **Prioritize significance** - a gap that matters little isn't worth listing
- **Distinguish types** - a methodological barrier is different from lack of interest

## Output Format

Use the template to create a structured gap analysis.

## Next Steps

After identifying gaps, consider:
- `/methodology-audit` - Assess which methods might address the gaps
- `/assumption-killer` - Examine if gaps rest on questionable assumptions
- Design a research proposal to fill the highest-priority gap
