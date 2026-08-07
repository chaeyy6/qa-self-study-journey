# Executing Test Scenarios

## Overview

Test Execution is the process of performing prepared test scenarios against an application to verify that it behaves according to the documented requirements.

During execution, testers validate application behavior, record observations, identify defects, and track testing progress. Executing structured scenarios ensures complete coverage and reduces the risk of missing important functionality.

---

## Test Data

Test Data refers to the input values or datasets required to execute test scenarios.

Common sources of test data include:

- Manually created test accounts
- Developer-provided seeded data
- Mock or dummy data
- Existing records within the testing environment

When dependent features are unavailable, teams often use mock data to continue testing without blocking progress.

---

## Best Practices During Execution

- Execute one test variable at a time to isolate failures.
- Keep all unrelated fields valid when validating a specific input.
- Follow documented test scenarios to ensure consistent coverage.
- Mark scenarios as executed regardless of whether they pass or fail.
- Record observations throughout the testing session.

---

## Managing Defects

Rather than creating a complete defect report immediately, testers often record short notes while executing tests.

Example:

- Login page
- Show Password button not responding
- Forgot Password link redirects incorrectly

After the execution session, these notes are expanded into complete defect reports with reproduction steps, expected results, actual results, environment details, and supporting evidence.

This approach maintains testing momentum while ensuring defects are documented accurately.

---

## Handling Blockers

Certain scenarios may temporarily block additional testing.

Examples include:

- Account lockouts after multiple failed login attempts
- API rate limiting
- Waiting for scheduled jobs to complete

Instead of waiting, testers continue executing other independent scenarios and return to blocked scenarios later.

---

## Tracking Progress

Execution progress is commonly monitored by calculating the percentage of completed scenarios.

**Execution Rate**

```
(Number of Executed Scenarios / Total Number of Scenarios) × 100
```

Tracking execution progress helps teams estimate testing completion and communicate overall project status.

---

## Key Takeaways

- Test execution verifies application behavior against expected requirements.
- Appropriate test data is essential for reliable testing.
- Execute one validation at a time to isolate failures.
- Executed scenarios are not necessarily passed scenarios.
- Record quick defect notes during execution and prepare detailed reports afterward.
- Continue with other scenarios when blocked to maximize testing efficiency.
- Monitor execution progress throughout the testing cycle.
