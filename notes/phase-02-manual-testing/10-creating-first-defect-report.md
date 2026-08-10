# Creating First Defect Report

## Learning Objective

To understand how to create clear and structured defect reports using Trello, including the correct format, priority labels, screenshots, and supporting evidence.

---

## 1. Defect Board Strategies & Workflows

Kanban boards such as Trello, Jira, or Azure DevOps can be structured in different ways depending on team size and collaboration requirements.

### Internal QA vs. Developer/Stakeholder Boards

- **QA-Only Board:** Used exclusively by the testing team to write, organize, and execute test scenario suites.
- **Shared Defect Board:** Accessible to developers, product managers, and testers to discuss, prioritize, and track defects.

### Module/Device-Based Grouping

Defect cards can be grouped into lists based on platform, role, or feature.

Examples:

- Mobile Defects
- Dashboard Defects
- API Defects

Issues can receive a **Solved** or **Fixed** label once addressed.

### Status-Driven Flow

A defect board can follow a left-to-right workflow:

**New Defects → In Progress / Pending Retest → Solved / Closed**

- **New Defects:** Created by QA.
- **In Progress / Pending Retest:** Used while developers are addressing the defect or have submitted a fix for retesting.
- **Solved / Closed:** Used by QA after verifying that the defect has been fixed.

### Hybrid Workflow

A board can combine both approaches by grouping initial defects by module while maintaining dedicated **Pending Retest** and **Closed** lists at the end of the workflow.

---

## 2. Best Practices for Writing Defect Card Titles

Defect titles should be structured so that developers can quickly identify the affected module and the problem.

### Recommended Format

> [Module Name] → Clear, Specific Bug Description

### Example

> Login → Password is not case sensitive

A structured title allows developers to understand the affected area and defect type at a glance without opening the card.

---

## 3. Anatomy of a Professional Defect Report

### Title

Identifies the affected module and provides a clear description of the defect.

**Example:**

> Login → Password is not case sensitive

### Steps to Reproduce

The minimum sequential steps required to trigger the defect.

**Example:**

1. Navigate to the Login page.
2. Enter a valid email address.
3. Enter a valid password using all lowercase letters.

### Test Data

The inputs required to execute the steps and reproduce the issue.

**Example:**

```text
Email: validuser@example.com
Password: tester123
