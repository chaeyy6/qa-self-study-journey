# Design Review

## Lesson Information

**Chapter:** First Test Activity – Requirements Analysis & Design Review  
**Lesson Title:** Design Review

---

## Learning Objective

To understand how to review software wireframes and design screens against documented requirements, identify inconsistencies or ambiguities before development begins, determine when an issue should be reported as a defect, and understand the importance of Test Oracles in validating expected behavior.

---

# Notes

## Overview

After requirements have been written, designers typically create wireframes or UI mockups that represent how the application should look and behave.

As a QA Engineer, one of the earliest testing activities is **Design Review**.

Instead of executing the software, you compare the design against the approved requirements to identify inconsistencies before development begins.

Finding issues during the design stage is significantly cheaper than discovering them after implementation.

---

# Reviewing Wireframes & Design Screens

## Screen 1 – Shopping Cart Page

### Quantity Input

**Wireframe**

Shows a quantity value of **0**.

**Requirement**

The minimum quantity per item is **1**, while the maximum is **99**.

**Issue**

The wireframe contradicts the documented requirement.

Allowing zero as a quantity introduces ambiguity because the requirements specify that entering **0** should remove the item rather than remain as a valid quantity.

---

### Delete Mechanism

**Wireframe**

Clicking **Delete** immediately removes the item.

**Requirement**

Removing an item requires a confirmation modal containing:

- Remove
- Cancel

**Issue**

The confirmation step is missing from the design.

Without confirmation, users could accidentally remove products.

---

### Coupon Application

**Wireframe**

Allows up to three coupons.

**Requirement**

Only one coupon can be applied per order.

**Issue**

The design violates the business rule by permitting multiple coupon codes.

---

### Cart Totals

**Wireframe**

Displays only:

```
Total (Including Taxes)
```

**Requirement**

Display:

- Cart Subtotal (before tax)
- Applicable Tax
- Final Total

**Issue**

The design hides important pricing information required by the business.

---

### Item Count

Example:

```
Product A ×2
Product B ×1
```

Should the cart display:

```
2 Products
```

or

```
3 Items
```

The requirement does not specify this.

This ambiguity should be clarified with the Product Owner or Business Analyst before development.

---

## Screen 2 – Checkout & Payment Page

### Payment Error Messages

**Wireframe**

Displays:

```
Payment Error

Please try again.
```

**Requirement**

The system should display a specific reason such as:

- Card Declined
- Insufficient Funds

**Issue**

Generic messages make troubleshooting difficult for users.

Specific error messages improve usability.

---

### Payment Methods

**Wireframe**

Shows:

- Visa
- Mastercard
- PayPal
- American Express

**Requirement**

Only:

- Visa
- Mastercard
- PayPal

**Issue**

American Express is not part of the documented requirements.

Additional functionality should be verified with stakeholders before implementation.

---

### Cutoff Time

**Wireframe**

Displays:

```
Order before 8:00 PM
```

**Requirement**

Orders placed before:

```
17:00 UTC
```

are processed on the same business day.

**Issue**

The design does not specify whether the displayed time is:

- UTC
- User's local timezone
- Server timezone

This ambiguity could confuse users from different countries.

---

## Why Standard Timezones Matter

Many systems operate globally.

If a requirement simply states:

```
Order before 5:00 PM
```

questions immediately arise:

- 5:00 PM where?
- Philippines?
- United States?
- Europe?
- Server location?

Using a standard timezone such as **UTC** ensures that everyone interprets the requirement consistently.

Some applications convert UTC into the user's local timezone automatically, while others explicitly display UTC.

The requirement should clearly define this behavior.

---

## Screen 3 – Order Confirmation

### Status Icon

The wireframe displays a red **X** for a successful order.

Success should typically be represented using a green checkmark or another positive indicator.

Although this is largely a UI/UX concern, it should still be raised during Design Review.

---

### Confirmation Email

**Wireframe**

States:

```
No confirmation email will be sent.
```

**Requirement**

A confirmation email containing:

- Order Summary
- Total
- Estimated Delivery Date

must be sent within five minutes.

**Issue**

The design directly contradicts the documented requirement.

---

### Mathematical Values

Designs generally illustrate:

- Layout
- Positioning
- Components

