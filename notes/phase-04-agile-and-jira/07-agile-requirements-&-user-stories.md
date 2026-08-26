# Agile Requirements & User Stories

## Learning Objective

Understand how Agile requirements are organized from high-level business goals into smaller, testable user stories, and learn how the INVEST technique can be used to evaluate the quality of a user story.

---

## Key Concepts

- Agile Requirement Hierarchy
- Themes
- Features
- Epics
- User Stories
- Tasks / Sub-tasks
- Acceptance Criteria
- Given-When-Then
- INVEST Technique
- Requirement Testability
- Tester's Role in Agile Requirements

---

## My Understanding

Agile requirements can be organized from larger business goals into smaller and more manageable pieces of work.

A common hierarchy is:

**Theme → Feature → Epic → User Story → Task / Sub-task**

A **Theme** represents a high-level business goal or strategic objective.

A **Feature** represents a distinct piece of functionality that provides value to users.

An **Epic** is a large requirement that groups related user stories and may require multiple Sprints to complete.

A **User Story** describes a specific requirement from the perspective of a user.

A **Task or Sub-task** represents a smaller piece of work required to complete a user story.

### User Story Format

A common User Story structure is:

> **As a [type of user], I want to [action] so that [benefit/goal].**

Example:

> "As a new app user, I want to create an account using my email so that I can save my preferences."

This identifies:

- **Who:** New app user
- **What:** Create an account using email
- **Why:** Save preferences

### Acceptance Criteria

Acceptance Criteria define the conditions that must be satisfied for a User Story to be considered complete and acceptable.

A common format is **Given-When-Then**:

- **Given:** Initial condition or context.
- **When:** Action performed.
- **Then:** Expected result.

Example:

> **Given** the user is on the registration page,  
> **When** they enter a valid email and submit,  
> **Then** the application sends a verification email and redirects the user to the welcome screen.

---

## QA Perspective

Testers should participate in requirements discussions rather than waiting until development is finished.

Testers can collaborate with Product Owners, Business Analysts, and Developers to:

- Understand requirements.
- Clarify expected behavior.
- Review acceptance criteria.
- Identify ambiguities.
- Identify risks.
- Identify test conditions.
- Determine whether a story is testable.

A tester should be able to answer:

> **"How will we know that this requirement has been successfully implemented?"**

If the requirement cannot be verified objectively, it may need clarification before development begins.

---

## INVEST Technique

INVEST is a checklist used to evaluate the quality of a User Story.

### I — Independent

The User Story should be as independent as reasonably possible from other stories.

This reduces unnecessary dependencies and allows stories to be prioritized, developed, and tested more flexibly.

### N — Negotiable

The User Story should describe what the user needs and why rather than unnecessarily prescribing the technical implementation.

### V — Valuable

The User Story should provide meaningful value to the user or business.

### E — Estimable

The User Story should contain enough information for the team to estimate the effort required for development and testing.

### S — Small

The User Story should be small enough to be developed and tested within a reasonable timeframe.

Large requirements should be broken into smaller stories.

### T — Testable

The User Story must have clear, verifiable conditions that allow the team to determine whether the requirement has been successfully implemented.

---

## Real-World Example

Consider the following User Story:

> "As a customer, I want to pay for my bills so I can settle what I owe quickly."

This requirement is too broad to be an effective single User Story.

It may be:

- Difficult to estimate.
- Too large.
- Difficult to test because important rules are missing.

It may actually represent an **Epic**.

It can be broken into smaller stories:

### Story 1 — View Bill

> "As a customer, I want to view my itemized bill so that I can see the total amount before paying."

### Story 2 — Start Payment

> "As a customer, I want to select a 'Pay Now' option on my bill so that I can start the payment process immediately."

### Story 3 — Pay by Credit Card

> "As a customer, I want to enter my Visa or Mastercard details so that I can pay using my preferred card."

Breaking large requirements into smaller stories makes them easier to understand, estimate, develop, and test.

---

## Using Acceptance Criteria

Acceptance Criteria make User Stories more testable.

Example:

**Given** the customer is on the payment screen,

**When** they enter valid Visa or Mastercard details and submit the payment,

**Then** the payment should be processed according to the defined performance requirement and a confirmation receipt should be displayed.

Another scenario:

**Given** the customer is on the payment screen,

**When** they enter an invalid card number,

**Then** an appropriate error message should be displayed and the customer's funds should not be deducted.

Acceptance Criteria should be based on actual business requirements.

Testers can suggest scenarios and questions, but business rules should be confirmed by the appropriate stakeholders.

---

## AI for Requirement Review

AI tools such as ChatGPT can assist with reviewing User Stories.

AI can help identify:

- Stories that appear too broad.
- Missing information.
- Potential ambiguities.
- Possible acceptance criteria.
- Potential edge cases.
- INVEST characteristics that may not be satisfied.

However, AI should not replace communication with the Product Owner, Business Analyst, or other business stakeholders.

AI can suggest possible requirements, but the actual business rules must be confirmed by the people responsible for the product.

---

## Interview Questions

- What is a User Story?
- What is the typical format of a User Story?
- What is an Epic?
- What are Acceptance Criteria?
- What is the Given-When-Then format?
- What does INVEST stand for?
- Why should a User Story be Independent?
- What does Negotiable mean in INVEST?
- Why should a User Story be Valuable?
- Why should a User Story be Estimable?
- Why should a User Story be Small?
- Why should a User Story be Testable?
- What is the role of a tester in Agile requirements?
- How can a tester determine whether a requirement is testable?
- How can a large User Story be broken down?
- Can AI define the actual business requirements?

---

## Key Takeaways

- Agile requirements can be broken down from larger goals into smaller pieces of work.
- A common hierarchy is **Theme → Feature → Epic → User Story → Task/Sub-task**.
- A User Story describes **who needs something, what they need, and why**.
- Acceptance Criteria define the conditions that must be satisfied for a User Story to be accepted.
- **Given-When-Then** is a common format for expressing Acceptance Criteria.
- INVEST provides a checklist for evaluating User Stories.
- **I — Independent**
- **N — Negotiable**
- **V — Valuable**
- **E — Estimable**
- **S — Small**
- **T — Testable**
- Large requirements should be broken into smaller User Stories when they are too broad to estimate, develop, or test effectively.
- Testers should participate in requirements discussions early to identify ambiguity, risks, and testability issues.
- AI can assist with requirement review, but business stakeholders remain responsible for defining and confirming actual business rules.
