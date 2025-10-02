# Definition of Done Prompt

## Overview
This prompt establishes clear, measurable criteria for when the MVP is considered complete and ready to launch. Use this after market analysis to define what "done" means before writing requirements.

## TASK
You are a product manager defining the Definition of Done (DoD) for the MVP. Your goal is to create clear, specific, measurable criteria that determine when the product is ready to ship. This prevents scope creep and ensures alignment between stakeholders on what "launched" means.

## CONSTRAINTS
- Focus on MVP scope only - what's the minimum to validate the solution
- All criteria must be measurable and verifiable (yes/no, not subjective)
- Include both feature completeness AND quality gates
- Consider security, data sovereignty, and compliance from the start
- Balance between shipping fast and shipping responsibly
- Get specific - avoid vague terms like "works well" or "user-friendly"
- Must include rollback plan and monitoring criteria

## INPUTS REQUIRED
Before starting, you need:
1. **Chosen Solution Concept** - From Solution Synthesis
2. **Core MVP Features** - The 3-5 essential capabilities identified
3. **Target Users** - From User Research
4. **Market Context** - Competitive positioning and timing considerations

## QUESTIONS TO ANSWER

### 1. Feature Completeness Criteria
- What specific features must be functional?
- What does "functional" mean for each feature?
- What user workflows must work end-to-end?
- What edge cases must be handled vs. can be deferred?
- What integrations must work?

### 2. Quality & Performance Criteria
- What response time/performance thresholds are required?
- What uptime/reliability is acceptable for MVP?
- What browsers/devices must be supported?
- What's the acceptable bug/defect threshold?
- What accessibility standards must be met?

### 3. Security & Compliance Criteria
- What security measures must be implemented?
- What data protection requirements must be met?
- What compliance requirements apply (GDPR, SOC2, etc.)?
- What authentication/authorization must work?
- What audit logging is required?

### 4. User Experience Criteria
- What onboarding flow must exist?
- What documentation/help must be available?
- What error handling/messaging must work?
- What feedback mechanisms must exist?
- What mobile responsiveness is required (if applicable)?

### 5. Operational Readiness Criteria
- What monitoring must be in place?
- What alerting is required?
- What backup/recovery capability must exist?
- What support processes must be ready?
- What deployment/rollback plan must exist?

### 6. Business/Legal Criteria
- What terms of service/privacy policy must be ready?
- What payment processing must work (if applicable)?
- What analytics/tracking must be implemented?
- What customer communication channels must be set up?

### 7. Launch Readiness Criteria
- What internal testing has been completed?
- What beta/pilot testing is required before general launch?
- What marketing/communication assets must be ready?
- What customer support resources must be prepared?

## EXPECTED RESULTS

Produce a Definition of Done document containing:

1. **MVP Scope Summary**
   - Brief description of what's included in MVP
   - Explicit list of what's NOT included (deferred to v2+)
   - Rationale for scope decisions

2. **Feature Completeness Checklist**
   - [ ] Feature 1: [Specific, measurable completion criteria]
   - [ ] Feature 2: [Specific, measurable completion criteria]
   - [ ] Feature 3: [Specific, measurable completion criteria]
   - [ ] End-to-end workflow: [Specific user journey that must work]
   - [ ] Integration: [Specific integration points that must function]

3. **Quality Gates Checklist**
   - [ ] Performance: [Specific metrics, e.g., "Page load < 2s for 95th percentile"]
   - [ ] Reliability: [e.g., "99% uptime over 7-day test period"]
   - [ ] Browser support: [e.g., "Works on Chrome, Firefox, Safari (latest 2 versions)"]
   - [ ] Bug threshold: [e.g., "Zero critical bugs, < 5 high-priority bugs"]
   - [ ] Accessibility: [e.g., "WCAG 2.1 Level A compliance"]

4. **Security & Compliance Checklist**
   - [ ] Authentication: [Specific requirements]
   - [ ] Authorization: [Specific requirements]
   - [ ] Data encryption: [At rest and in transit requirements]
   - [ ] Privacy policy: [Approved and published]
   - [ ] Security audit: [Completed with no critical findings]
   - [ ] Compliance: [Specific requirements met, e.g., "GDPR-compliant data handling"]

5. **User Experience Checklist**
   - [ ] Onboarding: [Specific flow completion criteria]
   - [ ] Documentation: [What must exist]
   - [ ] Error handling: [Coverage requirements]
   - [ ] Help/support: [What channels/resources exist]
   - [ ] Mobile: [Specific responsiveness criteria if applicable]

6. **Operational Readiness Checklist**
   - [ ] Monitoring: [What metrics are tracked]
   - [ ] Alerting: [What alerts are configured]
   - [ ] Backup: [What backup strategy is implemented]
   - [ ] Rollback plan: [Documented and tested]
   - [ ] Support playbook: [Common issues and resolutions documented]

7. **Business/Legal Readiness Checklist**
   - [ ] Terms of Service: [Reviewed by legal, published]
   - [ ] Privacy Policy: [Reviewed by legal, published]
   - [ ] Payment processing: [If applicable, tested and functional]
   - [ ] Analytics: [Core tracking implemented]
   - [ ] Customer communication: [Email/notification systems ready]

8. **Launch Criteria**
   - [ ] Internal testing: [Specific testing completed]
   - [ ] Beta testing: [If required, criteria for beta completion]
   - [ ] Marketing assets: [Landing page, messaging, etc.]
   - [ ] Support readiness: [Team trained, processes ready]
   - [ ] Go/No-Go checklist: [Final pre-launch verification]

9. **Acceptance Process**
   - Who reviews and approves DoD completion?
   - What's the sign-off process?
   - What happens if criteria aren't met?

10. **Known Limitations & Technical Debt**
    - What shortcuts were taken that need future work?
    - What scale limitations exist in MVP?
    - What's the plan to address technical debt post-launch?

## Usage Example

```
Claude, create a Definition of Done using this prompt.

Here's our MVP scope: [paste solution concept]
Here are our core features: [paste feature list]
Here's our user context: [paste user research summary]

Create comprehensive, measurable DoD criteria for our MVP launch.
```

---

**Version:** 1.0  
**Last Updated:** October 1, 2025  
**Status:** Initial Draft - To be refined through real-world use