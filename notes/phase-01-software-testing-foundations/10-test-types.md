# Test Types

## Overview

Software testing can be classified in different ways depending on **what is being tested**, **how the testing is performed**, and **the purpose of the test**.

Understanding these testing types helps QA Engineers choose the appropriate testing approach for different situations throughout the Software Development Life Cycle (SDLC).

---

# Functional Testing

## Definition

Functional Testing verifies that the software behaves according to its specified functional requirements.

It focuses on **what the system does**.

## Example

- Verify that a user can successfully log in using valid credentials.
- Verify that invalid credentials display the correct error message.

## Work Products

- Requirements
- User Stories
- Use Cases
- Business Rules

## Responsibility

- Software Testers
- Developers (during Unit Testing)

---

# Non-Functional Testing

## Definition

Non-Functional Testing evaluates **how well** the system performs rather than **what** it does.

Common quality characteristics include:

- Performance
- Security
- Reliability
- Usability

## Example

Verify that the homepage loads within two seconds while handling 1,000 concurrent users.

## Work Products

- Executable System
- Performance Requirements
- Security Requirements
- Usability Requirements

## Responsibility

- Performance Engineers
- Security Engineers
- Specialized Testers
- Sometimes DevOps Engineers

---

# Black-Box Testing

## Definition

Black-Box Testing evaluates software without knowledge of its internal implementation.

The tester only provides inputs and verifies the outputs against the expected behavior.

## Example

Submit a registration form and verify whether the appropriate success or error message appears.

## Work Products

- Requirements
- Specifications
- UI Designs
- User Stories

## Responsibility

- Software Testers

---

# White-Box Testing

## Definition

White-Box Testing evaluates software with knowledge of its internal code, logic, branches, and architecture.

## Example

Create unit tests that execute every branch of an `if-else` statement.

## Work Products

- Source Code
- Internal Logic
- Architecture

## Responsibility

- Developers

---

# Dynamic Testing

## Definition

Dynamic Testing is performed by executing the software and observing its behavior.

Dynamic Testing includes both:

- Black-Box Testing
- White-Box Testing

## Example

Execute the checkout process and verify that an order is successfully placed.

---

# Static Testing

## Definition

Static Testing evaluates work products **without executing the software**.

Examples include:

- Requirements Review
- Design Review
- Code Review
- Test Case Review
- Test Plan Review

Static Testing helps identify defects early before implementation.

---

## Static vs Dynamic Testing

| Static Testing | Dynamic Testing |
|----------------|-----------------|
| Software is **not executed** | Software is **executed** |
| Reviews documents and code | Executes the application |
| Finds defects early | Validates software behavior |

### Examples

| Reviewing | Running Software |
|-----------|------------------|
| Code Review → Static Testing | White-Box Testing → Dynamic Testing |
| Requirements Review → Static Testing | Black-Box Testing → Dynamic Testing |

---

# Retesting (Confirmation Testing)

## Definition

Retesting verifies that a previously reported defect has been successfully fixed.

## Focus

Only the **previously failed test case**.

## Example

Re-run the Login test after fixing the password validation bug.

---

# Regression Testing

## Definition

Regression Testing ensures that recent code changes have **not introduced new defects** into existing functionality.

## Scope

**Impact-based**

Focuses on:

- Related modules
- Integrated components
- Existing functionality affected by the change

## Example

A bug is fixed in the Cart module.

Regression Testing verifies that Checkout, Payment, Inventory, and other related modules continue to function correctly.

---

# Smoke Testing

## Definition

Smoke Testing is a **broad but shallow** verification performed on a new software build to determine whether it is stable enough for detailed testing.

## Scope

Tests one basic scenario from each critical module.

Examples:

- Login
- Registration
- Dashboard
- Search
- Checkout

## Purpose

Determine whether the build is stable enough for further testing.

---

# Sanity Testing

## Definition

Sanity Testing is a **narrow but deep** verification performed after a bug fix or feature update.

## Scope

Tests multiple scenarios within the modified module only.

## Example

After redesigning the Checkout module, verify:

- Credit Card Payment
- PayPal Payment
- Discounts
- Taxes
- Order Summary

## Purpose

Confirm that the modified functionality works correctly before proceeding with Regression Testing.

---

# Smoke vs Sanity vs Regression

| Testing Type | Scope | Focus | Purpose |
|--------------|-------|-------|---------|
| **Smoke Testing** | Broad + Shallow | Critical modules | Verify the build is stable enough for testing |
| **Sanity Testing** | Narrow + Deep | Modified module | Verify a fix or enhancement works correctly |
| **Regression Testing** | Impact-Based | Related existing functionality | Ensure recent changes did not break existing features |

---

# Key Takeaways

- Functional Testing verifies **what** the software does.
- Non-Functional Testing verifies **how well** the software performs.
- Black-Box Testing uses inputs and outputs without code knowledge.
- White-Box Testing requires knowledge of the source code.
- Static Testing reviews work products without executing software.
- Dynamic Testing requires executing the software.
- Retesting confirms that a reported defect has been fixed.
- Regression Testing ensures code changes have not affected existing functionality.
- Smoke Testing verifies the application's critical functionality before detailed testing.
- Sanity Testing validates a specific bug fix or modified feature before broader testing.

---

> **Summary**

Choosing the appropriate testing type depends on the objective of testing. Understanding the differences between Functional, Non-Functional, Static, Dynamic, Smoke, Sanity, Regression, and Retesting enables QA Engineers to design efficient testing strategies while ensuring software quality throughout the SDLC.
