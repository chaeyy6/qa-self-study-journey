# Statement Coverage

## Objective

Understand what Statement Coverage is, how it is calculated, and how it is used to determine whether executable statements in the code have been tested.

## 1. Statement Coverage

Statement Coverage is a white-box test design technique that measures the percentage of executable statements that are executed by the test cases.

Its purpose is to identify statements in the code that have not been executed during testing.

### Formula

**Statement Coverage = (Number of Executed Statements / Total Number of Executable Statements) × 100**

## 2. Statement Coverage Example

Consider the following code:

    if (age >= 18)
        print("Adult")
    else
        print("Minor")

There are two executable statements:

1. `print("Adult")`
2. `print("Minor")`

### Test Case 1

**Input:**

`age = 20`

The condition `age >= 18` is True, so:

`print("Adult")`

is executed.

Only 1 of the 2 executable statements has been executed.

**Statement Coverage = 1 / 2 × 100 = 50%**

### Test Case 2

**Input:**

`age = 15`

The condition `age >= 18` is False, so:

`print("Minor")`

is executed.

Both executable statements have now been executed across the test cases.

**Statement Coverage = 2 / 2 × 100 = 100%**

## 3. What 100% Statement Coverage Means

100% Statement Coverage means:

> Every executable statement in the code has been executed at least once by the test cases.

It indicates that no executable statement has been left untested based on execution.

However, achieving 100% Statement Coverage does not mean that the software is completely tested or defect-free.

## 4. Identifying Executable Statements

When calculating Statement Coverage, focus on statements that can actually be executed by the program.

For example:

    if (age >= 18)
        print("Adult")
    else
        print("Minor")

The condition itself is not counted as an executable statement for this calculation.

The executable statements are:

- `print("Adult")`
- `print("Minor")`

The tester counts how many of these statements are executed by the test cases.

## 5. Purpose of Statement Coverage

Statement Coverage can be used to:

- Identify untested executable code.
- Measure how much of the code has been exercised.
- Identify areas where additional test cases may be required.
- Support test completeness analysis.
- Help identify code that has not been executed during testing.

## 6. Limitations of Statement Coverage

Statement Coverage only measures whether executable statements have been executed.

It does not guarantee that:

- Every possible input has been tested.
- Every possible outcome has been tested.
- Every possible execution path has been tested.
- The code is free from defects.

Therefore, 100% Statement Coverage should not be interpreted as 100% test effectiveness.

## Key Takeaways

- Statement Coverage is a white-box testing technique.
- It measures the percentage of executable statements executed by test cases.
- The formula is `(Executed Statements / Total Executable Statements) × 100`.
- 100% Statement Coverage means every executable statement has been executed at least once.
- Statement Coverage helps identify code that has not been exercised.
- 100% Statement Coverage does not guarantee that the software is defect-free.

## Interview Questions

- What is Statement Coverage?
- How do you calculate Statement Coverage?
- What does 100% Statement Coverage mean?
- What is an executable statement?
- Why is Statement Coverage useful?
- What are the limitations of Statement Coverage?
