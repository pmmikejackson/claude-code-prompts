# Success Criteria & Metrics Prompt

## Overview
This prompt defines measurable success criteria and key metrics to determine if the MVP achieves its goals. Use this alongside Definition of Done to establish both "what we ship" and "how we know it worked."

## TASK
You are a product manager defining success criteria for the MVP launch. Your goal is to establish specific, measurable metrics that determine whether the product validates the hypothesis, achieves product-market fit signals, and justifies continued investment. These metrics must be trackable, meaningful, and tied to business outcomes.

## CONSTRAINTS
- All metrics must be measurable with actual data (not surveys alone)
- Define metrics for multiple timeframes (launch, 30-day, 90-day)
- Include leading indicators (early signals) and lagging indicators (final outcomes)
- Distinguish between "success" and "failure" thresholds clearly
- Consider both quantitative metrics and qualitative signals
- Metrics must be achievable given the MVP scope and resources
- Focus on learning and validation, not vanity metrics

## INPUTS REQUIRED
Before starting, you need:
1. **PM Interview Output** - The validated problem and market opportunity
2. **Solution Concept** - What we're building and why
3. **User Research** - Target personas and their behaviors
4. **Market Analysis** - Competitive benchmarks
5. **Definition of Done** - What we're actually shipping

## QUESTIONS TO ANSWER

### 1. Primary Success Hypothesis
- What is the core hypothesis we're testing with this MVP?
- What would prove the hypothesis true?
- What would prove it false?
- What's our confidence threshold (e.g., 70% confident to proceed)?

### 2. Adoption & Engagement Metrics
- How many users need to adopt the product?
- What's the definition of an "active user"?
- What engagement frequency indicates value?
- What's the target activation rate (% who complete onboarding)?
- What's the target retention rate (1-week, 1-month)?

### 3. Value Delivery Metrics
- What user behavior indicates they're getting value?
- What's the target time-to-value?
- What's the target completion rate for core workflows?
- What problems are being solved (tracked via feature usage)?

### 4. Business Metrics
- What's the target conversion rate (if applicable)?
- What's the target customer acquisition cost (CAC)?
- What's the target lifetime value (LTV)?
- What's the target revenue or ARR (if monetizing)?
- What's the target payback period?

### 5. Quality & Experience Metrics
- What's the acceptable error/bug rate?
- What's the target customer satisfaction score?
- What's the target Net Promoter Score (NPS)?
- What's the acceptable support ticket volume?
- What's the target resolution time for issues?

### 6. Market Validation Signals
- What competitive wins indicate we're differentiated?
- What user testimonials or case studies validate value?
- What market traction indicators matter (press, word-of-mouth)?
- What partnership or integration interest validates the approach?

### 7. Learning Goals
- What key questions must be answered by launch + 90 days?
- What user behaviors need validation?
- What assumptions are riskiest to validate?
- What would we need to see to pivot vs. persevere?

## EXPECTED RESULTS

Produce a success criteria document containing:

1. **Success Hypothesis Statement**
   - Clear statement of what we believe and are testing
   - Definition of "success" vs "failure" vs "inconclusive"
   - Confidence threshold for decision-making

2. **North Star Metric**
   - The single most important metric indicating product success
   - Why this metric was chosen
   - Target value at 30, 60, 90 days post-launch

3. **Adoption Metrics**
   | Metric | Definition | Target (30d) | Target (90d) | Tracking Method |
   |--------|-----------|--------------|--------------|-----------------|
   | Total signups | Users who create account | X | Y | Analytics |
   | Activation rate | % who complete onboarding | X% | Y% | Analytics |
   | Active users | Users who [specific action] weekly | X | Y | Analytics |
   | Retention (1-week) | % who return after 7 days | X% | Y% | Cohort analysis |
   | Retention (1-month) | % who return after 30 days | X% | Y% | Cohort analysis |

4. **Engagement Metrics**
   | Metric | Definition | Target (30d) | Target (90d) | Tracking Method |
   |--------|-----------|--------------|--------------|-----------------|
   | Weekly active users | Users active 1+ times/week | X | Y | Analytics |
   | Core feature usage | % users who use [key feature] | X% | Y% | Analytics |
   | Session frequency | Average sessions per user/week | X | Y | Analytics |
   | Session duration | Average time spent per session | Xm | Ym | Analytics |
   | Feature adoption | % using 2+ core features | X% | Y% | Analytics |

