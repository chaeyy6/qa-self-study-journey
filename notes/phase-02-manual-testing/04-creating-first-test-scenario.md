# Creating First Test Scenario

## Overview

Creating test scenarios is one of the first practical responsibilities of a QA Engineer.

A **Test Scenario** is a high-level statement describing **what should be tested**, not the detailed steps of how to test it.

Historically, testers created test scenarios manually from scratch. Today, Generative AI tools can assist in generating an initial draft, but it remains the tester's responsibility to review, refine, prioritize, and validate every generated scenario before it is used.

---

# Learning Objectives

After completing this lesson, you should be able to:

- Understand how the role of QA has changed with Generative AI.
- Explain why AI-generated test scenarios require review.
- Recognize common mistakes produced by AI.
- Apply prompt engineering to generate higher quality test scenarios.
- Understand that QA Engineers remain responsible for the final output.

---

# 1. Evolution of Test Scenario Creation

## Before Generative AI

Testers manually analyzed:

- Requirements
- User Stories
- Business Rules
- Design Documents
- Product Specifications

From these documents, they identified user flows and manually wrote every test scenario.

Example:

Requirement:

> Users can log in using their email address and password.

Possible manually created scenarios:

- Verify successful login using valid credentials.
- Verify login fails with an invalid password.
- Verify login fails when the email is not registered.
- Verify required field validation.
- Verify locked account behavior.

---

## Today (Generative AI)

Instead of writing everything manually, testers often ask AI to generate an initial list of scenarios.

Example prompt:

> Generate test scenarios for a Login feature.

The AI produces a draft.

The tester then:

- Reviews
- Removes duplicates
- Removes illogical scenarios
- Adds missing business scenarios
- Prioritizes them
- Validates them against requirements

The tester—not the AI—is responsible for the final version.

---

# 2. The Role of QA Has Changed

Modern QA Engineers spend less time writing scenarios from scratch and more time reviewing and improving generated output.

### Before

QA Engineer

↓

Analyze Requirements

↓

Write Test Scenarios

↓

Review

↓

Execute

### Today

Requirements

↓

AI Generates Draft

↓

QA Reviews

↓

QA Corrects

↓

QA Prioritizes

↓

QA Approves

↓

Execute

The responsibility remains with the QA Engineer.

---

# 3. Why Direct AI Output Is Often Wrong

A vague prompt usually produces vague results.

Example prompt:

> Generate test scenarios for a login page.

The AI has no context.

It begins making assumptions such as:

- Login uses email
- Login supports usernames
- Remember Me exists
- Social login exists
- CAPTCHA exists

These assumptions may not match the actual system.

---

# 4. AI Relies on Assumptions

Generative AI predicts likely answers from patterns learned during training.

It does **not** know your application's business rules unless you explicitly provide them.

Example requirement:

> Users can log in using email and password.

Without additional context, AI may assume:

- OTP login
- Google Login
- Facebook Login
- Phone Number Login
- Username Login

These features may not even exist.

---

# 5. AI Can Produce Illogical Test Scenarios

One common example discussed in the course is credential combinations.

Many AI tools generate:

- Valid Username + Valid Password
- Valid Username + Invalid Password
- Invalid Username + Valid Password
- Invalid Username + Invalid Password

However, not every combination provides unique testing value.

Example:

Invalid Username + Valid Password

This is often redundant because an invalid username cannot logically have a valid password associated with it.

Experienced testers review AI output and remove unnecessary scenarios.

---

# 6. AI Often Generates Too Many Scenarios

A simple login page may receive:

- 20 scenarios
- 30 scenarios
- 40 scenarios

Many of them are:

- duplicated
- overlapping
- low priority
- irrelevant

Executing unnecessary scenarios increases testing effort without increasing quality.

A QA Engineer should keep only scenarios that provide value.

---

# 7. Prompt Engineering Matters

Instead of asking:

> Generate Login Test Scenarios

Provide context.

Example:

Application:

- Email/password login only
- No social login
- Maximum 5 failed attempts
- Account locks for 15 minutes
- Email is mandatory
- Password is mandatory

Generate high-level test scenarios only.
Do not generate detailed test cases.
Avoid duplicate scenarios.

Providing context significantly improves AI output.

---

# 8. AI Is an Assistant, Not the Tester

AI can:

- Generate ideas
- Speed up drafting
- Suggest edge cases
- Organize scenarios

AI cannot:

- Understand undocumented business rules
- Replace requirement reviews
- Decide business priorities
- Replace QA judgment

The QA Engineer remains accountable for the final deliverables.

---

# Key Takeaways

- Test scenarios describe **what** should be tested, not **how**.
- Modern QA Engineers review AI-generated scenarios rather than blindly accepting them.
- AI-generated output should always be validated against requirements and business rules.
- Poor prompts produce poor test scenarios.
- Prompt engineering improves the quality of AI-generated scenarios.
- The final responsibility for the test scenarios always belongs to the QA Engineer.

---

# Reflection

## What did I learn?

I learned that creating test scenarios has evolved from a completely manual process to one where AI assists with generating an initial draft. However, QA Engineers remain responsible for reviewing, validating, prioritizing, and refining every scenario before execution. I also learned that prompt engineering plays an important role in producing useful AI-generated scenarios.

---

## What do I need to review?

- Writing better prompts for AI.
- Identifying redundant or illogical test scenarios.
- Reviewing AI-generated scenarios against business requirements.

---

# Interview Notes

- What is a Test Scenario?
- What is the purpose of a Test Scenario?
- How has Generative AI changed the role of QA Engineers?
- Why shouldn't testers blindly trust AI-generated test scenarios?
- Why is prompt engineering important when generating test scenarios?
- What common mistakes can AI make when generating test scenarios?
- Who is responsible for the final test scenarios—the AI or the QA Engineer?
