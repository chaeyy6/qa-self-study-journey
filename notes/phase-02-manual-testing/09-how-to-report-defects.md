# How to Report Defects

## What is a Defect?

In Software Quality Assurance, Defect, Bug, and Issue are commonly used interchangeably.

A defect occurs when the system's actual behavior differs from the expected behavior.

> Defect = Expected Behavior ≠ Actual Behavior

### Expected Behavior

The behavior that the software is supposed to produce according to project artifacts such as:

- User Stories
- Requirements Documents
- Design Specifications
- Product Owner instructions

### Actual Behavior

The behavior that actually occurs when the tester executes the software.

### Types of Defects

#### Functional Defect
The system does not perform an expected function.

Example:
> Clicking the Submit button does nothing.

#### Performance Defect
The system performs the expected operation but takes an unreasonable amount of time according to the expected behavior or requirements.

#### Data Integrity Defect
The system stores, displays, or processes incorrect, missing, or corrupted data.

---

## Anatomy of a High-Quality Defect Report

A good defect report should be self-contained so that developers can understand, reproduce, investigate, and fix the issue without requiring additional clarification.

### Title

A concise and descriptive summary of the defect.

**Good:**
> Submit button is unresponsive on Login Page

**Bad:**
> Login Problem

### Priority

Indicates how urgently the defect should be addressed.

- High
- Medium
- Low

### Environment

Describes the hardware and software environment where the defect occurred.

Examples:

- Staging server
- Windows 11
- Chrome
- iPhone 14

### Steps to Reproduce

The actions required to trigger the defect.

Example:

1. Navigate to `/login`.
2. Enter valid user credentials.
3. Click Submit.
4. Observe the page.

### Expected Result

Describes what should have happened according to the applicable requirements or specifications.

Example:

> User is redirected to the Dashboard after clicking Submit.

### Actual Result

Describes what actually happened during execution.

Example:

> The page remains static and no response or error message is displayed.

### Attachments

Provide supporting evidence when appropriate.

- **Screenshots:** Useful for static UI defects.
- **Videos:** Useful for dynamic or behavioral defects.
- **Logs:** Useful for API, server-side, network, and data-related issues.

### Status

Tracks the defect's lifecycle.

Example:

> New → In Progress → Pending Retest → Closed / Reopened

---

## False Positives

A false positive occurs when a reported issue turns out not to be an actual software defect.

Possible causes include:

- Environment problems
- Outdated configurations
- Incorrect test execution
- Tester misunderstanding

QA should investigate unexpected behavior carefully before assuming that every issue is a software defect.

---

## Retesting Hygiene

Detailed defect reports make future retesting easier.

When a developer reports that a defect has been fixed, QA needs to reproduce the original conditions to verify the fix.

A detailed report containing:

- Environment
- Steps to Reproduce
- Expected Result
- Actual Result
- Evidence

allows the tester to reproduce the original problem more reliably without depending on memory.

---

## Key Takeaways

- A defect occurs when actual behavior differs from expected behavior.
- Defect reports should be clear, descriptive, and reproducible.
- Expected and actual results should be clearly separated.
- Environment information can help developers reproduce defects.
- Screenshots, videos, and logs can provide valuable supporting evidence.
- Defects can have different priorities depending on their impact and urgency.
- False positives should be investigated before being treated as genuine defects.
- Good defect documentation makes future retesting more efficient.