They usually do **not** define:

- Tax calculations
- Backend logic
- Business calculations

These should come from the requirements or business rules.

---

# Handling Requirement vs. Application Discrepancies

## Requirement Contradicts the Application

If the application behaves differently from the approved requirements, report it as a defect.

Even if the application's behavior appears logical, the documented requirement remains the primary reference until stakeholders approve changes.

---

## Missing Functionality

If a feature planned for the current sprint is missing:

Report a defect.

If the feature belongs to a future sprint:

Do not report it as a defect.

---

## Unrequested Functionality

Sometimes developers implement additional features that were never requested.

Example:

Requirements specify:

```
Visa
Mastercard
PayPal
```

Developer also adds:

```
Apple Pay
```

Before reporting a defect, verify whether the Product Owner approved the additional functionality.

---

## Missing Essential Requirements

Occasionally neither the requirements nor the design include an important feature.

Example:

An online learning platform contains videos but has no video quality selector.

Rather than immediately reporting a defect, raise the concern with stakeholders.

The missing functionality may need to be added to the backlog.

---

## UI/UX Improvements

Not every observation is a software defect.

Suggestions such as:

- Better spacing
- Better colors
- Improved alignment
- Improved typography

should usually be raised as UI/UX improvements rather than functional defects.

---

# Test Oracles

## Definition

A **Test Oracle** is the source of truth used to determine the expected result of a test.

Whenever a tester executes a test, they compare:

```
Expected Result

vs

Actual Result
```

The Test Oracle answers the question:

> **"Where did the expected result come from?"**

Without a Test Oracle, testers would simply be guessing whether the application's behavior is correct.

---

## Why Test Oracles Are Important

Test Oracles help QA Engineers:

- Determine whether software behaves correctly.
- Avoid making assumptions.
- Detect defects objectively.
- Resolve disagreements between documentation and implementation.

---

## Common Test Oracles

Examples include:

- Functional Requirements
- User Stories
- Acceptance Criteria
- Wireframes / Figma Designs
- Product Owner
- Business Analyst
- Client
- Existing Production System

---

## Requirement vs Design Conflicts

Sometimes different project artifacts disagree.

Example:

Requirement:

```
Button should be Blue.
```

Wireframe:

```
Button is Green.
```

The tester should not decide which one is correct.

Instead, discuss the inconsistency with:

- Product Owner
- Business Analyst
- UX Designer
- Client

The team should establish the **primary Test Oracle** before testing continues.

---

# Key Takeaways

- Design Review is a Static Testing activity performed before software execution.
- QA Engineers compare wireframes against documented requirements to identify inconsistencies early.
- Ambiguous requirements should be clarified with stakeholders before implementation.
- Not every issue is a software defect—some observations are UI/UX suggestions or missing requirements.
- A Test Oracle is the source of truth used to determine the expected behavior of the software.
- QA Engineers should always ask **"According to what?"** before deciding whether something is a defect.

---

# Practical Application

I can apply this knowledge by reviewing wireframes and UI designs before development begins, ensuring they accurately reflect the documented requirements. I also understand the importance of using Test Oracles to validate expected behavior rather than relying on assumptions, allowing me to identify inconsistencies early and communicate effectively with Product Owners, Business Analysts, Developers, and Designers.

---

# Reflection

## What did I learn?

I learned that Design Review is an important Static Testing activity where QA Engineers compare wireframes and designs against requirements to identify inconsistencies before development begins. I also learned that Test Oracles provide the source of truth for determining expected behavior, helping testers make objective decisions instead of relying on assumptions.

---

## What do I need to review?

- Different sources of Test Oracles and when each should be used.
- Distinguishing functional defects from UI/UX suggestions.
- Handling conflicts between requirements, designs, and stakeholder decisions.

---

# Interview Notes

- What is Design Review?
- Why is Design Review considered Static Testing?
- What should a QA Engineer look for during a Design Review?
- What is a Test Oracle?
- Why are Test Oracles important?
- Give examples of common Test Oracles.
- How would you handle conflicting requirements and wireframes?
- What is the difference between a functional defect and a UI/UX suggestion?
- Why should ambiguous requirements be clarified before development begins?
- Why do globally used systems specify standard timezones such as UTC?
