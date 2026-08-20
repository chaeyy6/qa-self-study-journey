# Boundary Value Analysis

## Learning Objective

Understand how Boundary Value Analysis (BVA) extends Equivalence Partitioning by focusing on the values at the boundaries of partitions, and learn how to apply BVA to numeric ranges, age restrictions, and date-based validation.

---

## Key Concepts

- Boundary Value Analysis (BVA)
- Equivalence Partitioning (EP)
- Boundary Values
- 2-Value Boundary Testing
- Valid and Invalid Boundaries
- Date-Based Boundaries
- Boundary Coverage

---

## My Understanding

Boundary Value Analysis is a black-box test design technique that extends Equivalence Partitioning by focusing specifically on the limits or boundaries of partitions.

Instead of selecting representative values from the middle of each partition, BVA tests the values where one partition transitions into another because defects are more likely to occur at these points.

For example, if a speed limit is set to 120 km/h:

- 120 km/h is the highest value within the allowed partition.
- 121 km/h is the first value in the partition where a fine is applied.

Testing these values helps verify whether the system correctly handles the transition between the two conditions.

---

## QA Perspective

BVA helps QA Engineers identify defects that may not be discovered by testing only representative values from within a partition.

Common programming mistakes around boundaries include:

- Using `>` instead of `>=`.
- Using `<` instead of `<=`.
- Incorrectly including or excluding a boundary value.
- Overlapping conditional statements.

BVA is especially useful for higher-risk features where precision at range limits is important, such as financial calculations, tax thresholds, traffic fines, and age verification.

BVA works best when the input has clear numeric or sequential boundaries.

---

## Real-World Examples

### Exam Grading System

If scores are divided into the following ranges:

- 1–49 → Grade F
- 50–59 → Grade Pass
- 60–69 → Grade D+
- 70–79 → Grade C
- 80–89 → Grade B
- 90–100 → Grade A

BVA focuses on the transition points between these ranges.

| Boundary | Values Tested | Expected Result |
|---|---|---|
| Invalid / F | 0, 1 | Invalid / Grade F |
| F / Pass | 49, 50 | Grade F / Grade Pass |
| Pass / D+ | 59, 60 | Grade Pass / Grade D+ |
| D+ / C | 69, 70 | Grade D+ / Grade C |
| C / B | 79, 80 | Grade C / Grade B |
| B / A | 89, 90 | Grade B / Grade A |
| A / Invalid | 100, 101 | Grade A / Invalid |

Using the 2-value BVA approach results in **14 test cases** for these seven boundaries.

### Age Verification

For an application that allows users between 13 and 100 years old:

- 12 → Invalid
- 13 → Valid
- 100 → Valid
- 101 → Invalid

These values test both sides of the lower and upper boundaries.

### Date-Based Age Verification

Boundary testing can also be applied when age is calculated from a date of birth.

For example, if the reference date is January 5, 2020:

- January 5, 2007 → Valid because the user turns 13 on that day.
- January 6, 2007 → Invalid because the user turns 13 the following day.

Date-based testing may therefore require considering the exact day, month, and year.

### Leap Year Edge Case

Leap years can introduce additional boundary conditions.

When testing a February 29 birthday against a non-leap year, alternative dates such as February 28 and March 1 may need to be considered according to the application's business rules.

---

## Interview Questions

- What is Boundary Value Analysis?
- How does BVA differ from Equivalence Partitioning?
- Why are defects commonly found at boundary values?
- What is 2-value boundary testing?
- When would you use BVA?
- Can BVA be applied to every type of input?
- How would you apply BVA to an age range of 13–100?
- How would you test date-based age validation?
- What is the difference between EP coverage and BVA coverage?

---

## Key Takeaways

- Boundary Value Analysis focuses on the edges of equivalence partitions.
- BVA is an extension of Equivalence Partitioning.
- Boundary conditions are common locations for programming errors.
- 2-value BVA tests the last value of the lower partition and the first value of the upper partition.
- Both valid and invalid boundaries should be tested.
- BVA is most effective for numeric and sequential ranges.
- Date-based logic may require testing exact days, months, years, and leap-year edge cases.
- BVA generally requires more test cases than basic Equivalence Partitioning.
- EP and BVA complement each other and can be used together for stronger test coverage.
