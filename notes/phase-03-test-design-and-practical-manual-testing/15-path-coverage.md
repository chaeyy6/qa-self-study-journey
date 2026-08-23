# Path Coverage

## Objective

Understand how Path Coverage is used in white-box testing to verify whether the possible execution paths through the code have been executed by the test cases.

## 1. Path Coverage

Path Coverage is a white-box testing technique that measures whether the possible execution paths through the code have been executed by the test cases.

A **path** is a sequence of statements and decisions that the program follows from the beginning to the end of execution.

### Key Idea

> **Path Coverage = Test the different routes the program can take from start to finish.**

## 2. Path Coverage Example

Consider the following code:

    if (A)
        X
    else
        Y

    if (B)
        P
    else
        Q

There are two decisions:

- Decision A → TRUE or FALSE
- Decision B → TRUE or FALSE

The possible execution paths are:

| Path | A | B | Execution Path |
|---|---|---|---|
| 1 | TRUE | TRUE | X → P |
| 2 | TRUE | FALSE | X → Q |
| 3 | FALSE | TRUE | Y → P |
| 4 | FALSE | FALSE | Y → Q |

Therefore, there are **4 possible paths**.

To achieve **100% Path Coverage**, all four paths must be executed.

## 3. Designing Test Cases

Test cases can be designed to execute each possible path.

| Test Case | A | B | Path |
|---|---|---|---|
| TC1 | TRUE | TRUE | X → P |
| TC2 | TRUE | FALSE | X → Q |
| TC3 | FALSE | TRUE | Y → P |
| TC4 | FALSE | FALSE | Y → Q |

After executing all four test cases:

**Path Coverage = 4 / 4 × 100 = 100%**

## 4. Understanding Paths

A path is determined by the sequence of decisions made during execution.

For example:

    A = TRUE
    B = FALSE

produces the path:

    A → X → B → Q

This is one unique execution path.

Changing the outcome of either decision can result in a different path.

## 5. Number of Possible Paths

For simple code containing independent binary decisions, the number of possible combinations can increase quickly.

For example:

- 1 binary decision → 2 possible paths
- 2 binary decisions → 4 possible paths
- 3 binary decisions → 8 possible paths
- 4 binary decisions → 16 possible paths

A simple way to represent this is:

**Possible Paths = 2ⁿ**

where **n** is the number of independent binary decisions.

However, real programs can contain loops and more complex control flow, making exhaustive path testing difficult or impractical.

## 6. Limitations of Path Coverage

Path Coverage can become difficult when a program contains:

- Many decisions.
- Nested conditions.
- Multiple branches.
- Loops.
- Complex control flow.

The number of possible paths can grow rapidly, making 100% Path Coverage impractical for larger systems.

Therefore, testers may focus on the most important or risk-critical paths rather than attempting to test every possible path.

## Key Takeaways

- Path Coverage is a white-box testing technique.
- A path represents a specific route through the code from start to finish.
- Path Coverage requires testing the different possible execution paths.
- Multiple decisions create multiple possible paths.
- The number of possible paths can increase rapidly as the number of decisions increases.
- 100% Path Coverage means all identified paths have been executed.
- Path Coverage can become impractical when programs contain many decisions, loops, or complex control flow.

## Interview Questions

- What is Path Coverage?
- What is an execution path?
- What does 100% Path Coverage mean?
- How do decisions affect the number of possible paths?
- How many paths are possible with two independent binary decisions?
- What is the `2ⁿ` rule for calculating possible paths?
- Why can achieving 100% Path Coverage become impractical?
