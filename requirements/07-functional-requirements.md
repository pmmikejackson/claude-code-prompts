# Functional Requirements Prompt

## Overview
This prompt defines detailed functional requirements - what the system must do. Use this after Definition of Done and Success Criteria to translate high-level features into specific, implementable requirements.

## TASK
You are a product manager writing functional requirements for the MVP. Your goal is to clearly specify what the system must do, including user interactions, business logic, data handling, and integrations. Requirements must be clear enough for developers to implement without ambiguity.

## CONSTRAINTS
- Every requirement must be specific, testable, and unambiguous
- Use "The system shall..." format for each requirement
- Include acceptance criteria for each requirement
- Prioritize requirements (Must Have, Should Have, Could Have)
- Consider security and data sovereignty in every requirement
- Requirements must map to the core features from Solution Synthesis
- Focus on MVP scope only - defer nice-to-haves
- Each requirement should be independently implementable and testable

## INPUTS REQUIRED
Before starting, you need:
1. **Solution Concept** - From Solution Synthesis
2. **Definition of Done** - What's in scope for MVP
3. **User Research** - User workflows and pain points
4. **Success Criteria** - What needs to be tracked/measured

## QUESTIONS TO ANSWER

### 1. User Management & Authentication
- How do users sign up?
- What authentication methods are supported?
- What user data must be collected?
- How is user identity verified?
- What password/security requirements exist?
- How do users recover accounts?

### 2. Core User Workflows
- What are the primary user workflows?
- What actions can users take?
- What is the step-by-step flow for each workflow?
- What data is created, read, updated, or deleted?
- What validations are required?
- What are the success and error states?

### 3. Data Management
- What data does the system store?
- What is the data model/schema?
- What data relationships exist?
- How is data validated?
- What data can users export?
- What data retention policies exist?

### 4. Integrations
- What external systems must be integrated?
- What data flows between systems?
- What APIs must be called?
- What happens if integrations fail?
- What authentication is required for integrations?

### 5. Notifications & Communication
- What notifications must be sent?
- What triggers notifications?
- What channels are used (email, in-app, SMS)?
- What is the notification content?
- Can users configure notification preferences?

### 6. Search & Filtering
- What can users search for?
- What filters are available?
- What is the search algorithm?
- How are results ranked?
- What are the performance requirements?

### 7. Permissions & Access Control
- What roles exist in the system?
- What can each role do?
- How are permissions enforced?
- Can permissions be customized?
- What happens when users lack permission?

### 8. Analytics & Tracking
- What user actions must be tracked?
- What events are logged?
- What data is sent to analytics?
- How is user privacy protected?
- What opt-out mechanisms exist?

## EXPECTED RESULTS

Produce a functional requirements document containing:

