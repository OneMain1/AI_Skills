---
name: assumption-killer
description: Identifies consequential untested assumptions that most papers share - reveals hidden foundations that could invalidate findings if proven false
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# Assumption Killer Protocol

This skill identifies the most consequential assumptions that the majority of your papers share but never explicitly test, justify, or even acknowledge as assumptions. It reveals the hidden foundations of a field's knowledge.

## What This Skill Does

When analyzing your paper collection, this skill:

1. **Identifies 5-8 foundational assumptions** shared across papers
2. **Assesses risk level** of each assumption (how much would collapse if it's wrong)
3. **Names papers** that rely most heavily on each assumption
4. **Predicts consequences** if the assumption proves false
5. **Ranks assumptions** from most to least consequential

## When to Use

- After completing `/master-synthesis` analysis
- When critically evaluating a research paradigm
- Before designing studies that challenge conventional wisdom
- To identify high-impact research opportunities
- When writing a critical literature review

## How to Use

Invoke this skill with your papers:

```
/assumption-killer

Identify untested assumptions across these papers on [topic]:
[list of papers or paths]
```

## Analysis Instructions

### Step 1: Identify Shared Assumptions

Scan all papers to find assumptions that are:

#### A. Foundational to Conclusions
- If the assumption is false, major conclusions would need revision
- The assumption underlies interpretation of results
- Authors' theoretical framework depends on it

#### B. Never Tested or Justified
- No paper provides empirical evidence for the assumption
- Authors don't acknowledge it as an assumption (they treat it as fact)
- It's taken for granted across the field

#### C. Plausibly False or Context-Dependent
- The assumption could reasonably be wrong
- It might be true in some contexts but not others
- Alternative possibilities exist

**Do NOT include**:
- Explicitly tested hypotheses
- Acknowledged limitations
- Standard methodological assumptions (e.g., "samples are representative")
- Assumptions unique to one paper

**Focus on assumptions like**:
- "X always causes Y (never the reverse)"
- "Z is universal across cultures/contexts"
- "Mechanism M operates the same way in all populations"
- "Short-term effects indicate long-term effects"
- "Self-report accurately measures construct C"

### Step 2: Document Each Assumption

For each of the 5-8 most consequential assumptions:

#### A. State the Assumption
Write as a declarative claim that the papers implicitly accept as true.

**Format**: "X causes Y under all conditions" or "Z is universally applicable"

**Not**: "Papers assume X might cause Y" (too hedged)

#### B. Shared By
Name 2-3 papers that rely on this assumption most heavily.

Identify papers where:
- The assumption is most central to their argument
- Their conclusions would most change if assumption is false
- They build most directly on this foundation

#### C. Risk Level Assessment
Rate as **Low**, **Medium**, or **High** based on:

**Low**: If wrong, minor revisions to conclusions needed
**Medium**: If wrong, key findings would be invalidated
**High**: If wrong, the entire research paradigm collapses

#### D. Consequence Analysis
Explain what would change if the assumption proves false:

- What conclusions would need revision?
- What findings would be invalidated?
- Would the field need new theoretical frameworks?
- Would measurement approaches become obsolete?

Be specific about the cascade of effects.

### Step 3: Rank Assumptions

Order from **most to least consequential**.

Consider:
- How many papers depend on it?
- How central is it to the field's conclusions?
- How likely is it to be false?
- How much would change if it's disproven?

### Important Criteria

An assumption must be:
1. **Shared** - used by multiple papers (majority of your set)
2. **Untested** - never empirically examined in these papers
3. **Consequential** - its falsehood would significantly impact conclusions
4. **Implicit** - treated as fact, not acknowledged as assumption

## Important Guidelines

- **Be critical, not dismissive** - identifying assumptions is not attacking research
- **Be specific** - vague assumptions like "the theory is correct" don't help
- **Be evidence-based** - cite specific papers that rely on each assumption
- **Be fair** - focus on genuinely untested assumptions, not acknowledged limitations
- **Be consequential** - only include assumptions whose falsehood would matter

## Output Format

Use the template to create a structured assumption analysis.

## Next Steps

After identifying critical assumptions:
- Design research to explicitly test the highest-risk assumptions
- Use `/gap-scanner` to see if testing these assumptions fills identified gaps
- Consider how your research could provide evidence for or against key assumptions
- Write a critical commentary highlighting these hidden foundations
