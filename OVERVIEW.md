# Project Overview & Roadmap

## Vision

Build an autonomous PM agent that guides SaaS product development from initial idea validation through complete requirements documentation. The agent uses pragmatic marketing principles, prioritizes security and data sovereignty, and provides human-in-the-loop decision gates at critical points.

## Current State (v1.0)

**✅ Completed: Conversational Prompt Library**

We have 8 production-ready prompts that work conversationally with Claude/Cursor:

### Product Discovery Phase
1. **PM Interview - Market Validation** - Validates urgency, pervasiveness, willingness to pay
2. **User Research & Problem Context** - Deep user understanding, journey mapping
3. **Solution Synthesis & Value Proposition** - Generates 2-3 solution concepts
4. **Market Analysis & Competitive Positioning** - Web search-powered competitive intelligence

### Requirements Phase
5. **Definition of Done** - Clear launch criteria
6. **Success Criteria & Metrics** - Measurable success with tracking implementation
7. **Functional Requirements** - What the system must do
8. **Non-Functional Requirements** - Security, performance, compliance (security-first)

## Tool Stack

### Current Tools
- **GitHub** - Version control for prompt library
- **Cursor** - IDE for building products and testing prompts conversationally
- **Claude (web/API)** - Powers the prompts

### Planned Tools
- **n8n** (on NAS) - Workflow automation for PM agent
- **Claude Code** (optional) - Autonomous code generation from requirements

## Workflows

### Phase 1: Current Workflow (Conversational)
```
Developer → Opens Cursor
  ↓
Developer → Copies prompt from GitHub repo
  ↓
Developer → Pastes into Cursor AI chat
  ↓
Claude → Runs prompt conversationally
  ↓
Developer → Reviews output, refines, iterates
  ↓
Developer → Moves to next prompt with previous outputs
  ↓
Result → Complete requirements documentation
```

**Use this for:** Testing prompts, refining them, learning what works

### Phase 2: Future Workflow (Automated via n8n)

```
Developer → Triggers n8n workflow with initial idea
  ↓
n8n → Runs PM Interview prompt (Claude API)
  ↓
n8n → Presents findings to developer
  ↓
Developer → GO/NO-GO decision
  ↓
[If GO]
  ↓
n8n → Runs User Research prompt
  ↓
n8n → Runs Solution Synthesis prompt
  ↓
n8n → Presents 2-3 solution concepts
  ↓
Developer → Chooses concept
  ↓
n8n → Runs Market Analysis (with web search)
  ↓
n8n → Runs Definition of Done
  ↓
n8n → Runs Success Criteria
  ↓
n8n → Runs Functional Requirements
  ↓
n8n → Runs Non-Functional Requirements
  ↓
Result → Complete PRD delivered as structured document
```

**Use this for:** Production SaaS projects, repeatable process

### Phase 3: Code Generation (Optional)

After n8n generates complete requirements:

```
Developer → Reviews requirements doc
  ↓
Developer → Runs Claude Code with requirements
  ↓
Claude Code → Generates scaffold, boilerplate, core features
  ↓
Developer → Reviews, refines in Cursor
  ↓
Result → Working MVP codebase
```

**Use this for:** Accelerating development, generating boilerplate

## Development Approach

### Philosophy
- **Vibe coding friendly** - Visual tools, AI assistance, clear structure
- **Security first** - Data sovereignty and privacy built in from day one
- **Pragmatic marketing** - Validate before building
- **Iterative refinement** - Prompts evolve based on real usage

### Tool Selection Rationale

**Why Cursor (not terminal/Warp):**
- Visual feedback for complex architecture
- AI assistance for OOP struggles
- Error highlighting before runtime
- Integrated debugging

**Why n8n (not custom scripts):**
- Visual workflow builder
- Easy to modify without coding
- Runs on NAS (data sovereignty)
- Human-in-the-loop gates built-in

**Why separate Claude Code (not integrated):**
- Different use case (requirements vs code)
- Can be used independently
- Optional - not required for PM agent

