# Single-tier & Multi-tier Applications

## Learning Objective

Understand the differences between Single-tier and Multi-tier applications and recognize how application architecture influences software testing.

---

## Key Concepts

- Single-tier Applications
- Multi-tier Applications
- Presentation Layer
- Business Layer
- Data Layer

---

## My Understanding

This lesson introduced me to two common application architectures. A Single-tier application keeps the user interface, application logic, and data together in one system, making it relatively straightforward to develop and test.

In contrast, a Multi-tier application separates these responsibilities into different layers. Because each layer has its own role and communicates with the others, testing becomes more involved and requires verifying not only individual components but also their interactions.

---

## QA Perspective

As a QA Engineer, understanding an application's architecture can help narrow down where a defect may originate. For example, an issue could be related to the user interface, the application's business logic, or the database instead of assuming the entire application is at fault. This understanding also improves communication with developers during defect reporting.

---

## Real-World Examples

### Single-tier Applications

- Calculator
- Offline Notes App
- Alarm Clock

### Multi-tier Applications

- School Management System
- Online Banking System
- E-commerce Platform
- Social Media Platform

---

## Interview Questions

- What is the difference between a Single-tier and a Multi-tier application?
- What are the responsibilities of the Presentation, Business, and Data layers?
- Why is understanding application architecture important for a QA Engineer?

---

## Key Takeaways

- Single-tier applications combine all components into one application, making them simpler to test.
- Multi-tier applications separate responsibilities into multiple layers that communicate with one another.
- Modern software commonly uses Multi-tier architecture.
- Understanding application architecture helps QA Engineers investigate defects more effectively and communicate technical findings with the development team.
