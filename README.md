# Claude Code Prompt Library

A collection of reusable prompts for Claude Code focused on pragmatic SaaS product development.

## Philosophy

- **Security & Data Sovereignty First** - Every prompt considers data protection and user privacy
- **Pragmatic Marketing** - Validate urgency, pervasiveness, and willingness to pay before building
- **Iterative Refinement** - These prompts evolve based on real-world usage

## Prompt Categories

### 1. Product Discovery
- [PM Interview - Market Validation](./product-discovery/01-pm-interview.md)
- [User Research & Problem Context](./product-discovery/02-user-research.md)
- [Solution Synthesis & Value Proposition](./product-discovery/03-solution-synthesis.md)
- [Market Analysis & Competitive Positioning](./product-discovery/04-market-analysis.md)

### 2. Requirements (Coming Soon)
- Definition of Done
- Success Criteria
- Functional Requirements
- Non-Functional Requirements

### 3. Architecture & Security (Coming Soon)
- Security-first architecture
- Data sovereignty patterns
- Multi-tenancy design

## How to Use

1. Copy the relevant prompt into Claude Code at the start of your project
2. Run through the structured questions
3. Use the output to inform your next steps
4. Feed subsequent prompts with the artifacts from previous ones

## Agent Workflow

These prompts are designed to work as an autonomous PM agent with human-in-the-loop decision gates:

1. **PM Interview** → GO/NO-GO decision
2. **User Research** → Understanding phase
3. **Solution Synthesis** → Choose concept decision
4. **Market Analysis** → Competitive positioning (requires web search)
5. **Requirements** → Build specifications

## Contributing

These prompts are living documents. As you use them, note what works and what doesn't, then refine.

---

**Version:** 1.0  
**Last Updated:** October 1, 2025