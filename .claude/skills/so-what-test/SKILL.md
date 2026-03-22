---
name: so-what-test
description: Summarizes entire research body in 3 concise points for non-experts - what's proven, what's unknown, and why it matters
user-invocable: true
disable-model-invocation: false
allowed-tools: Read, Grep, WebFetch
---

# The 'So What' Test Protocol

This skill distills your entire literature collection into a clear, jargon-free summary for intelligent non-experts. It answers the fundamental question: "So what does all this research actually tell us?"

## What This Skill Does

When analyzing your paper collection, this skill produces exactly **3 numbered points**:

1. **What has been proven** - The strongest, most reliable finding (stated as fact, no hedging)
2. **What is still unknown** - The most significant thing the field hasn't figured out
3. **Why it matters** - The most important real-world implication or theoretical consequence

Each point is 2-3 sentences maximum.

## When to Use

- When explaining your research area to non-specialists
- For grant proposals' "broader impacts" sections
- When writing press releases or public summaries
- To prepare for interdisciplinary collaborations
- Before presenting to non-academic audiences
- To test if research has practical value

## How to Use

Invoke this skill with your papers:

```
/so-what-test

Summarize this research for a non-expert:
[list of papers or paths]
```

## Analysis Instructions

### Audience

**Write as if speaking to**:
- An intelligent person with no domain knowledge
- Someone who reads *The Economist* or *Scientific American*
- A smart colleague from a completely different field
- Your dean, your funder, or a policymaker

**NOT**:
- A specialist in your field
- Someone who knows the jargon
- An academic peer reviewer

### Format Requirements

**Exactly 3 numbered points**

Each point:
- 2-3 sentences maximum
- No more, no less

**Total length**: ~150-200 words for all three points combined

### Point 1: What Has Been Proven

**The strongest, most reliable finding from this literature.**

**Requirements**:
- State as a **direct claim** with no hedging
- No "suggests," "may indicate," "appears to show"
- Write as established fact
- Choose the finding with the most robust evidence

**If uncertain**: Don't fabricate certainty. Instead, write: "This research has not yet produced definitive findings, but consistently shows [pattern]."

**Example format**:
"This research proves that [claim]. The effect holds across [contexts/populations/methods], making it one of the most reliable findings in [field]."

**NOT**:
"Research suggests that X might be related to Y under certain conditions, though more work is needed."

### Point 2: What Is Still Unknown

**The most significant thing this field has not yet figured out.**

**Requirements**:
- State **honestly** without minimizing the uncertainty
- Identify the biggest gap, not a minor loose end
- Be specific about what's unknown
- Don't sugarcoat or downplay

**Example format**:
"Researchers still don't know [specific unknown]. This gap exists because [reason: can't measure it, haven't tested it, methods don't exist yet]."

**NOT**:
"While much progress has been made, future research could explore some additional nuances."

### Point 3: Why It Matters

**The single most important real-world implication.**

**Requirements**:
- If there's a **practical application**, state it clearly
- If there's **no direct application**, state the biggest theoretical consequence instead
- Focus on impact outside the academic field
- Make it concrete and specific

**Example format** (practical):
"This matters because [concrete real-world impact: helps design better X, changes how we should do Y, explains why Z happens in society]."

**Example format** (theoretical):
"This matters because it fundamentally changes how we understand [phenomenon], which has implications for [broader domain]."

**NOT**:
"This contributes to the scholarly literature and opens avenues for future research."

### Overall Style Rules

**Required**:
- ✓ Use plain language
- ✓ Explain concepts without jargon
- ✓ Be direct and concrete
- ✓ State clearly and confidently

**Forbidden**:
- ✗ No jargon without explanation
- ✗ No citations (this is for non-experts)
- ✗ No hedging that weakens the point
- ✗ No "this contributes to the literature" vaguenesss

## Important Guidelines

- **Be honest** - if nothing definitive is proven, say so
- **Be selective** - one proven finding, not five weak ones
- **Be specific** - concrete examples beat abstract claims
- **Be accessible** - your parent or neighbor should understand it
- **Be confident** - if the papers support it, state it as fact

## Output Format

Use the template to create the 3-point summary.

## Next Steps

After creating the So What summary:
- Use it to pitch your research area to non-specialists
- Include it in grant broader impacts sections
- Share with collaborators from other fields
- Use it as an "elevator pitch" for your research area
- Test it on someone outside your field - can they understand it?