1. **Document Overview**
   - Product name and version
   - Purpose of this document
   - Scope (what's included/excluded)
   - Intended audience

2. **User Personas & Use Cases**
   - Brief summary of target users (from User Research)
   - Primary use cases for each persona
   - User goals and workflows

3. **Functional Requirements by Feature Area**

   For each feature area, provide:

   ### Feature Area: [Name]
   
   **Overview:** Brief description of this feature area
   
   **User Stories:**
   - As a [user type], I want to [action] so that [benefit]
   - As a [user type], I want to [action] so that [benefit]
   
   **Requirements:**
   
   **FR-[AREA]-001: [Requirement Title]** (Priority: Must Have / Should Have / Could Have)
   
   The system shall [specific requirement].
   
   **Acceptance Criteria:**
   - [ ] Given [context], when [action], then [expected result]
   - [ ] Given [context], when [action], then [expected result]
   
   **Dependencies:** [Other requirements this depends on, if any]
   
   **Notes:** [Any additional context, edge cases, or clarifications]
   
   ---

4. **Example Feature Areas to Cover:**

   ### FR-100: User Registration & Authentication
   - FR-101: User signup
   - FR-102: Email verification
   - FR-103: Login
   - FR-104: Password reset
   - FR-105: Session management
   - FR-106: Logout
   
   ### FR-200: User Profile Management
   - FR-201: View profile
   - FR-202: Edit profile
   - FR-203: Upload profile picture
   - FR-204: Account settings
   - FR-205: Delete account
   
   ### FR-300: [Core Feature 1 - specific to your product]
   - FR-301: [Specific capability]
   - FR-302: [Specific capability]
   - etc.
   
   ### FR-400: [Core Feature 2 - specific to your product]
   - FR-401: [Specific capability]
   - FR-402: [Specific capability]
   - etc.
   
   ### FR-500: Data Management
   - FR-501: Create data
   - FR-502: Read/view data
   - FR-503: Update data
   - FR-504: Delete data
   - FR-505: Data validation
   - FR-506: Data export
   
   ### FR-600: Search & Filtering
   - FR-601: Search functionality
   - FR-602: Filter by criteria
   - FR-603: Sort results
   - FR-604: Pagination
   
   ### FR-700: Notifications
   - FR-701: Email notifications
   - FR-702: In-app notifications
   - FR-703: Notification preferences
   - FR-704: Notification history
   
   ### FR-800: Analytics & Tracking
   - FR-801: Event tracking
   - FR-802: User behavior analytics
   - FR-803: Conversion tracking
   - FR-804: Privacy controls
   
   ### FR-900: Integrations
   - FR-901: [Integration 1]
   - FR-902: [Integration 2]
   - FR-903: Webhook support
   - FR-904: API access

5. **Data Model Overview**
   
   Define key entities and their relationships:
   
   **Entity: User**
   - user_id (primary key)
   - email (unique, required)
   - password_hash (required)
   - created_at (timestamp)
   - last_login (timestamp)
   - etc.
   
   **Entity: [Core Data Object]**
   - [Define fields, types, constraints]
   
   **Relationships:**
   - User → [Data Object] (one-to-many)
   - etc.

6. **API Requirements** (if applicable)
   
   Define key API endpoints needed:
   
   **POST /api/v1/users/signup**
   - Purpose: Create new user account
   - Request body: { email, password }
   - Response: { user_id, token }
   - Status codes: 201 (success), 400 (validation error), 409 (email exists)
   
   **GET /api/v1/[resource]**
   - Purpose: [Description]
   - Parameters: [List]
   - Response: [Format]
   - etc.

7. **Business Rules**
   
   Document key business logic:
   
   - BR-001: Passwords must be at least 12 characters with uppercase, lowercase, number, and symbol
   - BR-002: Users must verify email within 24 hours or account is deleted
   - BR-003: Free tier users can create up to 10 [items]
   - BR-004: [Specific business rule]
   - etc.

8. **User Interface Requirements**
   
   Key UI/UX requirements:
   
   - UI-001: All forms must show inline validation errors
   - UI-002: Loading states must be shown for operations taking >500ms
   - UI-003: Success/error messages must be displayed for all user actions
   - UI-004: Primary actions must use [color] buttons
   - UI-005: Destructive actions must require confirmation
   - etc.

9. **Error Handling Requirements**
   
   - ERR-001: All errors must be logged with user_id, timestamp, and context
   - ERR-002: User-facing error messages must be clear and actionable
   - ERR-003: System errors must not expose sensitive information
   - ERR-004: Users must be able to retry failed operations
   - etc.

10. **Data Validation Requirements**
    
    - VAL-001: Email addresses must be validated against RFC 5322 format
    - VAL-002: All user input must be sanitized to prevent XSS
    - VAL-003: File uploads must validate file type and size
    - VAL-004: Numeric inputs must validate min/max ranges
    - etc.

11. **Requirements Traceability Matrix**
    
    | Requirement ID | User Story | Priority | Success Metric | Test Case |
    |---------------|-----------|----------|----------------|-----------|
    | FR-101 | As a user, I want to sign up | Must Have | Activation rate | TC-101 |
    | FR-301 | As a user, I want to [action] | Must Have | Feature usage % | TC-301 |
    | etc. | | | | |

12. **Out of Scope**
    
    Explicitly list what is NOT included in MVP:
    - [Feature deferred to v2]
    - [Feature deferred to v2]
    - [Integration deferred to v2]
    - etc.

13. **Assumptions & Dependencies**
    
    - Assumption 1: Users have internet connectivity
    - Assumption 2: Users access via modern browsers (Chrome, Firefox, Safari latest 2 versions)
    - Dependency 1: [External service] API must be available
    - Dependency 2: Payment processor integration
    - etc.

## FORMATTING GUIDELINES

**Requirement Statement Format:**
- Use "The system shall..." or "The user shall be able to..."
- Be specific and measurable
- Avoid ambiguous words like "fast", "easy", "user-friendly"
- Use active voice

**Good Examples:**
- ✅ "The system shall send a verification email within 30 seconds of user signup"
- ✅ "Users shall be able to filter results by date range, status, and category"
- ✅ "The system shall validate email format before account creation"

**Bad Examples:**
- ❌ "The system should work well"
- ❌ "Users can do stuff with data"
- ❌ "Fast performance"

## Usage Example

```
Claude, write functional requirements using this prompt.

Here's our solution concept: [paste]
Here's our Definition of Done: [paste]
Here's our user research: [paste]
Here's our success criteria: [paste]

Create comprehensive, implementable functional requirements for our MVP.
```

---

**Version:** 1.0  
**Last Updated:** October 1, 2025  
**Status:** Initial Draft - To be refined through real-world use