# Basics of Agile & Agile Testing

## Learning Objective

Understand the core values and principles of Agile, recognize the differences between Agile and traditional sequential development, and understand how these differences affect the role of software testing.

---

## Key Concepts

- Agile 4 Values
- Agile 12 Principles
- Agile Development
- Traditional / Sequential / Waterfall Development
- Fixed vs Estimated
- Agile Testing
- Static Testing
- Dynamic Testing

---

## My Understanding

Agile is an approach to software development that emphasizes collaboration, working software, customer feedback, and responding to change.

The Agile Manifesto is built around four values:

1. **Individuals and Interactions over Processes and Tools**
2. **Working Software over Comprehensive Documentation**
3. **Customer Collaboration over Contract Negotiation**
4. **Responding to Change over Following a Plan**

The items on the right still have value. However, when there is a conflict between the two, Agile gives greater priority to the items on the left.

### Agile 4 Values

#### 1. Individuals and Interactions over Processes and Tools

Agile prioritizes communication, collaboration, and interaction between people.

**Example:**  
If a tester discovers a confusing requirement, discussing it directly with the developer or Product Owner may resolve the issue faster than relying entirely on formal communication.

#### 2. Working Software over Comprehensive Documentation

Agile prioritizes working and testable software over creating extensive documentation.

**Example:**  
Testing an actual login feature provides more useful feedback about its behavior than only reviewing a document describing how login should work.

#### 3. Customer Collaboration over Contract Negotiation

Agile encourages continuous collaboration with customers and stakeholders.

**Example:**  
Customer feedback may reveal that a feature does not behave as expected, allowing the team to clarify the requirement before continuing development.

#### 4. Responding to Change over Following a Plan

Agile accepts that requirements and business needs can change.

**Example:**  
If a requirement changes during development, the team can adapt the feature and update the affected test cases.

### Agile 12 Principles

The twelve principles provide practical guidance for applying the Agile values.

1. **Customer Satisfaction** — Deliver valuable software early and continuously.
2. **Welcome Changing Requirements** — Accept changes even later in development when they provide value.
3. **Frequent Delivery** — Deliver working software frequently in short cycles.
4. **Daily Collaboration** — Business stakeholders and developers work closely together.
5. **Build Around Motivated People** — Give teams the support and trust they need.
6. **Face-to-Face Communication** — Direct communication is an effective way to share information.
7. **Working Software** — Working software is a primary measure of progress.
8. **Sustainable Pace** — Teams should be able to maintain a consistent pace over time.
9. **Technical Excellence** — Good design and technical practices improve agility.
10. **Simplicity** — Maximize the amount of work not done by avoiding unnecessary work.
11. **Self-Organizing Teams** — Teams should determine how best to accomplish their work.
12. **Regular Reflection** — Teams regularly reflect and adjust how they work.

### Traditional / Sequential Development

Traditional sequential development, commonly represented by the **Waterfall model**, generally follows predefined phases.

A simplified workflow is:

**Requirements → Design → Development → Testing → Release**

The project generally defines its requirements and scope early, then estimates the time and resources required to complete them.

### Agile Development

Agile development works through short, iterative cycles.

A simplified workflow is:

**Plan → Develop → Test → Review → Improve → Repeat**

Instead of waiting until the entire product is completed, working software is delivered incrementally and feedback is gathered throughout development.

---

## QA Perspective

Agile changes how QA participates in software development.

In traditional sequential development, testing is often concentrated after development, although static testing such as requirement and design reviews can happen earlier.

In Agile, testing is performed continuously as features are developed.

A QA Engineer may:

1. Review requirements.
2. Help clarify acceptance criteria.
3. Design test cases.
4. Test developed features.
5. Report defects.
6. Retest fixes.
7. Perform regression testing.
8. Provide feedback.
9. Participate in retrospectives.

### Fixed vs Estimated

A useful way to understand the difference between traditional and Agile development is to look at what is fixed and what is estimated.

| Aspect | Traditional / Waterfall | Agile |
|---|---|---|
| **Requirements / Scope** | Fixed | Estimated / Flexible |
| **Time** | Estimated | Fixed |
| **Cost / Resources** | Estimated | Fixed / Relatively Fixed |
| **Development** | Sequential | Iterative |
| **Testing** | Often later, with early static reviews | Continuous dynamic testing |
| **Requirement Changes** | More difficult and costly | Expected and accommodated |
| **Customer Feedback** | Usually less frequent | Frequent |
| **Delivery** | Often one major release | Frequent increments |

### Simple Way to Remember

**Traditional / Waterfall:**

> **Scope is fixed → estimate Time and Cost**

**Agile:**

> **Time and Cost are fixed → estimate and prioritize Scope**

### Testing Impact

**Traditional Development:**

There is a strong focus on reviewing requirements, specifications, and designs early because mistakes discovered later can be expensive to fix.

**Agile Development:**

There is a strong focus on testing actual working software because features are developed and delivered incrementally.

---

## Real-World Examples

### Traditional / Sequential Development

- Building a bridge
- Building a car
- Large infrastructure projects
- Projects with highly stable and predefined requirements

These projects often require significant planning before implementation because changing requirements later can be expensive.

### Agile Development

- Mobile applications
- E-commerce platforms
- Web applications
- SaaS products
- Products with frequently changing customer requirements

For example, an app being prepared for Black Friday may have a fixed launch date and development team. The team prioritizes the most valuable features that can realistically be completed before the deadline.

---

## Interview Questions

- What is Agile?
- What are the four Agile values?
- What are the twelve Agile principles?
- How does Agile differ from Waterfall?
- What is fixed in traditional development?
- What is fixed in Agile?
- What does Agile mean by responding to change?
- Why is working software important in Agile?
- How does Agile affect software testing?
- What is the difference between static and dynamic testing?
- Why is testing performed continuously in Agile?
- Does Agile mean there is no documentation?
- Does Agile mean there is no planning?
- What role does a QA Engineer play in an Agile team?

---

## Key Takeaways

- Agile is based on four core values and twelve principles.
- Agile emphasizes collaboration, working software, customer involvement, and responding to change.
- The items on the right side of the Agile values still have value, but the items on the left take priority when they conflict.
- Traditional sequential development generally fixes the scope and estimates the time and resources required.
- Agile generally fixes the available time and resources while allowing scope to be prioritized and adjusted.
- Traditional development is generally sequential, while Agile is iterative and incremental.
- Agile encourages frequent delivery and customer feedback.
- QA Engineers participate throughout the Agile development cycle.
- Agile testing is continuous and focuses heavily on testing working software.
- Understanding the development approach helps a QA Engineer determine how and when testing should be performed.
