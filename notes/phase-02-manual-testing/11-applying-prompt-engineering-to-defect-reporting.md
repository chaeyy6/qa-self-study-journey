# Applying Prompt Engineering Techniques to Defect Reporting

## Learning Objective

To understand and apply various prompt engineering techniques to defect reporting.

---

## 1. Key Prompt Engineering Techniques for QA

Prompt engineering techniques can be used to guide generative AI tools when creating structured defect reports.

### Meta Prompting

Asking a generative AI tool to create a structured prompt that can then be used for a specific task.

**Example:**

> "I need a prompt to send to a generative tool, so that it helps me in creating defect reports for a project."

**QA Use Case:**

Creating a reusable prompt that instructs an AI tool on how to generate structured defect reports.

### Zero-Shot Prompting

Asking the AI to generate an output without providing any prior examples.

**QA Use Case:**

Providing raw defect details and asking the AI to generate a defect report without showing an example of the desired format.

### One-Shot Prompting

Providing one example of the desired output to guide the AI's formatting and response pattern.

**Example:**

> "This is an example defect that I have already created for the same project, please use it as a guide for generating new reports."

**QA Use Case:**

Providing one complete defect report, such as:

> Login → Password not case sensitive

alongside new raw defect descriptions.

### Few-Shot Prompting

Providing two or more examples of the desired output to guide the AI's response pattern.

**QA Use Case:**

Providing multiple sample defect reports representing different categories, such as:

- UI defects
- Functional defects
- Security defects

This allows the AI to identify the desired reporting pattern from multiple examples.

### Prompt Chaining

An iterative, conversational technique where prompts are progressively refined through multiple messages.

**QA Use Case:**

A tester can provide additional instructions after an initial response.

**Example:**

> "For future reports, drop preconditions and keep actual results under 15 words."

The AI can then apply the updated instructions to subsequent reports.

---

## 2. Standardization & Team Consistency

### Shared Prompt Templates

Individual testers should not create isolated, custom AI prompts for the same task.

Testing teams should standardize defect-reporting prompt templates to help maintain consistency in:

- Output length
- Structure
- Tone
- Formatting

Standardized prompts help ensure that AI-assisted defect reports follow a consistent format across the testing team.

### Conciseness Over Verbosity

Defect reports should contain the information developers need without unnecessary details.

Avoid bloated reports containing redundant information such as:

- Repeated impact analysis
- Generic preconditions
- Obvious environment details

The goal is to create **lean and actionable defect reports** that developers can quickly understand and use.

---

## 3. Screenshot & Visual Evidence Standards

### Always Include the Full URL

When capturing screenshots of web applications, include the browser address bar whenever possible.

The URL provides developers with additional context about:

- The environment
- The server
- The exact application route

### Avoid Cropped Component Screenshots

Avoid tightly cropped screenshots that show only an isolated UI component, such as:

- An input field
- A button
- A small section of the page

Cropped screenshots can hide the page hierarchy and make it more difficult to understand the context of the defect.

### Use Visual Callouts

Highlight the specific defect using clear visual annotations.

Examples:

- Bounding boxes
- Arrows
- Short explanatory text

Annotations should make the defect immediately identifiable without obscuring important UI information.

---

## 4. End-to-End QA Lifecycle Review

The overall QA workflow covered in this lesson is:

**Requirements Review → Scenario Writing → Execution → Defect Logging → Developer Fix → Retesting → Closure**

### 1. Requirements & Design Analysis

Review project specifications, requirements, and user stories.

### 2. Scenario Design

Create structured test scenarios covering:

- Positive paths
- Negative paths
- Edge cases

### 3. Test Execution

Execute scenarios sequentially using verified test data.

### 4. Defect Logging

During testing:

1. Capture rough notes when a defect is discovered.
2. Continue testing where possible.
3. Use standardized prompts to compile the notes into structured defect reports.

### 5. Triage & Developer Resolution

Assign an appropriate priority to the defect:

- High
- Medium
- Low

Developers investigate and implement fixes.

Once a fix is ready, the defect can be moved to **Pending Retest**.

### 6. Retesting & Lifecycle Resolution

Retest the defect using the original reproduction steps.

**If Fixed:**

Move the defect to **Closed / Solved**.

**If Still Reproducible:**

Reopen the defect and add comments explaining the remaining failure.

---

## Key Takeaways

- Prompt engineering techniques can assist with creating consistent defect reports.
- **Zero-shot prompting** uses no examples.
- **One-shot prompting** uses one example.
- **Few-shot prompting** uses multiple examples.
- **Meta prompting** can be used to generate reusable prompts for specific QA tasks.
- **Prompt chaining** allows instructions and outputs to be progressively refined.
- Shared prompt templates help maintain consistency across a QA team.
- Defect reports should be concise, structured, and actionable.
- Screenshots should preserve enough context to help developers understand the defect.
- Visual callouts can make defects easier to identify.
- AI-assisted reporting should support the QA process rather than replace tester judgment.
- Defects should progress through the appropriate lifecycle from logging to retesting and closure.

---

## Reflection

### What did I learn?

I learned how different prompt engineering techniques can be applied to defect reporting, including meta prompting, zero-shot prompting, one-shot prompting, few-shot prompting, and prompt chaining.

I also learned how standardized prompts can help maintain consistency when using AI to assist with defect reporting.

Additionally, I learned that visual evidence should contain enough context to help developers understand a defect and that screenshots should use appropriate annotations when necessary.

### What do I need to review?

- The differences between zero-shot, one-shot, and few-shot prompting.
- When to use each prompt engineering technique.
- How to create reusable prompts for defect reporting.
- How prompt engineering can support the QA lifecycle.
- Best practices for screenshots and visual defect evidence.

---

## Interview Notes

- **Zero-Shot Prompting:** Asking AI to generate an output without providing examples.
- **One-Shot Prompting:** Providing one example to guide the AI's output.
- **Few-Shot Prompting:** Providing multiple examples to guide the AI's output.
- **Meta Prompting:** Asking AI to generate a prompt for a specific task.
- **Prompt Chaining:** Refining an AI's output through multiple prompts or interactions.
- Shared prompts can help QA teams maintain consistent defect-reporting formats.
- AI can assist with defect reporting, but testers should still verify the accuracy and completeness of the generated information.
- Defect reports should be clear, concise, and actionable.