5. **Value Delivery Metrics**
   | Metric | Definition | Target (30d) | Target (90d) | Tracking Method |
   |--------|-----------|--------------|--------------|-----------------|
   | Time-to-value | Time from signup to first value | Xm | Ym | Analytics |
   | Task completion | % who complete core workflow | X% | Y% | Analytics |
   | Problem resolution | Users reporting problem solved | X | Y | Survey + usage |
   | Workflow frequency | How often core workflow used | X/week | Y/week | Analytics |

6. **Business Metrics** (if applicable)
   | Metric | Definition | Target (30d) | Target (90d) | Tracking Method |
   |--------|-----------|--------------|--------------|-----------------|
   | Conversion rate | % of users who pay | X% | Y% | Payment system |
   | Monthly recurring revenue | MRR from paying customers | $X | $Y | Payment system |
   | Customer acquisition cost | Cost to acquire paying customer | $X | $Y | Marketing + sales |
   | Payback period | Months to recover CAC | Xm | Ym | Financial analysis |

7. **Quality & Experience Metrics**
   | Metric | Definition | Acceptable Threshold | Tracking Method |
   |--------|-----------|---------------------|-----------------|
   | Error rate | % of sessions with errors | < X% | Error monitoring |
   | Page load time | 95th percentile load time | < Xs | Performance monitoring |
   | Customer Satisfaction | CSAT score | > X/5 | In-app survey |
   | Net Promoter Score | NPS score | > X | Post-usage survey |
   | Support tickets | Tickets per 100 users | < X | Support system |

8. **Leading Indicators** (Early signals before full metrics mature)
   - Week 1: [Specific early signals to watch]
   - Week 2-4: [Signals that predict 90-day success]
   - What early patterns indicate success vs. failure?

9. **Lagging Indicators** (Final outcomes)
   - 90-day cohort retention
   - Customer LTV
   - Word-of-mouth growth rate
   - Revenue or business impact

10. **Qualitative Success Signals**
    - User testimonials or case studies showing clear value
    - Competitive wins or customers switching from competitors
    - Organic word-of-mouth or referrals
    - Partnership or integration interest from other companies
    - Media or analyst attention
    - Expansion opportunities (users asking for more features/tiers)

11. **Learning Questions & Validation**
    - Key question 1: [How we'll answer it and success criteria]
    - Key question 2: [How we'll answer it and success criteria]
    - Key question 3: [How we'll answer it and success criteria]
    - Assumption 1: [How we'll validate and what confirms/refutes it]
    - Assumption 2: [How we'll validate and what confirms/refutes it]

12. **Decision Framework**
    - **Success** (Clear signal to continue/invest): [Specific criteria]
    - **Qualified Success** (Proceed with adjustments): [Specific criteria]
    - **Inconclusive** (Need more time/data): [Specific criteria]
    - **Pivot Signal** (Change approach): [Specific criteria]
    - **Failure** (Stop): [Specific criteria]

13. **Measurement Plan**
    - What analytics tools will be used?
    - What tracking must be implemented?
    - How often are metrics reviewed?
    - Who is responsible for monitoring?
    - What dashboards or reports will be created?

14. **Review Cadence**
    - Daily: [What to monitor daily]
    - Weekly: [What to review weekly]
    - 30-day checkpoint: [Comprehensive review]
    - 60-day checkpoint: [Mid-point assessment]
    - 90-day checkpoint: [Final MVP success evaluation]

## Usage Example

```
Claude, define success criteria using this prompt.

Here's what we're building: [paste solution concept]
Here's the problem we're solving: [paste PM interview summary]
Here's our target users: [paste user research summary]
Here's the competitive context: [paste market analysis summary]

Create comprehensive success criteria and metrics for our MVP.
```

---

**Version:** 1.0  
**Last Updated:** October 1, 2025  
**Status:** Initial Draft - To be refined through real-world use