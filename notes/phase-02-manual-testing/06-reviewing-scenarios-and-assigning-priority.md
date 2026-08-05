# Reviewing Scenarios and Assigning Priority

## Overview

Creating test scenarios is only the first step in the testing process. Before they can be executed or converted into test cases, QA Engineers must review the generated scenarios to ensure they are accurate, complete, non-duplicative, and aligned with the project requirements.

After reviewing the scenario list, testers assign priorities based on business impact and risk to determine which scenarios should be executed first.

---

## Reviewing Test Scenarios

Whether test scenarios are written manually or generated using AI, they should always be reviewed before use.

During the review, QA Engineers should verify that each scenario:

- Aligns with the documented requirements
- Covers the intended business process
- Does not duplicate another scenario
- Does not contain unsupported assumptions
- Is written clearly and consistently
- Provides sufficient test coverage

AI-generated scenarios should always be treated as draft output that requires human validation.

---

## Prompt Construction Best Practices

### Write Naturally

Prompt components such as Role, Context, Instruction, Input Data, Constraints, and Output Format do not have to be written as literal labels.

Instead, they can be expressed naturally in complete sentences.

Example:

> You are a Senior QA Engineer reviewing login requirements. Generate high-level test scenarios covering positive, negative, and edge cases.

---

### Start a New Conversation for New Tasks

When switching to a different feature or project, start a new AI conversation.

This helps prevent:

- Previous context affecting new outputs
- Irrelevant assumptions
- Mixed project information

---

## Handling Ambiguous Requirements

When business rules are missing from the requirements, QA Engineers should avoid making assumptions.

Instead of inventing undocumented values, write generic scenarios until clarification is obtained.

Example:

Requirement:

> Lock the account after multiple failed login attempts.

Instead of assuming:

> Lock the account for 30 minutes.

Write:

> Verify that the user can log in after the account lockout period ends.

The exact duration should be clarified with the Product Owner or Business Analyst.

---

## Validating Error Messages

How error messages are tested depends on the requirement.

### When the requirement specifies the exact message

Validate the exact text.

Example:

> "This coupon has expired and is no longer valid."

---

### When the requirement is generic

Verify that an appropriate error message is displayed without assuming the exact wording.

Example:

> Verify that an appropriate error message is displayed when payment fails.

---

## Reviewing AI Output

Multiple AI tools may generate different scenario lists.

Some teams compare outputs from multiple AI models to identify additional ideas and improve coverage.

The QA Engineer then:

1. Combines the generated scenarios.
2. Removes duplicate or overlapping scenarios.
3. Organizes them into logical categories.
4. Reviews them against the project requirements.

The final scenario list should always be reviewed by a tester before execution.

---

## Assigning Priority

Not every test scenario has the same importance.

Scenarios should be prioritized according to their business impact and associated risk.

| Priority | Focus Area | Examples |
|----------|------------|----------|
| **High** | Critical functionality, security, business-critical workflows | Login, Payment, Authentication, Authorization |
| **Medium** | Supporting functionality | Password Reset, Session Timeout, Account Lockout |
| **Low** | Edge cases and uncommon inputs | Special characters, Rapid button clicks |
| **Very Low** | Cosmetic or convenience behavior | Remembering field values, Minor UI preferences |

---

## Risk-Based Testing

Risk-based testing allows teams to focus on the areas that would have the greatest impact if they failed.

Risk is commonly evaluated using:

- Business impact
- Likelihood of failure

High-risk features are tested first because failures in these areas could significantly affect users or the business.

Examples include:

- User Authentication
- Payments
- Order Processing
- Data Security

---

## Final QA Review

Before creating test cases, QA Engineers should verify that every test scenario aligns with:

- Requirements
- Acceptance Criteria
- Business Rules
- Wireframes
- Figma Designs

After review, the finalized scenarios can be imported into test management tools such as:

- Jira
- Zephyr Scale
- Xray
- TestRail

---

## Best Practices

- Review every generated scenario before using it.
- Remove duplicate scenarios.
- Avoid undocumented assumptions.
- Clarify ambiguous requirements.
- Prioritize scenarios according to business risk.
- Focus testing effort on the highest-risk functionality first.

---

## Key Takeaways

- Test scenarios should always be reviewed before execution.
- AI-generated scenarios require human validation.
- Ambiguous requirements should lead to clarification—not assumptions.
- Scenario priority is determined by business impact and risk.
- High-priority scenarios should be executed before lower-priority ones.
- A reviewed and prioritized scenario list provides the foundation for creating effective test cases.
