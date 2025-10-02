# Success Criteria & Metrics Prompt

## Overview
This prompt defines measurable success criteria and key metrics to determine if the MVP achieves its goals. Use this alongside Definition of Done to establish both "what we ship" and "how we know it worked."

## TASK
You are a product manager defining success criteria for the MVP launch. Your goal is to establish specific, measurable metrics that determine whether the product validates the hypothesis, achieves product-market fit signals, and justifies continued investment. These metrics must be trackable, meaningful, and tied to business outcomes.

**CRITICAL: You must specify exactly HOW each metric will be measured - what tools, what events to track, what code instrumentation is needed.**

## CONSTRAINTS
- All metrics must be measurable with actual data (not surveys alone)
- Define metrics for multiple timeframes (launch, 30-day, 90-day)
- Include leading indicators (early signals) and lagging indicators (final outcomes)
- Distinguish between "success" and "failure" thresholds clearly
- Consider both quantitative metrics and qualitative signals
- Metrics must be achievable given the MVP scope and resources
- Focus on learning and validation, not vanity metrics
- **MANDATORY: Specify exact tracking implementation for every metric**

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

### 8. Measurement Implementation Requirements
- What analytics platform will be used? (e.g., Mixpanel, Amplitude, PostHog, self-hosted)
- What events need to be tracked in code?
- What user properties need to be captured?
- What conversion funnels need to be set up?
- How will we track revenue/payments?
- What dashboards need to be built?

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
   - **Exact tracking implementation** (what event/calculation)

3. **Adoption Metrics**
   | Metric | Definition | Target (30d) | Target (90d) | Event/Implementation |
   |--------|-----------|--------------|--------------|---------------------|
   | Total signups | Users who create account | X | Y | Track `user_signup` event with timestamp |
   | Activation rate | % who complete onboarding | X% | Y% | Track `onboarding_completed` event, calculate % of signups |
   | Active users | Users who [specific action] weekly | X | Y | Track `[action]` event, count unique users per week |
   | Retention (1-week) | % who return after 7 days | X% | Y% | Track any activity event, cohort analysis by signup date |
   | Retention (1-month) | % who return after 30 days | X% | Y% | Track any activity event, cohort analysis by signup date |

4. **Engagement Metrics**
   | Metric | Definition | Target (30d) | Target (90d) | Event/Implementation |
   |--------|-----------|--------------|--------------|---------------------|
   | Weekly active users | Users active 1+ times/week | X | Y | Track session_start event, count weekly uniques |
   | Core feature usage | % users who use [key feature] | X% | Y% | Track `feature_[name]_used` event, % of total users |
   | Session frequency | Average sessions per user/week | X | Y | Track `session_start`, calculate avg per user per week |
   | Session duration | Average time spent per session | Xm | Ym | Track `session_start` and `session_end`, calculate duration |
   | Feature adoption | % using 2+ core features | X% | Y% | Track feature events, identify users with 2+ distinct features |

5. **Value Delivery Metrics**
   | Metric | Definition | Target (30d) | Target (90d) | Event/Implementation |
   |--------|-----------|--------------|--------------|---------------------|
   | Time-to-value | Time from signup to first value moment | Xm | Ym | Track `user_signup` and `value_moment_achieved`, calculate time diff |
   | Task completion | % who complete core workflow | X% | Y% | Track `workflow_completed` event, % of users who started |
   | Problem resolution | Users reporting problem solved | X | Y | Track `problem_solved` survey response or event |
   | Workflow frequency | How often core workflow used | X/week | Y/week | Track `workflow_completed`, calculate per-user frequency |

6. **Business Metrics** (if applicable)
   | Metric | Definition | Target (30d) | Target (90d) | Event/Implementation |
   |--------|-----------|--------------|--------------|---------------------|
   | Conversion rate | % of users who pay | X% | Y% | Track `payment_completed`, % of total signups |
   | Monthly recurring revenue | MRR from paying customers | $X | $Y | Sum subscription amounts from payment system |
   | Customer acquisition cost | Cost to acquire paying customer | $X | $Y | Marketing spend / paying customers |
   | Payback period | Months to recover CAC | Xm | Ym | CAC / (MRR per customer) |

7. **Conversion Funnel Tracking**
   Define the complete funnel with drop-off measurement:
   - Step 1: Landing page visit → Track `page_view` on landing page
   - Step 2: Signup started → Track `signup_started` (clicked signup button)
   - Step 3: Account created → Track `user_signup` (completed registration)
   - Step 4: Onboarding started → Track `onboarding_started`
   - Step 5: Onboarding completed → Track `onboarding_completed`
   - Step 6: First value moment → Track `value_moment_achieved`
   - Step 7: Payment (if applicable) → Track `payment_completed`
   
   **Calculate drop-off rates between each step to identify friction points**

