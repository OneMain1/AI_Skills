---
name: master-synthesis
description: Creates a comprehensive synthesis of the literature - identifies consensus, active debates, strongest evidence, and the key open question across all papers
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# Master Synthesis Protocol

This skill creates a high-level synthesis of your entire literature collection, writing across all papers to identify what's settled, what's debated, what's most reliable, and what's the most important unanswered question.

## What This Skill Does

When analyzing your paper collection, this skill produces a **400-word synthesis** with four sections:

1. **Established consensus** (~100 words) - What the field collectively agrees on
2. **Active debates** (~100 words) - What researchers meaningfully disagree about
3. **Strongest evidence** (~100 words) - What claims have the most robust support
4. **Key open question** (~80 words) - The most important unanswered question

## When to Use

- After completing most other analysis skills
- When writing the synthesis section of a literature review
- To get a bird's-eye view of a research area
- Before proposing a new research project
- To brief others on the state of a field

## How to Use

Invoke this skill with your papers:

```
/master-synthesis

Synthesize the literature across these papers on [topic]:
[list of papers or paths]
```

## Analysis Instructions

### Critical Rule: Write ACROSS the Literature

**Do NOT summarize individual papers.**

Instead:
- Write about patterns across all papers
- Identify collective findings
- Synthesize themes that emerge from multiple sources
- Focus on the literature as a body, not as individual contributions

### Section 1: Established Consensus (~100 words)

**What does this field collectively agree on?**

Identify claims that:
- Appear in multiple papers without contradiction
- Are treated as foundational by most authors
- Form the baseline assumptions of the field

**Requirements**:
- Cite at least 2 papers supporting each claim
- Write declaratively - state facts, not "researchers suggest"
- If there's no consensus on something, don't include it here

**Format**: Write as flowing paragraphs, not bullet points.

**Example structure**:
"This literature agrees that [claim 1] (Author A, Year; Author B, Year). Additionally, researchers consistently find that [claim 2] (Author C, Year; Author D, Year). There is widespread acceptance that [claim 3] (Author E, Year; Author F, Year)."

### Section 2: Active Debates (~100 words)

**What do researchers in this field meaningfully disagree about?**

Identify genuine intellectual debates where:
- Authors take different positions on the same question
- Disagreements are substantive, not methodological trivia
- Multiple papers engage with the contested issue

**Requirements**:
- Name the disagreeing positions WITHOUT naming individual papers
- Write about the debate itself, not who's involved
- Focus on why the debate matters

**Format**: Describe debates as active ongoing discussions.

**Example structure**:
"The field is divided on [issue 1], with some arguing [position A] while others contend [position B]. Another unresolved debate concerns [issue 2], where disagreement centers on [core point of contention]. A third area of active discussion involves [issue 3]."

### Section 3: Strongest Evidence (~100 words)

**What claims are supported by the most consistent, replicated, or methodologically robust evidence?**

Identify findings that:
- Are replicated across multiple papers with different methods
- Come from rigorous methodologies (per `/methodology-audit`)
- Show consistent patterns despite varying contexts

**Requirements**:
- Prioritize empirical evidence over theoretical claims
- Focus on reliability and robustness, not just agreement
- Write about the evidence quality, not just the claim

**Format**: State what's well-established based on evidence strength.

**Example structure**:
"The most robust finding is [claim 1], which has been demonstrated through [different methods/contexts]. Equally well-supported is [claim 2], consistently observed across [variation in studies]. Strong convergent evidence also supports [claim 3]."

### Section 4: The Key Open Question (~80 words)

**What is the single most important unanswered question in this field?**

Choose the question whose resolution would:
- Most change our understanding
- Unlock answers to other questions
- Advance the field fundamentally

**Requirements**:
- End with a clear, specific question (not vague "future research needed")
- Explain why resolving it matters
- Don't hedge - commit to the most important question

**Format**: Build up to the question, then state it clearly.

**Example structure**:
"Despite advances in [area], the literature has not resolved [issue]. This gap is critical because [reason]. The key unanswered question is: [Specific question]?"

### Overall Requirements

**Total length**: Exactly 400 words maximum

**Style rules**:
- No hedging phrases like "it seems," "may suggest," "appears to indicate"
- State claims clearly and directly
- If papers lack consensus on a topic, state that explicitly rather than hedging
- Use citations in-text: (Author, Year)
- Write for a knowledgeable reader, not a general audience

**What to avoid**:
- Individual paper summaries
- Lists of "Paper A found X, Paper B found Y"
- Vague generalizations
- Hedging language that weakens claims

## Important Guidelines

- **Synthesize, don't summarize** - write about collective patterns, not individual papers
- **Be decisive** - if the literature is unclear, say so; don't pretend consensus exists
- **Cite evidence** - every claim in "consensus" needs at least 2 paper citations
- **Stay focused** - 400 words is tight; every sentence must earn its place
- **Be honest** - if a section can't be populated (e.g., no real consensus), state that

## Output Format

Use the template to create the synthesis.

## Next Steps

After creating the master synthesis:
- Use this as the foundation for your literature review
- Share with collaborators to align understanding
- Use the "key open question" to guide your research proposal
