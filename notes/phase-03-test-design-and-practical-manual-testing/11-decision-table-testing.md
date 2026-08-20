# Decision Table Testing

## Learning Objective

Understand how Decision Table Testing is used to analyze and test complex business logic involving multiple conditions and their corresponding outcomes, and learn how to identify combinations of conditions and ensure adequate rule coverage.

---

## Key Concepts

- Decision Table Testing
- Conditions
- Actions
- Rules
- Rule Combinations
- Combinatorial Explosion
- Rule Coverage
- Test Optimization

---

## My Understanding

Decision Table Testing is a systematic black-box test design technique used to test complex business logic involving multiple conditions that can produce different actions or outcomes.

A decision table organizes the logic into conditions, actions, and rules.

- **Conditions** represent the inputs or prerequisites that influence system behavior.
- **Actions** represent the expected outcomes based on those conditions.
- **Rules** represent unique combinations of condition values and their corresponding actions.

Each column in a decision table represents one possible rule or combination of conditions.

For binary conditions, where each condition has two possible values such as Yes/No or True/False, the number of possible rules can be calculated using:

**Number of Rules = 2ⁿ**

where **n** is the number of conditions.

For example, two binary conditions produce:

**2² = 4 rules**

---

## QA Perspective

Decision Table Testing helps QA Engineers systematically test business logic where multiple conditions can influence the final outcome.

Instead of creating test cases randomly, testers can identify every possible combination of conditions and determine the expected action for each combination.

Decision tables can also be used to evaluate existing test cases. By mapping existing tests against the rules, testers can identify:

- Missing coverage.
- Duplicate test cases.
- Redundant combinations.
- Unclear business logic.

However, the number of combinations can grow rapidly as more conditions are introduced. This is known as **combinatorial explosion**.

For example:

- 10 binary conditions → 2¹⁰ = 1,024 possible rules.
- 40 conditions with 4 possible values each → 4⁴⁰ possible combinations.

When complete combination testing becomes impractical, testers may need to optimize the decision table or select another test design technique based on risk, time, and requirements.

---

## Real-World Examples

### E-Commerce Discount Logic

An e-commerce application may apply a discount based on two conditions:

- Order total is greater than $100.
- User has a Gold subscription.

The four possible combinations are:

| Condition / Action | Rule 1 | Rule 2 | Rule 3 | Rule 4 |
|---|---|---|---|---|
| Order Total > $100 | True | True | False | False |
| Gold Subscription | True | False | True | False |
| Apply Discount | Yes | No | No | No |

Testing these four rules ensures that each possible combination of the two conditions is considered.

### Speeding Fine System

A speeding system may use:

- Speed greater than 50.
- Vehicle is in a school zone.

The four possible rules are:

- **R1:** Speed > 50 + School Zone → Go to Jail.
- **R2:** Speed ≤ 50 + School Zone → No Action.
- **R3:** Speed > 50 + Not School Zone → Pay Fine.
- **R4:** Speed ≤ 50 + Not School Zone → No Action.

Existing test cases can be mapped against these rules to determine which combinations are already covered.

For example:

- Speed 55 + School Zone → Covers R1.
- Speed 44 + School Zone → Covers R2.
- Speed 77 + Not School Zone → Covers R3.
- A test where Speed ≤ 50 + Not School Zone → Covers R4.

If a test produces the same condition combination as an already covered rule, it may be considered redundant.

### Scored Examination

Decision Table Testing may become impractical when there are too many possible combinations.

For example, a 40-question examination with four possible answers per question would create an extremely large number of combinations.

Instead, other test design techniques may be more appropriate.

Using Equivalence Partitioning:

- Below 65% → Fail.
- 65% or higher → Pass.

Using Boundary Value Analysis:

- 25 correct answers → 62.5% → Fail.
- 26 correct answers → 65% → Pass.

This demonstrates that the most appropriate test technique depends on the nature and complexity of the requirement.

---

## Interview Questions

- What is Decision Table Testing?
- What are the main components of a decision table?
- What is a condition?
- What is an action?
- What is a rule in Decision Table Testing?
- How do you calculate the number of rules for binary conditions?
- What is combinatorial explosion?
- How can you reduce redundant test cases in a decision table?
- When would Decision Table Testing be more appropriate than Equivalence Partitioning?
- When might another test design technique be more appropriate than Decision Table Testing?

---

## Key Takeaways

- Decision Table Testing is a black-box test design technique for testing combinations of conditions and outcomes.
- Conditions represent inputs or prerequisites.
- Actions represent the expected system behavior.
- Each rule represents a unique combination of conditions.
- Binary conditions produce 2ⁿ possible combinations.
- The number of combinations can increase rapidly as more conditions are introduced.
- Existing test cases can be mapped to decision table rules to identify coverage gaps and duplicate tests.
- Decision tables can be optimized when complete combination testing is impractical.
- Equivalence Partitioning and Boundary Value Analysis may be more appropriate for certain requirements.
- The choice of test design technique should depend on the application's logic, risk, and testing constraints.
