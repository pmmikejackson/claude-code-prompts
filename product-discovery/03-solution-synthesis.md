# Solution Synthesis & Value Proposition Prompt

## Overview
This prompt synthesizes findings from the PM Interview and User Research to propose concrete solution concepts. Use this after validating the market and understanding users deeply.

## TASK
You are a product strategist. Your goal is to analyze the validated problem and user research, then synthesize 2-3 distinct solution concepts that address the core user needs. Each concept should have clear differentiation, a defined value proposition, and a realistic MVP scope.

## CONSTRAINTS
- Base all proposals strictly on evidence from PM Interview and User Research outputs
- Propose 2-3 distinct approaches (not minor variations)
- Each concept must be technically feasible within 3-6 months for MVP
- Focus on solving the CORE pain, not every possible feature
- Consider security and data sovereignty from the start (given user context)
- Be opinionated but explain your reasoning
- Present concepts in order of recommendation (strongest first)

## INPUTS REQUIRED
Before starting, you need:
1. **PM Interview Summary** - Problem validation (urgency, pervasiveness, willingness to pay)
2. **User Research Output** - Personas, journey maps, pain points, mental models

## QUESTIONS TO ANSWER

### For Each Solution Concept:

**1. Core Solution Approach**
- What is the fundamental approach to solving this problem?
- What makes this approach different from existing solutions?
- What's the key insight driving this concept?

**2. Target Users & Jobs-to-be-Done**
- Which user personas does this primarily serve?
- What specific job(s) does it help them accomplish?
- What pain points does it eliminate?

**3. Core Capabilities (MVP Scope)**
- What are the 3-5 essential capabilities for MVP?
- What's the minimum viable feature set?
- What are we explicitly NOT building in v1?

**4. Value Proposition**
- What's the one sentence value prop?
- Why would users choose this over current alternatives?
- What's the economic value to users?

**5. Differentiation**
- How is this different from existing solutions?
- What's our unique angle or advantage?
- What makes this defensible?

**6. Technical Considerations**
- Any critical technical requirements?
- Security/data sovereignty implications?
- Integration needs?

**7. Risks & Open Questions**
- What assumptions need validation?
- What could cause this concept to fail?
- What don't we know yet?

## EXPECTED RESULTS

Produce a solution concept document containing:

1. **Executive Summary**
   - Brief recap of the validated problem
   - Your recommended solution concept (with reasoning)

2. **Solution Concept #1** (Recommended)
   - Name/tagline for the concept
   - Core approach and key insight
   - Target users and jobs-to-be-done
   - MVP capabilities (3-5 features)
   - Value proposition statement
   - Differentiation from alternatives
   - Technical considerations
   - Risks and open questions

3. **Solution Concept #2** (Alternative)
   - [Same structure as #1]

4. **Solution Concept #3** (Alternative) - Optional
   - [Same structure as #1]

5. **Comparison Matrix**
   - Side-by-side comparison of concepts
   - Pros/cons of each approach
   - Estimated complexity/time to MVP
   - Risk assessment

6. **Recommendation**
   - Which concept to pursue and why
   - What needs to be validated next
   - Suggested next steps

## Usage Example

```
Claude, synthesize solution concepts using the Solution Synthesis prompt.

Here's the PM Interview output: [paste summary]
Here's the User Research output: [paste summary]

Propose 2-3 distinct solution concepts for me to evaluate.
```

---

**Version:** 1.0  
**Last Updated:** October 1, 2025  
**Status:** Initial Draft - To be refined through real-world use