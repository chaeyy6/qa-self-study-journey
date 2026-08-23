# MC/DC & Loop Coverage

## Objective

Understand Modified Condition/Decision Coverage (MC/DC) and Loop Coverage as white-box testing techniques, including how MC/DC verifies the independent effect of individual conditions and how Loop Coverage verifies loop behavior across different iteration counts.

## 1. Modified Condition/Decision Coverage (MC/DC)

Modified Condition/Decision Coverage (MC/DC) is a white-box testing technique that verifies that:

1. The overall decision has been evaluated to both TRUE and FALSE.
2. Each individual condition has been evaluated to both TRUE and FALSE.
3. Each individual condition independently affects the overall decision.

### Key Idea

> **MC/DC = Prove that changing each individual condition can independently change the final decision.**

## 2. MC/DC Example

Consider the following code:

    if (A AND B)
        Allow
    else
        Deny

There are two conditions:

- **A:** Has ID
- **B:** Has Valid Ticket

### Test Cases

| Test | A | B | Decision |
|---|---|---|---|
| TC1 | TRUE | TRUE | TRUE |
| TC2 | FALSE | TRUE | FALSE |
| TC3 | TRUE | FALSE | FALSE |

### A Independently Affects the Decision

Compare TC1 and TC2:

- TC1 → A = TRUE, B = TRUE → Decision = TRUE
- TC2 → A = FALSE, B = TRUE → Decision = FALSE

Only **A** changed, and the overall decision changed.

Therefore, A independently affects the decision.

### B Independently Affects the Decision

Compare TC1 and TC3:

- TC1 → A = TRUE, B = TRUE → Decision = TRUE
- TC3 → A = TRUE, B = FALSE → Decision = FALSE

Only **B** changed, and the overall decision changed.

Therefore, B independently affects the decision.

This achieves **MC/DC coverage**.

## 3. MC/DC Key Point

MC/DC is more rigorous than simply checking whether conditions have been evaluated as TRUE and FALSE.

The tester must demonstrate that each condition can independently influence the overall decision.

### Simple Way to Remember

- **Condition Coverage:** Did each condition become TRUE and FALSE?
- **MC/DC:** Can each condition independently change the overall decision?

## 4. Loop Coverage

Loop Coverage is a white-box testing technique that focuses on testing the behavior of loops for different numbers of iterations.

Loops can introduce defects involving:

- Incorrect starting conditions.
- Incorrect termination conditions.
- Incorrect iteration counts.
- Infinite loops.
- Boundary errors.

## 5. Simple Loop Example

Consider the following code:

    FOR i = 1 TO 3
        print(i)

The loop is expected to execute three times.

Important test situations include:

| Test | Iterations | Purpose |
|---|---:|---|
| TC1 | 0 | Verify the loop does not execute when appropriate |
| TC2 | 1 | Verify a single iteration |
| TC3 | 2 | Verify multiple iterations |
| TC4 | 3 | Verify the expected maximum |
| TC5 | 4 | Test behavior beyond the expected limit |

The exact test cases depend on the loop's requirements and constraints.

## 6. Loop Boundaries

Loop testing pays particular attention to values around the loop boundaries.

Common cases include:

- **0 iterations**
- **1 iteration**
- **2 iterations**
- **Typical number of iterations**
- **Maximum number of iterations**
- **Maximum + 1**

For example, if a loop is expected to execute between 1 and 10 times, important values to consider include:

**0, 1, 2, 10, and 11**

These values help identify errors in loop initialization, termination, and boundary conditions.

## 7. Purpose of Loop Coverage

Loop Coverage can be used to:

- Verify that loops execute correctly.
- Test whether loops execute when expected.
- Test loop termination.
- Identify infinite-loop problems.
- Detect off-by-one errors.
- Test loop boundary conditions.

## 8. MC/DC and Loop Coverage

MC/DC and Loop Coverage focus on different aspects of the code.

| Technique | Main Focus |
|---|---|
| **MC/DC** | Whether individual conditions independently affect a decision. |
| **Loop Coverage** | Whether loops behave correctly across different iteration counts. |

Both are white-box testing techniques but address different types of code behavior.

## Key Takeaways

- MC/DC stands for Modified Condition/Decision Coverage.
- MC/DC verifies that each individual condition can independently affect the overall decision.
- MC/DC requires comparing test cases where one condition changes while the other conditions remain unchanged.
- Loop Coverage focuses on testing loops across different iteration counts.
- Loop testing pays particular attention to boundary values.
- Common loop cases include 0, 1, normal, maximum, and beyond-maximum iterations.

## Interview Questions

- What is MC/DC?
- What does MC/DC stand for?
- What is the purpose of MC/DC?
- How do you prove that a condition independently affects a decision?
- What is the difference between Condition Coverage and MC/DC?
- What is Loop Coverage?
- Why are loop boundaries important?
- What iteration counts are commonly considered during loop testing?
- What types of defects can Loop Coverage help identify?