8. **Quality & Experience Metrics**
   | Metric | Definition | Acceptable Threshold | Event/Implementation |
   |--------|-----------|---------------------|---------------------|
   | Error rate | % of sessions with errors | < X% | Track `error_occurred` with error details, % of total sessions |
   | Page load time | 95th percentile load time | < Xs | Real User Monitoring (RUM) tool or custom timing events |
   | Customer Satisfaction | CSAT score | > X/5 | In-app survey after key actions, track `survey_completed` |
   | Net Promoter Score | NPS score | > X | Post-usage survey (30 days), track `nps_survey_completed` |
   | Support tickets | Tickets per 100 users | < X | Support system integration or manual tracking |

9. **Analytics Implementation Checklist**
   - [ ] Analytics platform selected and configured (specify: _______)
   - [ ] User identification system implemented (user_id tracking)
   - [ ] All critical events instrumented in code
   - [ ] Event properties defined (what data captured with each event)
   - [ ] Conversion funnels configured in analytics platform
   - [ ] Cohort analysis capability set up
   - [ ] Real-time dashboard created for key metrics
   - [ ] Revenue/payment tracking integrated
   - [ ] Error tracking/monitoring configured
   - [ ] Performance monitoring implemented
   - [ ] Data retention policy defined
   - [ ] Privacy compliance verified (GDPR/CCPA)

10. **Event Tracking Specification**
    For developers to implement - specify ALL events needed:
    
    **User Lifecycle Events:**
    - `user_signup` (properties: source, timestamp, user_id)
    - `onboarding_started` (properties: user_id, timestamp)
    - `onboarding_step_completed` (properties: user_id, step_name, timestamp)
    - `onboarding_completed` (properties: user_id, timestamp, time_to_complete)
    
    **Engagement Events:**
    - `session_start` (properties: user_id, timestamp, device, browser)
    - `session_end` (properties: user_id, timestamp, duration)
    - `page_view` (properties: user_id, page_name, timestamp)
    
    **Feature Usage Events:**
    - `feature_[name]_viewed` (properties: user_id, timestamp)
    - `feature_[name]_used` (properties: user_id, timestamp, context)
    - `workflow_started` (properties: user_id, workflow_name, timestamp)
    - `workflow_completed` (properties: user_id, workflow_name, timestamp, duration)
    
    **Value Events:**
    - `value_moment_achieved` (properties: user_id, timestamp, value_type)
    - `problem_solved` (properties: user_id, problem_type, timestamp)
    
    **Business Events:**
    - `payment_started` (properties: user_id, plan, timestamp)
    - `payment_completed` (properties: user_id, plan, amount, timestamp)
    - `subscription_created` (properties: user_id, plan, mrr, timestamp)
    - `subscription_cancelled` (properties: user_id, reason, timestamp)
    
    **Error/Quality Events:**
    - `error_occurred` (properties: user_id, error_type, error_message, timestamp)
    - `page_load_time` (properties: user_id, page, load_time, timestamp)

11. **Leading Indicators** (Early signals before full metrics mature)
    - Week 1: [Specific early signals to watch with exact tracking]
    - Week 2-4: [Signals that predict 90-day success with exact tracking]
    - What early patterns indicate success vs. failure?

12. **Lagging Indicators** (Final outcomes)
    - 90-day cohort retention
    - Customer LTV
    - Word-of-mouth growth rate
    - Revenue or business impact

13. **Qualitative Success Signals**
    - User testimonials or case studies showing clear value
    - Competitive wins or customers switching from competitors
    - Organic word-of-mouth or referrals
    - Partnership or integration interest from other companies
    - Media or analyst attention
    - Expansion opportunities (users asking for more features/tiers)

14. **Learning Questions & Validation**
    - Key question 1: [How we'll answer it and success criteria]
    - Key question 2: [How we'll answer it and success criteria]
    - Key question 3: [How we'll answer it and success criteria]
    - Assumption 1: [How we'll validate and what confirms/refutes it]
    - Assumption 2: [How we'll validate and what confirms/refutes it]

15. **Decision Framework**
    - **Success** (Clear signal to continue/invest): [Specific criteria]
    - **Qualified Success** (Proceed with adjustments): [Specific criteria]
    - **Inconclusive** (Need more time/data): [Specific criteria]
    - **Pivot Signal** (Change approach): [Specific criteria]
    - **Failure** (Stop): [Specific criteria]

16. **Review Cadence**
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

Create comprehensive success criteria with EXACT tracking implementation for our MVP.
```

---

**Version:** 1.1  
**Last Updated:** October 1, 2025  
**Status:** Updated with measurement implementation requirements