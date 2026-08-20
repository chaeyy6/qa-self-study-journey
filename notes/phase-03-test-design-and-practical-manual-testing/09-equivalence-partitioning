# Equivalence Partitioning

## Learning Objective

Understand how Equivalence Partitioning (EP) divides system inputs into logical groups where values within the same partition are expected to produce similar behavior, allowing testers to achieve effective test coverage while reducing redundant test cases.

---

## Key Concepts

- Black-Box Testing
- Equivalence Partitioning
- Valid and Invalid Partitions
- Representative Test Values
- Partition Identification
- Test Coverage

---

## My Understanding

Equivalence Partitioning is a black-box test design technique that divides system inputs into logical groups or ranges called partitions.

Instead of testing every possible input value, I can select a representative value from each partition because values within the same partition are expected to behave similarly.

Partitions can be valid or invalid. However, invalid inputs should not automatically be treated as one partition. If different invalid inputs produce different system behaviors or validation messages, they should be separated into different partitions.

For example, if an application accepts ages from 13 to 100, the inputs can be divided into partitions such as below 13, 13 to 100, and above 100. A representative value can then be selected from each partition rather than testing every possible age.

---

## QA Perspective

Equivalence Partitioning helps QA Engineers reduce redundant testing while maintaining effective test coverage.

A tester can identify partitions from explicit requirements, user stories, use cases, or business rules. When requirements do not clearly define the partitions, the tester may use testing knowledge and intuition, but the identified behavior should be validated with an appropriate source such as a Product Owner or Business Analyst.

EP can be applied to many types of functionality, including input fields, age restrictions, price ranges, order quantities, user roles, categories, and data types.

Equivalence Partitioning should also be combined with other test design techniques when appropriate, such as Boundary Value Analysis.

---

## Real-World Examples

- **Exam grading:** Scores can be divided into partitions based on defined grade ranges.
- **User registration:** Ages can be divided into valid and invalid age groups.
- **Amazon price filtering:** Products can be divided into prices below, within, or above the selected range.
- **Facebook sign-up:** Age ranges can produce different registration behaviors.
- **Udemy categories:** Courses can be grouped into categories and subcategories, allowing representative inputs to be tested.
- **Access control:** User roles such as Administrator, Registered User, and Guest can represent different permission partitions.
- **Input validation:** Text, numeric values, special characters, and different input lengths can be treated as separate partitions.

---

## Interview Questions

- What is Equivalence Partitioning?
- Why is Equivalence Partitioning considered a black-box test design technique?
- What is the difference between a valid and invalid partition?
- Why should invalid inputs sometimes be divided into multiple partitions?
- How would you apply Equivalence Partitioning to an age validation field?
- How does Equivalence Partitioning reduce redundant testing?
- Does 100% Equivalence Partitioning coverage guarantee that the application is defect-free?
- How does Equivalence Partitioning differ from Boundary Value Analysis?

---

## Key Takeaways

- Equivalence Partitioning divides inputs into logical groups expected to behave similarly.
- Testers can select representative values instead of testing every possible input.
- Partitions can be valid or invalid.
- Different invalid inputs may require separate partitions when they produce different system behavior.
- EP helps reduce redundant test cases while maintaining effective coverage.
- Requirements are an important source for identifying partitions.
- Equivalence Partitioning can be applied to ranges, categories, roles, input fields, and data types.
- 100% EP coverage does not guarantee a defect-free system.
- EP can be combined with other test design techniques such as Boundary Value Analysis.
