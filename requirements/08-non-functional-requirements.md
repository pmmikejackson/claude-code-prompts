# Non-Functional Requirements Prompt

## Overview
This prompt defines non-functional requirements (NFRs) - how the system must perform. Covers security, performance, scalability, reliability, compliance, and data sovereignty. Given your focus on security and data sovereignty, these requirements are CRITICAL.

## TASK
You are a product manager with deep security and infrastructure expertise, writing non-functional requirements for a SaaS MVP. Your goal is to specify measurable quality attributes, security controls, compliance requirements, and operational characteristics. **Security and data sovereignty must be built in from day one, not bolted on later.**

## CONSTRAINTS
- All requirements must be specific and measurable (use numbers, not adjectives)
- Prioritize requirements (Critical, High, Medium, Low)
- Consider regulatory compliance from the start (GDPR, CCPA, SOC2, etc.)
- Balance security with usability - don't make the system unusable
- Every requirement must have a verification method
- Focus on MVP-appropriate requirements (don't over-engineer)
- **MANDATORY: Data sovereignty and user privacy are non-negotiable**

## INPUTS REQUIRED
Before starting, you need:
1. **Solution Concept** - What we're building
2. **User Research** - User expectations and technical context
3. **Market Analysis** - Competitive benchmarks
4. **Functional Requirements** - What the system does
5. **Definition of Done** - Quality gates

## QUESTIONS TO ANSWER

### 1. Security Requirements
- How is user data encrypted (at rest and in transit)?
- What authentication mechanisms are required?
- How are passwords stored?
- What session management is required?
- How is the system protected against common attacks (XSS, CSRF, SQL injection)?
- What audit logging is required?
- How are secrets and API keys managed?

### 2. Data Sovereignty & Privacy
- Where is user data stored geographically?
- Can users choose data residency?
- What data is collected and why?
- How long is data retained?
- How can users export their data?
- How can users delete their data?
- What compliance requirements apply?

### 3. Performance Requirements
- What are acceptable response times?
- What throughput is required?
- What are the concurrent user limits?
- What database query performance is required?
- What page load times are acceptable?

### 4. Scalability Requirements
- How many users must the system support initially?
- What is the growth projection?
- How will the system scale (vertical/horizontal)?
- What are the bottlenecks?

### 5. Reliability & Availability
- What uptime is required?
- What is acceptable downtime?
- What backup frequency is required?
- What is the recovery time objective (RTO)?
- What is the recovery point objective (RPO)?

### 6. Compliance Requirements
- What regulations apply (GDPR, CCPA, HIPAA, SOC2)?
- What audit requirements exist?
- What data breach notification is required?
- What terms of service/privacy policy requirements exist?

### 7. Monitoring & Observability
- What must be monitored?
- What alerts are required?
- What logging is required?
- What metrics must be tracked?

## EXPECTED RESULTS

Produce a non-functional requirements document containing:

1. **Document Overview**
   - Product name and version
   - Purpose and scope
   - Compliance posture (what regulations apply)

2. **Security Requirements**

   ### SEC-100: Authentication & Authorization
   
   **SEC-101: Password Security** (Priority: Critical)
   - The system shall enforce passwords with minimum 12 characters including uppercase, lowercase, numbers, and symbols
   - The system shall hash passwords using bcrypt with work factor of at least 12
   - The system shall never store passwords in plaintext
   - The system shall implement rate limiting of 5 failed login attempts per 15 minutes
   
   **Verification:** Security audit, penetration testing
   
   **SEC-102: Session Management** (Priority: Critical)
   - The system shall expire sessions after 24 hours of inactivity
   - The system shall use secure, httpOnly, sameSite cookies for session tokens
   - The system shall regenerate session IDs after login
   - The system shall invalidate all sessions on password change
   
   **Verification:** Security audit, automated testing
   
   **SEC-103: Multi-Factor Authentication** (Priority: High)
   - The system should support TOTP-based 2FA
   - The system should allow recovery codes generation
   - The system should require 2FA for sensitive operations
   
   **Verification:** Manual testing, security review
   
   ### SEC-200: Data Protection
   
   **SEC-201: Encryption at Rest** (Priority: Critical)
   - The system shall encrypt all user data at rest using AES-256
   - The system shall encrypt database backups
   - The system shall store encryption keys separately from encrypted data
   
   **Verification:** Infrastructure audit, compliance scan
   
   **SEC-202: Encryption in Transit** (Priority: Critical)
   - The system shall use TLS 1.3 or TLS 1.2 for all connections
   - The system shall enforce HTTPS for all web traffic
   - The system shall use HSTS headers with max-age of at least 1 year
   - The system shall achieve A+ rating on SSL Labs test
   
   **Verification:** SSL Labs scan, security audit
   
   **SEC-203: Data Sanitization** (Priority: Critical)
   - The system shall sanitize all user inputs to prevent XSS attacks
   - The system shall use parameterized queries to prevent SQL injection
   - The system shall validate and sanitize file uploads
   - The system shall implement Content Security Policy (CSP) headers
   
   **Verification:** Automated security testing, code review
   
   ### SEC-300: Access Control
   
   **SEC-301: Principle of Least Privilege** (Priority: Critical)
   - The system shall enforce role-based access control (RBAC)
   - The system shall restrict API access based on user permissions
   - The system shall log all access to sensitive data
   
   **Verification:** Access control testing, audit review
   
   ### SEC-400: Audit & Logging
   
   **SEC-401: Security Event Logging** (Priority: Critical)
   - The system shall log all authentication attempts (success and failure)
   - The system shall log all access to sensitive data
   - The system shall log all permission changes
   - The system shall log all data exports and deletions
   - The system shall retain security logs for at least 90 days
   
   **Verification:** Log review, compliance audit
   
   **SEC-402: Log Protection** (Priority: High)
   - The system shall protect logs from tampering
   - The system shall encrypt logs containing sensitive information
   - The system shall restrict access to logs to authorized personnel only
   
   **Verification:** Security audit
   
   ### SEC-500: Secrets Management
   
   **SEC-501: API Key Management** (Priority: Critical)
   - The system shall never commit secrets to version control
   - The system shall use environment variables or secrets management service for all secrets
   - The system shall rotate API keys at least annually
   - The system shall revoke compromised keys within 1 hour
   
   **Verification:** Code review, infrastructure audit

3. **Data Sovereignty & Privacy Requirements**

   ### PRIV-100: Data Residency
   
   **PRIV-101: Geographic Data Storage** (Priority: Critical)
   - The system shall store all user data in [specify region: US, EU, etc.]
   - The system shall not transfer user data outside of specified regions without explicit consent
   - The system shall document data residency in privacy policy
   
   **Verification:** Infrastructure audit, compliance review
   
   **PRIV-102: Data Localization** (Priority: High)
   - The system should allow users to choose data storage region [if applicable]
   - The system should clearly indicate where user data is stored
   
   **Verification:** Feature testing, user documentation review
   
   ### PRIV-200: Data Minimization
   
   **PRIV-201: Data Collection** (Priority: Critical)
   - The system shall collect only data necessary for core functionality
   - The system shall document purpose for all collected data
   - The system shall not collect sensitive personal information without explicit consent
   
   **Verification:** Data audit, privacy review
   
   **PRIV-202: Data Retention** (Priority: Critical)
   - The system shall retain user data only as long as necessary
   - The system shall delete inactive accounts after [specify period]
   - The system shall automatically purge deleted data after [specify period]
   
   **Verification:** Automated testing, data audit
   
   ### PRIV-300: User Rights
   
   **PRIV-301: Right to Access** (Priority: Critical)
   - The system shall allow users to download all their data in machine-readable format (JSON/CSV)
   - The system shall provide data export within 48 hours of request
   
   **Verification:** Feature testing, compliance audit
   
   **PRIV-302: Right to Deletion** (Priority: Critical)
   - The system shall allow users to delete their account and all associated data
   - The system shall complete account deletion within 30 days
   - The system shall confirm deletion to user via email
   
   **Verification:** Feature testing, data audit
   
   **PRIV-303: Right to Rectification** (Priority: High)
   - The system shall allow users to correct inaccurate personal data
   - The system shall update corrected data across all systems within 24 hours
   
   **Verification:** Feature testing
   
   ### PRIV-400: Consent Management
   
   **PRIV-401: Explicit Consent** (Priority: Critical)
   - The system shall obtain explicit consent before collecting personal data
   - The system shall document consent with timestamp and IP address
   - The system shall allow users to withdraw consent
   
   **Verification:** Feature testing, privacy audit
   
   **PRIV-402: Cookie Consent** (Priority: Critical)
   - The system shall obtain consent before setting non-essential cookies
   - The system shall allow users to manage cookie preferences
   - The system shall respect Do Not Track signals where applicable
   
   **Verification:** Cookie audit, privacy review

4. **Performance Requirements**

   ### PERF-100: Response Time
   
   **PERF-101: Page Load Time** (Priority: High)
   - The system shall load pages in under 2 seconds for 95th percentile
   - The system shall achieve First Contentful Paint (FCP) under 1.5 seconds
   - The system shall achieve Largest Contentful Paint (LCP) under 2.5 seconds
   
   **Verification:** Performance monitoring, real user monitoring (RUM)
   
   **PERF-102: API Response Time** (Priority: High)
   - The system shall respond to API requests in under 500ms for 95th percentile
   - The system shall respond to database queries in under 100ms for 95th percentile
   
   **Verification:** API monitoring, database performance monitoring
   
   ### PERF-200: Throughput
   
   **PERF-201: Concurrent Users** (Priority: High)
   - The system shall support at least [X] concurrent users without degradation
   - The system shall handle at least [Y] requests per second
   
   **Verification:** Load testing
   
   ### PERF-300: Resource Utilization
   
   **PERF-301: Database Performance** (Priority: High)
   - The system shall maintain database CPU utilization under 70% during peak load
   - The system shall maintain database connection pool utilization under 80%
   
   **Verification:** Database monitoring

5. **Scalability Requirements**

   ### SCALE-100: Growth Capacity
   
   **SCALE-101: User Growth** (Priority: High)
   - The system shall scale to support 10x user growth within 3 months
   - The system shall support horizontal scaling of application servers
   
   **Verification:** Architecture review, load testing
   
   **SCALE-102: Data Growth** (Priority: High)
   - The system shall support database growth to [X] TB
   - The system shall partition data to support scale
   
   **Verification:** Database architecture review

6. **Reliability & Availability Requirements**

   ### REL-100: Uptime
   
   **REL-101: Service Availability** (Priority: High)
   - The system shall maintain 99.0% uptime (allows ~7.2 hours/month downtime)
   - The system shall provide status page showing real-time availability
   
   **Verification:** Uptime monitoring, SLA tracking
   
   ### REL-200: Backup & Recovery
   
   **REL-201: Data Backup** (Priority: Critical)
   - The system shall perform automated backups every 24 hours
   - The system shall retain backups for at least 30 days
   - The system shall encrypt all backups
   - The system shall store backups in geographically separate location
   
   **Verification:** Backup testing, infrastructure audit
   
   **REL-202: Disaster Recovery** (Priority: Critical)
   - The system shall achieve Recovery Time Objective (RTO) of 4 hours
   - The system shall achieve Recovery Point Objective (RPO) of 24 hours
   - The system shall test disaster recovery procedures quarterly
   
   **Verification:** DR testing, incident simulation
   
   ### REL-300: Fault Tolerance
   
   **REL-301: Graceful Degradation** (Priority: High)
   - The system shall continue operating with reduced functionality if non-critical services fail
   - The system shall display clear error messages when functionality is unavailable
   - The system shall automatically retry failed operations with exponential backoff
   
   **Verification:** Chaos engineering, failure testing

7. **Compliance Requirements**

   ### COMP-100: GDPR Compliance (if applicable)
   
   **COMP-101: Data Protection Officer** (Priority: Critical)
   - The organization shall designate a Data Protection Officer [if required]
   - The system shall document data processing activities
   
   **Verification:** Compliance audit
   
   **COMP-102: Data Breach Notification** (Priority: Critical)
   - The system shall detect and report data breaches within 72 hours
   - The system shall maintain incident response procedures
   
   **Verification:** Incident response testing
   
   ### COMP-200: SOC 2 Compliance (if pursuing)
   
   **COMP-201: Security Controls** (Priority: High)
   - The system shall implement controls per SOC 2 Type II requirements
   - The system shall undergo annual SOC 2 audit [when appropriate]
   
   **Verification:** SOC 2 audit
   
   ### COMP-300: Industry-Specific Compliance
   
   **COMP-301: [Specific Regulation]** (Priority: depends on industry)
   - [Specific requirements based on industry: HIPAA, PCI-DSS, etc.]
   
   **Verification:** [Specific audit requirements]

8. **Monitoring & Observability Requirements**

   ### MON-100: System Monitoring
   
   **MON-101: Uptime Monitoring** (Priority: Critical)
   - The system shall monitor endpoint availability every 60 seconds
   - The system shall alert on-call team within 5 minutes of downtime
   
   **Verification:** Monitoring configuration review
   
   **MON-102: Performance Monitoring** (Priority: High)
   - The system shall track response times for all API endpoints
   - The system shall track database query performance
   - The system shall track error rates
   
   **Verification:** Monitoring dashboard review
   
   **MON-103: Security Monitoring** (Priority: Critical)
   - The system shall monitor for suspicious authentication patterns
   - The system shall alert on unusual data access patterns
   - The system shall monitor for security vulnerabilities
   
   **Verification:** Security monitoring review
   
   ### MON-200: Alerting
   
   **MON-201: Alert Configuration** (Priority: High)
   - The system shall alert on critical errors within 5 minutes
   - The system shall alert on degraded performance within 15 minutes
   - The system shall implement alert escalation for unacknowledged alerts
   
   **Verification:** Alert testing
   
   ### MON-300: Logging
   
   **MON-301: Application Logging** (Priority: High)
   - The system shall log all errors with stack traces
   - The system shall log all API requests and responses (excluding sensitive data)
   - The system shall implement structured logging (JSON format)
   
   **Verification:** Log review

9. **Usability & Accessibility Requirements**

   ### USA-100: Browser Support
   
   **USA-101: Browser Compatibility** (Priority: High)
   - The system shall support Chrome (latest 2 versions)
   - The system shall support Firefox (latest 2 versions)
   - The system shall support Safari (latest 2 versions)
   - The system shall support Edge (latest 2 versions)
   
   **Verification:** Cross-browser testing
   
   ### USA-200: Accessibility
   
   **USA-201: WCAG Compliance** (Priority: High)
   - The system shall meet WCAG 2.1 Level AA standards
   - The system shall be navigable by keyboard
   - The system shall provide alt text for all images
   - The system shall maintain sufficient color contrast ratios
   
   **Verification:** Accessibility audit, automated testing

10. **Maintainability Requirements**

    ### MAINT-100: Code Quality
    
    **MAINT-101: Code Standards** (Priority: High)
    - The codebase shall maintain automated test coverage of at least 70%
    - The codebase shall pass linting without errors
    - The codebase shall be documented with inline comments for complex logic
    
    **Verification:** Code review, CI/CD pipeline checks
    
    ### MAINT-200: Deployment
    
    **MAINT-201: Deployment Process** (Priority: High)
    - The system shall support zero-downtime deployments
    - The system shall support automated rollback on deployment failure
    - The system shall deploy to staging environment before production
    
    **Verification:** Deployment testing

11. **Requirements Priority Matrix**

    | ID | Requirement | Priority | Impact if Missing | Verification Method |
    |----|-------------|----------|-------------------|---------------------|
    | SEC-101 | Password security | Critical | Security breach | Security audit |
    | SEC-201 | Encryption at rest | Critical | Data exposure | Infrastructure audit |
    | PRIV-301 | Data export | Critical | Compliance violation | Feature testing |
    | PERF-101 | Page load time | High | User abandonment | Performance monitoring |
    | REL-201 | Data backup | Critical | Data loss | Backup testing |

12. **Compliance Checklist**

    - [ ] Privacy policy reviewed by legal
    - [ ] Terms of service reviewed by legal
    - [ ] Data processing agreement (DPA) prepared
    - [ ] Cookie policy implemented
    - [ ] GDPR requirements met (if applicable)
    - [ ] CCPA requirements met (if applicable)
    - [ ] Security controls documented
    - [ ] Incident response plan documented
    - [ ] Data breach notification procedures documented

13. **Testing Requirements**

    - Load testing: Must support [X] concurrent users
    - Security testing: Penetration test before launch
    - Performance testing: Must meet all PERF requirements
    - Disaster recovery testing: Quarterly
    - Backup restoration testing: Monthly
    - Accessibility testing: WCAG 2.1 Level AA audit

## Usage Example

```
Claude, write non-functional requirements using this prompt.

Here's what we're building: [paste solution concept]
Here's our functional requirements: [paste or summarize]
Here's our target users: [paste user research]
Here's our compliance needs: [GDPR, SOC2, etc.]

Create comprehensive NFRs with strong focus on security and data sovereignty.
```

---

**Version:** 1.0  
**Last Updated:** October 1, 2025  
**Status:** Initial Draft - To be refined through real-world use