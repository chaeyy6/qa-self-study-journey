# Zephyr Scale — Test Case Management

## Objective

Understand how Zephyr Scale supports test case management through configuration, test case reuse, parameterization, BDD/Gherkin, bulk operations, and test case lifecycle management.

## 1. Test Case Configuration

Zephyr Scale provides configuration options that allow teams to customize how test cases are organized and managed.

Examples include:

- Environments
- Labels
- Iterations
- Priorities
- Data Sets
- Statuses
- Custom Fields

Test cases can also be imported from or exported to external tools such as spreadsheets.

## 2. Reusing Test Cases with Call to Test

**Call to Test** allows an existing test case to be reused as part of another test case.

For example, a larger workflow could be structured as:

- Login
- Add to Cart
- Checkout
- Leave a Review

Instead of rewriting the same steps, existing test cases can be called from another test case.

### Benefits

- Reduces duplicated test steps.
- Improves test case maintenance.
- Supports modular test design.
- Allows common workflows to be reused across multiple tests.

## 3. Using Parameters

Parameters allow test cases to use reusable variables instead of hardcoded values.

For example:

```text
OTP = 1234
````

A parameter can then be referenced within a test step instead of directly entering the value.

Parameters can use default values or be overridden for specific scenarios.

### Benefits

* Reduces hardcoded test data.
* Improves test case reusability.
* Simplifies test maintenance.
* Makes it easier to perform different positive and negative tests.

## 4. BDD & Gherkin Test Cases

**Behavior-Driven Development (BDD)** focuses on describing application behavior in a structured and readable format.

Zephyr Scale supports **Gherkin** keywords such as:

* **Given** — Defines the initial context or state.
* **When** — Defines the action being performed.
* **Then** — Defines the expected result.
* **And** — Adds another condition, action, or result.

Example:

```text
Given the user is on the Cart page
When the user adds an item to the cart
Then the number of items in the cart increases
And the updated total price is displayed
```

BDD test cases can help connect requirements, manual testing, and automation.

## 5. Exporting Test Cases to Cucumber

BDD/Gherkin test cases can be exported from Zephyr Scale as `.feature` files for use with Cucumber.

This creates a connection between manual test documentation and automated testing.

The exported feature file contains the test scenario structure, but step definitions must still be implemented before the scenario can be executed as automated code.

## 6. Cloning Test Cases

Cloning allows an existing test case to be duplicated and used as the starting point for a new test case.

For example, a valid login test could be cloned and modified to create an invalid login test.

### Benefits

* Saves time when test cases have similar structures.
* Reduces repetitive test case creation.
* Allows the cloned test case to be modified independently.

The cloned test case does not carry over historical information such as execution history, comments, or linked defects.

## 7. Archiving & Deleting Test Cases

### Archiving

Archiving removes obsolete or temporary test cases from active use while preserving their historical information.

Archived test cases can be restored when necessary.

### Deleting

Deleting permanently removes a test case.

Deletion should be performed carefully because test cases with active dependencies may not be eligible for deletion.

### Key Difference

```text
Archive → Remove from active use while preserving history.

Delete → Permanently remove the test case.
```

## 8. Creating Test Cases in Bulk

Zephyr Scale allows multiple test cases to be created at the same time.

This is useful when creating a large number of test cases during test planning.

Shared attributes can be applied to the test cases, such as:

* Status
* Priority
* Component
* Owner
* Labels

Detailed steps and parameters can be added afterward.

## 9. Editing Test Cases in Bulk

Multiple existing test cases can also be modified simultaneously.

Examples include:

* Changing priority.
* Updating status.
* Changing components.
* Updating owners.
* Applying labels.

Bulk editing should be performed carefully because selecting a field and leaving it empty may clear the existing value for all selected test cases.



```
```
