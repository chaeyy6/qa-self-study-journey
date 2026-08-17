# 07 — Zephyr Scale — Test Cycles & Test Plans

## Objective

Understand how Test Cycles are used to execute and track testing progress in Zephyr Scale, how Test Cycles can be managed across different testing runs, and how Test Plans organize multiple Test Cycles at a higher level.

## 1. Test Cycles & Progress Tracking

A **Test Cycle** represents a specific testing run where test cases are executed and their results are tracked.

### Progress Tracking

Zephyr Scale provides high-level execution progress through statuses such as:

- Passed
- Failed
- Blocked
- In Progress
- Not Executed

This allows testers and stakeholders to quickly understand the current state of a testing cycle.

### Regression Testing

An executed Test Cycle can be cloned for a new regression run.

Cloning a Test Cycle:

- Preserves the test case mappings.
- Resets execution results.
- Resets actual execution time.

This allows the same group of test cases to be reused for a new testing iteration without manually rebuilding the cycle.

## 2. Test Cycle Time Estimation

Test cases can have an **Estimated Time** that represents the expected effort required for execution.

Estimations can be:

- Added individually.
- Updated in bulk across multiple test cases.

### Important Rule

Test case estimations should be configured **before the test cases are added to a Test Cycle**.

If the estimation is changed after a test case has already been added to an existing cycle, the cycle retains the original estimation.

A new Test Cycle must be created for the updated estimation to be reflected.

## 3. Actual Execution Time

Zephyr Scale automatically tracks **Actual Time** during test execution through the Test Player.

The timer:

- Starts during execution.
- Tracks the actual execution duration.
- Cannot be manually edited.

This provides more reliable execution metrics.

### Estimated vs. Actual Time

Comparing estimated and actual execution time can help teams understand testing effort and improve future planning.

## 4. Editing Test Cycles

Existing Test Cycles can be modified to maintain accurate project information.

Editable information includes:

- Cycle name
- Folder
- Status
- Release version
- Owner
- Planned start date
- Planned end date

Test Cycles can also contain:

- Jira issue links
- Comments
- Attachments
- Execution history

### Impact of Test Case Changes

Adding or removing test cases can change the overall estimated time of the Test Cycle.

However, changing the estimated time of an individual test case after it has already been added does not automatically update the cycle's existing estimation.

## 5. Cloning & Deleting Test Cycles

### Cloning

Cloning a Test Cycle is useful when the same test cases need to be executed again, particularly for regression testing.

The test case structure is preserved while execution results are reset for the new cycle.

### Deleting

Test Cycles can be permanently deleted.

However, deletion may be prevented when another item has a direct dependency on the cycle.

A Jira issue linked to a Test Cycle provides **traceability**, but does not necessarily prevent the Test Cycle from being deleted.

## 6. Organizing & Finding Test Cycles

Test Cycles can be organized and grouped using different criteria, such as:

- Version
- Test Plan
- Month / Date

Filters can also be used to locate relevant cycles based on:

- Assigned tester
- Iteration
- Folder

Test Cycles can also be accessed through the Jira backlog to continue or launch testing activities.

## 7. Test Plans

A **Test Plan** provides a higher-level way to organize multiple Test Cycles.

In general software testing, a Test Plan can refer to a comprehensive document describing the testing strategy, scope, schedule, resources, tools, and management approach.

In **Zephyr Scale**, however, a Test Plan primarily acts as a container for multiple Test Cycles.

### Zephyr Scale Hierarchy

Test Plan
    ↓
Test Cycle(s)
    ↓
Test Case(s)

## 8. Test Plan Features

A Test Plan can contain information such as:

Name
Objective
Status
Owner
Folder
Labels

Test Plans can also contain:

Jira issue links
Web links
Attachments
Comments
Execution history
Progress Aggregation

The overall progress of a Test Plan reflects the combined progress of the Test Cycles assigned to it.

This provides a higher-level view of testing progress across multiple execution runs.
