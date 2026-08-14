# Test Case Fundamentals & Setup

## Objective

Understand the purpose and structure of test cases, distinguish test cases from test scenarios, and prepare a structured document for writing and executing test cases.

## 1. Test Case Writing Approaches

Projects may use different approaches to test documentation:

- **Test Scenarios Only** — High-level scenarios are created and executed directly.
- **Test Cases Only** — Detailed test cases are created directly from requirements.
- **Both** — High-level scenarios are created first and then expanded into detailed test cases.

The appropriate approach depends on project complexity, risk, time, team practices, and required traceability.

## 2. Test Scenario vs. Test Case

### Test Scenario

A high-level description of what needs to be tested.

Example:

> Verify login functionality using valid credentials.

Test scenarios are generally:

- Quick to create.
- Useful for defining test coverage.
- Less detailed than test cases.

### Test Case

A detailed set of conditions, steps, test data, and expected results used to verify a specific behavior.

### Key Difference

**Scenario = What to test**

**Test Case = How to test it**

## 3. Key Test Case Fields

### Title

A concise description of what is being tested.

Example:

> Verify login with valid username and password

The title should be specific enough to distinguish the test case from other tests.

### Preconditions

Conditions that must be satisfied before execution.

Example:

> User has an existing account with valid credentials.

### Test Steps

The sequential actions required to execute the test.

Example:

1. Navigate to the Login page.
2. Enter a valid username.
3. Enter a valid password.
4. Click Login.

Steps should be clear, actionable, and consistently written.

### Expected Result

Describes what the system should do.

Example:

> User is successfully logged in and redirected to the Home page.

Expected behavior should be based on requirements and defined system behavior.

### Test Suite / Folder

Used to organize related test cases.

Examples:

- Login
- Sign Up
- Cart
- Checkout
- Payment

Depending on the tool, this may also be referred to as a module, feature, folder, or test condition.

### Test Environment

Describes the hardware, software, platform, or environment required for testing.

Examples:

- Windows
- Chrome
- Android
- iOS
- Staging server

### Actual Result

Records what actually happened during execution.

The Actual Result is generally left blank during the test design phase and populated during execution.

## 4. Test Case Execution Statuses

Common execution statuses include:

| Status | Meaning |
|---|---|
| Ready to Test | Test case is designed but has not yet been executed. |
| Pass | Actual behavior matches the expected result. |
| Fail | Actual behavior differs from the expected result. |
| Blocked | A dependency or prerequisite prevents execution. |
| Skipped | The test was intentionally not executed. |

A failed test may result in a defect being logged for investigation.

## 5. Preparing Google Sheets

Google Sheets can be used as a simple and collaborative tool for test case management.

### Project Information Sheet

The first tab can contain high-level project information such as:

- Project Name
- Test Case Designer
- Team Members
- Target Platform / OS Version
- Server / Base URL
- Delivery Date

This provides context for the test documentation.

### Test Suite Tabs

Separate tabs can be created for different application areas.

Examples:

- Sign Up
- Login
- Cart
- Checkout
- Payment

Existing tabs can be duplicated and renamed to quickly create additional test suites.

## 6. Test Case Sheet Structure

A test case sheet may contain fields such as:

- Test Case ID
- Test Case Title
- Preconditions
- Test Steps
- Test Data
- Expected Result
- Actual Result
- Status
- Environment

The exact structure should be adapted to the project's requirements and team standards.

## 7. Formatting Test Cases

Google Sheets can be formatted to improve readability and organization.

Examples:

- Use bold formatting for test case titles.
- Number test steps sequentially.
- Use line breaks within cells when necessary.
- Separate expected results from test steps when individual step verification is required.
- Merge expected-result cells when only the final outcome needs to be recorded.

## 8. Test Case Status Tracking

Dropdown lists can be used to standardize execution statuses.

Example:

> Ready to Test → Pass / Fail / Blocked / Skipped

Additional project-specific statuses can be added when required.

## 9. Environment & Multi-Run Coverage

Test cases may need to be executed across multiple devices, browsers, operating systems, or environments.

Examples:

- Chrome / Windows
- Safari / macOS
- iPhone
- Android
- Staging environment

Separate execution or status columns can be used to track results across different configurations.

## 10. Using a View-Only Test Case Template

When a shared instructor document is provided as View-Only:

1. Open the provided document.
2. Sign in to a Google account.
3. Select **File → Make a copy**.
4. Save the copy to your own Google Drive.
5. Use the copied document as the editable test case template.

The original shared document should remain unchanged.

## 11. Test Case Traceability

Test cases can be connected to the scenarios from which they were created.

Example:

**Requirement**

↓  

**Test Scenario**

↓  

**Test Case**

↓  

**Test Execution**

↓  

**Pass / Fail / Blocked**

↓  

**Defect (if required)**

Maintaining this relationship improves test coverage and makes it easier to identify which requirements and scenarios have been tested.

## Key Takeaways

- A test scenario describes **what should be tested**.
- A test case provides the detailed information needed to execute the test.
- Test cases should contain clear steps and measurable expected results.
- Preconditions define what must already be true before execution.
- Actual results are recorded during execution.
- Google Sheets can be used to organize test cases and execution statuses.
- Test cases can be organized into suites or application modules.
- Test cases should be traceable to their corresponding scenarios and requirements.
- The level of test case detail should depend on project requirements, risk, and team standards.
