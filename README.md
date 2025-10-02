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

### 2. Requirements Definition
- [Definition of Done](./requirements/05-definition-of-done.md)
- [Success Criteria & Metrics](./requirements/06-success-criteria.md)
- [Functional Requirements](./requirements/07-functional-requirements.md)
- [Non-Functional Requirements](./requirements/08-non-functional-requirements.md)

### 3. Architecture & Security (Coming Soon)
- Security-first architecture
- Data sovereignty patterns
- Multi-tenancy design

## How to Use

### Conversational Mode (Current)
1. Copy the relevant prompt into Claude Code or Claude
2. Run through the structured questions
3. Use the output to inform your next steps
4. Feed subsequent prompts with the artifacts from previous ones

### Automated Agent Mode (Future)
These prompts will be adapted for n8n workflow automation with:
- Structured input/output formats
- Human-in-the-loop decision gates
- Automated handoffs between stages

## Agent Workflow

These prompts are designed to work as an autonomous PM agent with human-in-the-loop decision gates:

1. **PM Interview** → Market validation → **[GO/NO-GO decision]**
2. **User Research** → Deep user understanding
3. **Solution Synthesis** → 2-3 solution concepts → **[Choose concept decision]**
4. **Market Analysis** → Competitive positioning (requires web search)
5. **Definition of Done** → Launch criteria
6. **Success Criteria** → Measurement plan with tracking implementation
7. **Functional Requirements** → What the system does
8. **Non-Functional Requirements** → How the system performs (security, performance, compliance)

## Current Status

**✅ Complete:**
- Product Discovery Phase (4 prompts)
- Requirements Phase (4 prompts)

**🚧 Coming Next:**
- Architecture & Security prompts
- n8n workflow templates
- Structured I/O formats for automation

## Contributing

These prompts are living documents. As you use them:
1. Note what works and what doesn't
2. Refine based on real-world results
3. Update versions and commit improvements
4. Share learnings

## Version History

- **v1.0** - October 1, 2025 - Initial prompt library with 8 core prompts

---

**Maintained by:** [@pmmikejackson](https://github.com/pmmikejackson)  
**License:** MIT  
**Last Updated:** October 1, 2025