# Creating Test Cases & Tracking Project Progress

## Learning Objective

Understand the difference between test scenarios and test cases, identify the key components of a test case, and understand how Qase and Jira can be used to execute tests, maintain traceability, report defects, and track project progress within an Agile workflow.

---

## Key Concepts

- Test Scenarios
- Test Cases
- Test Case Components
- Test Execution
- Test Runs
- Regression Testing
- Requirement Traceability
- Qase–Jira Integration
- Defect Reporting
- Defect Triage
- Definition of Done

---

## My Understanding

I learned that a **test scenario** and a **test case** serve different purposes. A test scenario is a high-level description of what needs to be tested, while a test case provides the detailed steps and expected results needed to verify a specific behavior.

For example:

**Test Scenario:** Verify user login functionality.

**Test Case:** Verify that a user can successfully log in using valid email and password credentials.

I also learned that test cases can contain several components, including preconditions, test steps, expected results, postconditions, and additional metadata such as severity, status, behavior type, and testing type.

Test cases can be grouped into **Test Runs** for execution. Their results can be recorded as Passed, Failed, Blocked, Skipped, or Invalid. Previously created test cases can also be executed again during regression testing to verify that existing functionality continues to work after changes.

A single User Story can have multiple test cases because different scenarios and conditions may need to be verified.

---

## QA Perspective

As a QA Engineer, creating detailed and traceable test cases helps ensure that requirements are properly verified and that testing can be repeated consistently.

The relationship between requirements, test cases, execution, and defects can be represented as:

**User Story / Requirement**  
↓  
**Multiple Test Cases**  
↓  
**Test Execution / Test Run**  
↓  
**Pass / Fail Result**  
↓  
**Defect, if applicable**

A failed test does not automatically mean that there is a defect. The tester should investigate the failure and determine whether it was caused by an actual product issue, incorrect test data, an environment problem, or another factor.

If an actual defect is confirmed, it can be reported through the team's defect-tracking process, such as creating a Bug in Jira. The defect can then be associated with the failed test case and affected User Story to maintain traceability.

Defects may also go through **triage**, where the team evaluates factors such as severity, priority, ownership, and resolution.

---

## Real-World Examples

### Test Scenario and Test Case

- **Test Scenario:** Verify user login functionality.
- **Test Case:** Verify successful login using valid email and password.
- **Negative Test Case:** Verify login is rejected when an incorrect password is entered.
- **Edge Case:** Verify login behavior when the password reaches the maximum allowed length.

### Test Case Structure

- **Precondition:** A registered user account exists.
- **Step:** Enter a valid email address.
- **Expected Result:** The email is accepted.
- **Step:** Enter the correct password.
- **Expected Result:** The password is accepted.
- **Step:** Click the Login button.
- **Expected Result:** The user is successfully logged in and redirected to the dashboard.

### Defect Flow

**User Story:** User Login  
↓  
**TC-001:** Verify login with valid credentials  
↓  
**Execution:** Failed  
↓  
**Investigation:** Confirmed application defect  
↓  
**BUG-001:** Login accepts an incorrect password  
↓  
**Linked to User Story and Failed Test Case**

### Definition of Done

Depending on the team's agreed Definition of Done, a User Story may require:

- Development completed
- Required sub-tasks completed
- Acceptance criteria satisfied
- Testing completed
- Required regression testing completed
- Critical defects resolved

The exact Definition of Done depends on the team's process and agreement.

---

## Interview Questions

- What is the difference between a test scenario and a test case?
- What information is typically included in a test case?
- What are preconditions and postconditions?
- What is a test run?
- What is the difference between a test case and a test run?
- What does Passed, Failed, Blocked, Skipped, or Invalid mean during test execution?
- What is regression testing?
- Can one User Story have multiple test cases?
- Does a failed test automatically mean there is a defect?
- What should a tester do when a test fails?
- How does Qase–Jira integration improve traceability?
- How can a defect be linked to a test case and User Story?
- What is defect triage?
- What is the Definition of Done?
- When can a User Story be considered Done?

---

## Key Takeaways

- A **test scenario describes what to test**, while a **test case describes how to test it**.
- Test cases provide detailed, repeatable instructions for verifying expected behavior.
- A single User Story can have **multiple test cases** covering different conditions and scenarios.
- Test Runs allow multiple test cases to be executed and their results tracked together.
- A failed test should be investigated before concluding that a defect exists.
- Confirmed defects can be linked to the failed test case and affected User Story to maintain traceability.
- Regression testing re-executes existing tests after changes to verify that previously working functionality has not been broken.
- Defect triage helps the team determine the severity, priority, ownership, and resolution of reported defects.
- A User Story is considered Done when it satisfies the team's agreed **Definition of Done**.
- Qase and Jira can work together to provide traceability across **requirements → test cases → test execution → defects**.
