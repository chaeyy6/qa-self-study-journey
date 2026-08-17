# 06 — Zephyr Scale — Test Data & Data-Driven Testing

## Objective

Understand Data-Driven Testing (DDT), how it separates test logic from test data, and how Zephyr Scale Parameters and Data Sets can be used to create reusable and maintainable test cases.

## 1. Data-Driven Testing (DDT)

**Data-Driven Testing** separates test steps from test data.

Instead of creating separate test cases for every variation of input, a single test case can be executed multiple times using different rows of test data.

### Benefits of DDT

- **Reduces duplication:** Avoids creating repetitive test cases for different inputs.
- **Improves coverage:** Allows one test case to cover multiple data variations.
- **Simplifies maintenance:** Test steps only need to be updated in one place.
- **Supports automation:** The approach can also be applied to automated testing frameworks.

## 2. Parameters vs. Test Data

Zephyr Scale provides both **Parameters** and **Test Data**, but they serve different purposes.

### Parameters

**Parameters** are variables used within a test case to represent values that may need to be reused or changed.

Example:

`Enter {valid_otp}`

The parameter can have a default value, such as:

`valid_otp = 1234`

Parameters are particularly useful when the same value needs to be referenced in multiple parts of a test case or when a value may need to be overridden for a specific test execution.

### Test Data

**Test Data** is used when the same test case needs to be executed against multiple sets of input values.

Example:

| Username | Password |
| --- | --- |
| user1@example.com | Password123 |
| user2@example.com | Password456 |
| user3@example.com | Password789 |

The test steps remain the same while the data changes for each execution iteration.

### Key Difference

**Parameters → Represent reusable variables within a test case.**

**Test Data → Provides multiple sets of input values for repeated test execution.**

### Simple Example

For a login test:

**Parameter:**

`{username}`

**Test Data:**

- `user1@example.com`
- `user2@example.com`
- `user3@example.com`

The parameter defines **what value the test step expects**, while the test data provides **the different values used during execution**.

## 3. Inline Test Data vs. Shared Data Sets

### Inline Test Data

Test data is defined directly within an individual test case.

Best suited for:

- One-time data variations.
- Test-specific values.
- Data that does not need to be reused.

### Shared Data Sets

Test data is configured centrally and can be reused across multiple test cases.

Best suited for:

- Common project-wide test data.
- User roles.
- Subscription plans.
- Test credit card information.
- Other frequently reused values.

### Key Difference

**Inline Test Data:** Specific to one test case.

**Shared Data Set:** Reusable across multiple test cases.

## 4. Creating Inline Test Data

Inline test data can be created directly within a test case.

### Basic Workflow

1. Open the test case.
2. Navigate to the **Test Script** section.
3. Switch from **Parameters** to **Test Data**.
4. Add columns for the required test data.
5. Enter the required data rows.
6. Reference the data in test steps using variables.

Example:

**Test Data:**

- Valid Phone Number
- Valid OTP

A test step can reference the corresponding variable:

`Enter {Valid Phone Number}`

## 5. Creating Shared Data Sets

Shared Data Sets can be configured centrally in Zephyr Scale.

### Basic Workflow

1. Navigate to **Configuration**.
2. Open **Data Sets**.
3. Create a new Data Set.
4. Add the required columns and values.
5. Open the test case where the Data Set will be used.
6. Open **Test Data**.
7. Import the shared Data Set.
8. Map the data to the appropriate test rows.

Examples of reusable data include:

- Guest
- Regular User
- Blocked User
- Different credit card types
- Different subscription plans

## 6. Data-Driven Test Execution

When a DDT test case is added to a **Test Cycle**, Zephyr Scale creates execution iterations based on the rows in the test data table.

Each data row can have its own execution result.

Example:

**Test Case:** Login with Different User Types

- Guest → Pass
- Regular User → Pass
- Blocked User → Fail

This allows each data variation to be evaluated independently while maintaining a single test case.

## 7. Updating DDT Test Cases

If a test case is modified after it has already been added to a Test Cycle, Zephyr Scale can mark the execution as **Outdated**.

The **Update Test Script** option can then be used to apply the latest test case changes.

> Updating the test script may remove attachments associated with deleted steps.

## Key Takeaways

- **Data-Driven Testing** separates test logic from test data and allows one test case to be executed against multiple data sets.
- **Parameters** represent reusable variables within a test case.
- **Test Data** provides different input values for repeated test execution.
- **Inline Test Data** is specific to an individual test case.
- **Shared Data Sets** can be reused across multiple test cases.
- DDT reduces test case duplication and improves maintainability.
- Each data row can have an independent execution result.
- Parameters and Test Data can work together to create flexible and reusable test cases.
