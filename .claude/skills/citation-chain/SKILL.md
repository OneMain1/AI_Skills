---
name: citation-chain
description: Traces the intellectual history of key concepts across papers - identifies who introduced, challenged, and refined major ideas in the literature
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# Citation Chain Protocol

This skill traces the intellectual genealogy of key concepts across your uploaded papers, showing how ideas originate, get challenged, and evolve over time.

## What This Skill Does

When analyzing your paper collection, this skill:

1. **Identifies the 3 most frequently referenced concepts** across papers
2. **Traces each concept's history** within your literature set
3. **Maps intellectual lineage** - who introduced it, who challenged it, who refined it
4. **Assesses current status** - is the concept settled, contested, or evolving?

## When to Use

- After completing `/research-intake` analysis
- When you want to understand how key ideas developed
- Before writing a theoretical framework section
- To identify foundational vs. emerging concepts in a field

## How to Use

Invoke this skill with your papers:

```
/citation-chain

Trace conceptual history across these papers on [topic]:
[list of papers or paths]
```

## Analysis Instructions

### Step 1: Identify Top 3 Concepts

Scan all papers to find the 3 concepts that appear most frequently, defined as:
- **Named explicitly** by multiple authors
- **Debated or discussed** across papers (not just mentioned)
- **Built upon or referenced** as foundational to arguments

Examples of concepts: "working memory," "social capital," "algorithmic fairness," "attention mechanism"

### Step 2: Trace Each Concept's Intellectual History

For each of the 3 concepts, use only evidence from the uploaded papers to answer:

#### A. Origin
- **Who first introduced or defined this concept** within this paper set?
- **How was it originally defined?** (1-2 sentence summary)
- **What problem was it meant to solve?**

#### B. Challenge
- **Which paper(s) questioned or challenged the concept?**
- **What was the nature of the challenge?** (methodological doubt, conceptual critique, empirical disconfirmation)
- **How serious was the challenge?** (minor refinement vs. fundamental questioning)

If no paper challenged it, state: "No challenges identified in this literature set."

#### C. Refinement
- **Which paper(s) modified or extended the concept?**
- **What changes were made?** (narrowed scope, added dimensions, integrated with other concepts)
- **Did the refinement gain acceptance across papers?**

If no refinement occurred, state: "No refinements identified in this literature set."

#### D. Current Status
Based solely on evidence in these papers, classify as:

- **Settled** - widely accepted, no active debate, used consistently
- **Contested** - active disagreement about definition, validity, or application
- **Evolving** - undergoing refinement, new dimensions being added, applications expanding

Justify your classification with specific evidence from papers.

### Step 3: Visualize the Chain

For each concept, create a timeline-style outline:

```
Concept → Challenge → Refinement → Current Status
[Origin paper] → [Challenger] → [Refiner] → [Assessment]
```

## Important Guidelines

- **Use only uploaded papers** - do not guess or infer from outside knowledge
- **Be evidence-based** - cite specific papers for each claim about origin/challenge/refinement
- **State what's missing** - if a concept lacks a clear challenger or refinement, say so explicitly
- **Focus on substance** - track conceptual evolution, not just citation counts
- **Be selective** - analyze 3 concepts thoroughly rather than 10 superficially

## Output Format

Use the template to create structured concept histories.

## Next Steps

After tracing citation chains, consider:
- `/assumption-killer` - Examine if foundational concepts rest on untested assumptions
- `/gap-scanner` - Identify where conceptual development needs to go next
- `/master-synthesis` - Integrate concept histories into broader literature synthesis
