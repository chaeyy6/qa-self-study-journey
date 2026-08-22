# State-Transition & Pairwise Testing

## Objective

Understand how State-Transition Testing is used to verify system behavior as it moves between different states, and how Pairwise Testing reduces the number of test cases required when testing combinations of multiple input parameters.

## 1. State-Transition Testing

State-Transition Testing is a black-box test design technique used to verify how a system behaves when it moves from one state to another based on specific inputs, events, or user actions.

### Key Terms

- **State:** A condition or mode in which the system currently exists.
- **Transition:** A change from one state to another caused by an input or event.
- **Start State:** The initial state where the system begins.
- **End / Dead State:** A terminal state where execution ends and no further transitions are available.

## 2. ATM PIN Validation Example

An ATM can be modeled using several states:

1. Enter PIN — Start State
2. Enter PIN — 2nd Attempt
3. Enter PIN — 3rd Attempt
4. Eat Card — Dead State
5. Profile Page — Dead State

Possible transitions include:

- **A:** Enter PIN → 2nd Attempt after an incorrect PIN.
- **B:** 2nd Attempt → 3rd Attempt after an incorrect PIN.
- **C:** 3rd Attempt → Eat Card after an incorrect PIN.
- **D:** Enter PIN → Profile Page after a correct PIN.
- **E:** 2nd Attempt → Profile Page after a correct PIN.
- **F:** 3rd Attempt → Profile Page after a correct PIN.

This allows the tester to verify both normal and exceptional user flows.

## 3. State-Transition Coverage

### All-States Coverage

The objective is to visit every state at least once.

For the ATM example, two test cases can achieve full state coverage:

- **TC1:** Correct PIN on the first attempt → visits Enter PIN and Profile Page.
- **TC2:** Wrong PIN three times → visits Enter PIN, 2nd Attempt, 3rd Attempt, and Eat Card.

Together, these test cases visit all five states.

### All-Transitions Coverage

The objective is to execute every transition at least once.

For the ATM example, four test cases are required:

- **TC1:** Correct PIN → covers transition D.
- **TC2:** Wrong PIN → Wrong PIN → Wrong PIN → covers A, B, and C.
- **TC3:** Wrong PIN → Correct PIN → covers A and E.
- **TC4:** Wrong PIN → Wrong PIN → Correct PIN → covers A, B, and F.

All six transitions are therefore covered.

### Important Relationship

**All-Transitions Coverage guarantees All-States Coverage, but All-States Coverage does not necessarily guarantee All-Transitions Coverage.**

A test can visit every state without executing every possible transition between those states.

## 4. When to Use State-Transition Testing

State-Transition Testing is useful when system behavior depends on the current state of the application.

Examples include:

- ATM PIN attempts
- User account lockout
- Login sessions
- Shopping cart states
- Order processing
- Payment processing
- Password reset workflows
- Ticket or support-request status changes
- Device operating modes

The technique is particularly useful when the same input can produce different results depending on the system's current state.

## 5. Pairwise Testing

Pairwise Testing is a black-box combinatorial test technique used when a system contains multiple input parameters, each with several possible values.

Instead of testing every possible combination, Pairwise Testing ensures that every possible pair of parameter values occurs together in at least one test case.

This significantly reduces the number of required test cases while maintaining useful interaction coverage.

## 6. Why Pairwise Testing Is Useful

Pairwise Testing helps:

- Reduce the number of test cases.
- Reduce execution time.
- Reduce maintenance effort.
- Maintain coverage of interactions between parameter values.
- Identify defects caused by combinations of two parameters.

It is especially useful when testing filters, configurations, settings, and combinations of user-selected options.

## 7. Udemy Search Filter Example

Consider a course search feature with three parameters:

### Ratings

- 4.5+
- 4.0+
- 3.5+
- 3.0+

**4 values**

### Video Duration

- 0–1 hours
- 1–3 hours
- 3–6 hours
- 6–17 hours
- 17+ hours

**5 values**

### Course Level

- All Levels
- Beginner
- Intermediate
- Expert

**4 values**

### Exhaustive Testing

Testing every possible combination would require:

**4 × 5 × 4 = 80 test cases**

Adding more parameters would cause the number of combinations to grow rapidly.

### Pairwise Testing

Instead of executing all 80 combinations, a Pairwise test set can reduce the required tests substantially while ensuring that every pair of parameter values is covered.

In the instructor's example, the combination set was reduced to **22 test cases**.

The exact number of generated tests can vary depending on the parameters, values, and constraints being used.

## 8. Business Rules and Constraints

Real applications often contain combinations that are not valid.

For example:

- A 0–1 hour course may not be available at Expert level.
- 17+ hour content may only be available for Expert-level courses.

These rules can be provided as constraints when generating the Pairwise test set.

The generator can then remove combinations that are impossible or invalid.

This prevents testers from wasting time executing test cases for combinations that should never exist.

## 9. Pairwise Testing Tools

Creating Pairwise combinations manually becomes difficult as the number of parameters increases.

Dedicated Pairwise test-generation tools can automatically create optimized combinations.

The tester provides:

- Parameters
- Possible values
- Business constraints

The tool then generates a reduced set of test cases designed to achieve Pairwise coverage.

## 10. When to Use Pairwise Testing

Pairwise Testing is particularly useful for:

- E-commerce filters
- Search filters
- Software configuration screens
- Device configurations
- Browser and operating-system combinations
- Hardware settings
- Product options
- Data-driven testing
- Application settings

It is most useful when testing every possible combination would require an excessive number of test cases.

## 11. Comparing Black-Box Test Design Techniques

| Technique | Main Purpose |
|---|---|
| **Equivalence Partitioning (EP)** | Divide inputs into groups with similar expected behavior. |
| **Boundary Value Analysis (BVA)** | Test values at the edges of partitions. |
| **Decision Table Testing** | Test combinations of conditions and business rules. |
| **State-Transition Testing** | Test how the system moves between states. |
| **Pairwise Testing** | Reduce the number of tests required for multiple parameter combinations. |

### Simple Way to Remember Them

- **EP:** Which groups of inputs should I test?
- **BVA:** Which values at the edges should I test?
- **Decision Table:** Which combinations of conditions should I test?
- **State Transition:** How does the system behave as it moves between states?
- **Pairwise:** How can I efficiently test combinations of multiple parameters?

## Key Takeaways

- State-Transition Testing verifies how a system behaves as it moves between different states.
- States represent system conditions, while transitions represent changes between those conditions.
- All-States Coverage ensures every state is visited.
- All-Transitions Coverage ensures every transition is executed.
- All-Transitions Coverage provides stronger coverage than All-States Coverage.
- Pairwise Testing reduces the number of test cases needed when multiple parameters have many possible combinations.
- Pairwise Testing focuses on covering every pair of parameter values at least once.
- Business constraints can be used to exclude invalid combinations.
- Different black-box techniques should be selected according to the type of requirement being tested.
- No single test design technique is appropriate for every testing problem.

## Interview Questions

- What is State-Transition Testing?
- What is the difference between a state and a transition?
- What is All-States Coverage?
- What is All-Transitions Coverage?
- Which provides stronger coverage: All-States or All-Transitions?
- What is Pairwise Testing?
- Why is Pairwise Testing useful?
- When would you use Pairwise Testing?
- What is the difference between Decision Table Testing and Pairwise Testing?
