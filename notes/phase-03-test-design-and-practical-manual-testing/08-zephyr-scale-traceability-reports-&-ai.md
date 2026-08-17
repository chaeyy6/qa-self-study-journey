# 08 — Zephyr Scale — Traceability, Reports & AI

## Objective

Understand how Zephyr Scale supports traceability, reporting, and AI-assisted test creation and execution, including how sensitive data, manual interventions, and parallel execution are handled in AI-powered testing workflows.

## 1. Bidirectional Traceability

**Bidirectional Traceability** allows relationships between requirements, test cases, test executions, and defects to be tracked in both directions.

This helps teams understand:

- Which requirements are covered by test cases.
- Which test cases validate a specific requirement.
- Which tests have been executed.
- Which defects are associated with testing activities.

Traceability helps maintain visibility between requirements and testing throughout the QA lifecycle.

## 2. Reports in Zephyr Scale

Reports provide a higher-level view of testing activity and results.

They can help teams monitor information such as:

- Test execution progress.
- Passed and failed tests.
- Testing coverage.
- Defect-related information.
- Overall testing status.

Reports can be useful for communicating testing progress to developers, QA teams, and stakeholders.

## 3. AI-Assisted Test Creation & Execution

Zephyr Scale's AI-powered testing capabilities can assist with creating and executing test cases.

Instead of relying entirely on traditional automation code and predefined selectors, the AI-based approach can interpret natural-language descriptions and locate UI elements.

### No-Code Generative AI vs. Traditional Automation

Traditional frameworks such as:

- Selenium
- Playwright
- Cypress

typically rely on automation code and selectors such as XPath or CSS selectors.

A Generative AI-based approach can instead use natural-language instructions to identify and interact with UI elements.

This can reduce the amount of traditional automation code required for certain testing workflows.

## 4. Manual Intervention During AI Recording

Some browser actions require access to the local system and cannot initially be performed autonomously by cloud-based runners.

Examples include:

- Uploading files.
- Downloading files.
- Recording audio.

### Hybrid Recording Workflow

When an unsupported action is encountered:

1. The AI-assisted test creation process pauses.
2. The tester manually performs the required local action.
3. The action is recorded.
4. Future automated executions can repeat the recorded action.

This creates a **hybrid workflow** combining manual intervention with automated execution.

## 5. Managing Sensitive Data with Secrets

Sensitive information should not be hardcoded directly into test cases.

Examples include:

- Passwords.
- Authentication tokens.
- Credit card information.
- Other confidential credentials.

Hardcoding sensitive information can expose it to users with access to the project.

### Secrets in Reflect

Sensitive values can be stored as **Secrets** in Reflect.

Basic workflow:

1. Open **Reflect**.
2. Navigate to **Globals**.
3. Open **Secrets**.
4. Select **Add Secret**.
5. Define the secret key and value.

Example:

Key: password
Value: SuperSecretPassword

Using Secrets in Zephyr Scale

Instead of entering the sensitive value directly, the test can reference the secret using:

${password}

The parameter name is case-sensitive and must match the corresponding key in Reflect.

The actual secret remains hidden from team members while being securely injected during cloud execution.

## 6. Parallel Test Execution

Automated test cases within a Test Cycle can be executed in parallel using cloud infrastructure.

Instead of running tests sequentially:

Test 1 → Test 2 → Test 3 → Test 4

independent tests can run concurrently:

Test 1 ─┐
Test 2 ─┤
Test 3 ─┼→ Run simultaneously
Test 4 ─┘
Benefit

Parallel execution can significantly reduce overall execution time when tests are independent.

For example, twelve independent five-minute tests could potentially complete in approximately five minutes when executed simultaneously rather than requiring approximately sixty minutes sequentially.

Key Takeaways
- Bidirectional Traceability connects requirements and testing in both directions.
- Reports provide visibility into testing progress, results, and coverage.
- AI-assisted testing can generate and execute tests using natural-language instructions.
- Traditional frameworks such as Selenium, Playwright, and Cypress commonly rely on code and selectors.
- Some local browser actions may require manual intervention during initial AI recording.
- Sensitive information should be stored as Secrets rather than hardcoded into test cases.
- Secret references are case-sensitive.
-Parallel execution allows independent automated tests to run simultaneously and reduce overall execution time.