## Roadmap

### ✅ Phase 1: Conversational Prompts (COMPLETE)
- [x] Build 8 core prompts
- [x] GitHub repository
- [x] Documentation
- [x] Test with Cursor

### 🚧 Phase 2: Prompt Refinement (IN PROGRESS)
- [ ] Test prompts on real project ideas
- [ ] Gather feedback on what works/doesn't work
- [ ] Refine based on actual usage
- [ ] Version 1.1 updates

### 📋 Phase 3: n8n Automation (PLANNED)
- [ ] Design n8n workflow structure
- [ ] Convert prompts to structured I/O format
- [ ] Build n8n workflow with decision gates
- [ ] Test end-to-end automation
- [ ] Document n8n setup process

### 📋 Phase 4: Additional Prompts (PLANNED)
- [ ] Architecture & Security prompts
- [ ] Multi-tenancy design patterns
- [ ] API design prompts
- [ ] Database schema design prompts

### 📋 Phase 5: Claude Code Integration (OPTIONAL)
- [ ] Test Claude Code with generated requirements
- [ ] Create handoff format (requirements → code)
- [ ] Document code generation workflow

## Success Criteria

### For Phase 1 (Current)
- ✅ 8 working prompts
- ✅ GitHub repository
- ✅ Clear documentation
- 🔄 Successfully used on 1-2 real projects (in progress)

### For Phase 2 (n8n Automation)
- Complete PM agent workflow runs end-to-end
- Decision gates work properly
- Requirements output is high quality
- Time saved vs manual process: >70%

### For Phase 3 (Claude Code)
- Generated code compiles/runs
- Security requirements implemented
- Data sovereignty patterns followed
- Developer can build on scaffold

## Key Design Decisions

### Why Conversational First?
Testing and refinement are critical. Automation only works if the prompts are proven. Conversational use lets us iterate quickly.

### Why Human-in-the-Loop?
Product decisions (GO/NO-GO, concept selection) require human judgment. Agent generates insights, human makes strategic calls.

### Why Security First?
SaaS products handle user data. Security and privacy must be architected in, not bolted on. Every prompt considers this.

### Why GitHub (not Google Docs)?
- Version control for prompt refinement
- Works better with Claude Code
- Easy to clone/fork for projects
- Developer-friendly workflow

## Open Questions

### For n8n Implementation
- [ ] How do we structure prompt I/O for n8n parsing?
- [ ] What's the best format for passing context between prompts?
- [ ] How do we handle web search in n8n? (API integration needed)
- [ ] What's the authentication flow for Claude API in n8n?

### For Claude Code
- [ ] What's the handoff format between requirements and code gen?
- [ ] How do we ensure security patterns are implemented?
- [ ] How do we validate generated code meets NFRs?

## Notes for Future Development

### When Converting to n8n
- Each prompt needs clear JSON input/output schema
- Build prompt templates with variable injection
- Create error handling for API failures
- Implement retry logic for Claude API rate limits
- Store intermediate outputs in n8n database

### When Adding Claude Code
- Requirements doc must be complete before code gen
- Start with scaffold generation, not full features
- Always generate with security/data sovereignty patterns
- Test generated code before committing

### When Scaling
- Consider prompt token limits (stay under context windows)
- May need to chunk large requirements docs
- Build summarization prompts for context compression
- Cache frequently used context (user personas, etc.)

## Contributing

These are living documents. As you use them:

1. **Test thoroughly** - Run prompts on real projects
2. **Document issues** - Note what doesn't work
3. **Propose improvements** - Update prompts based on learnings
4. **Version changes** - Increment version numbers
5. **Commit improvements** - Push refinements to GitHub

## Contact & Support

**Repository:** https://github.com/pmmikejackson/claude-code-prompts  
**Maintainer:** @pmmikejackson  
**License:** MIT  

---

**Last Updated:** October 1, 2025  
**Current Version:** 1.0  
**Status:** Phase 1 Complete, Phase 2 In Progress