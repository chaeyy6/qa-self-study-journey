# Decision Coverage & Condition Coverage

## Objective

Understand how Decision Coverage and Condition Coverage are used in white-box testing to verify decision outcomes and individual conditions within the code.

## 1. Decision Coverage

Decision Coverage is a white-box testing technique that measures whether each possible outcome of a decision has been executed.

For a basic decision, the possible outcomes are:

- **TRUE**
- **FALSE**

### Formula

**Decision Coverage = (Number of Decision Outcomes Executed / Total Number of Decision Outcomes) × 100**

## 2. Decision Coverage Example

Consider the following code:

    if (age >= 18)
        print("Adult")
    else
        print("Minor")

The decision is:

`age >= 18`

It has two possible outcomes:

- TRUE → Adult
- FALSE → Minor

### Test Cases

| Test | Age | Decision |
|---|---:|---|
| TC1 | 20 | TRUE |
| TC2 | 15 | FALSE |

Both decision outcomes have been executed.

**Decision Coverage = 2 / 2 × 100 = 100%**

### Key Point

> Decision Coverage checks whether every possible outcome of a decision has been executed.

For a simple decision:

> **TRUE + FALSE**

## 3. Condition Coverage

Condition Coverage is a white-box testing technique that measures whether each individual condition within a decision has been evaluated to both TRUE and FALSE.

## 4. Condition Coverage Example

Consider the following code:

    if (age >= 18 AND hasID == true)
        print("Allow")
    else
        print("Deny")

There are two individual conditions:

- **Condition A:** `age >= 18`
- **Condition B:** `hasID == true`

For 100% Condition Coverage, each individual condition must be evaluated as both TRUE and FALSE.

### Test Cases

| Test | Age ≥ 18 | Has ID |
|---|---|---|
| TC1 | TRUE | TRUE |
| TC2 | FALSE | TRUE |
| TC3 | TRUE | FALSE |

Now:

- Condition A → TRUE and FALSE
- Condition B → TRUE and FALSE

Therefore:

**Condition Coverage = 100%**

### Key Point

> Condition Coverage checks whether every individual condition has been evaluated as both TRUE and FALSE.

## 5. Decision Coverage vs Condition Coverage

The key difference is what is being measured.

### Decision Coverage

Looks at the **overall decision**.

    (A AND B)

The question is:

> Did the overall decision become TRUE and FALSE?

### Condition Coverage

Looks at the **individual conditions**.

    A AND B

The questions are:

> Did A become TRUE and FALSE?

> Did B become TRUE and FALSE?

### Simple Way to Remember

- **Decision Coverage:** Overall decision → TRUE / FALSE
- **Condition Coverage:** Individual conditions → TRUE / FALSE

## 6. When to Use Decision Coverage

Decision Coverage is useful when:

- Testing conditional logic.
- Verifying both outcomes of decisions.
- Identifying decision outcomes that have not been executed.
- Measuring structural test coverage.

## 7. When to Use Condition Coverage

Condition Coverage is useful when:

- A decision contains multiple conditions.
- Individual conditions need to be evaluated separately.
- Testing complex logical expressions.
- Identifying conditions that have not been evaluated to both TRUE and FALSE.

## Key Takeaways

- Decision Coverage checks whether every possible outcome of each decision has been executed.
- For a basic decision, this means testing both TRUE and FALSE outcomes.
- Condition Coverage checks whether each individual condition within a decision evaluates to TRUE and FALSE.
- Decision Coverage focuses on the overall decision.
- Condition Coverage focuses on individual conditions.
- Multiple conditions within one decision require each condition to be considered separately.

## Interview Questions

- What is Decision Coverage?
- What is Condition Coverage?
- What is the difference between Decision Coverage and Condition Coverage?
- How do you calculate Decision Coverage?
- What is an individual condition?
- How do you achieve 100% Condition Coverage?
- What does TRUE and FALSE represent in Decision Coverage?
