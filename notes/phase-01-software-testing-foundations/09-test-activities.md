# Test Activities

## Learning Objective

Understand the difference between testing and debugging, the Software Testing Life Cycle (STLC), and the different test levels used throughout software development.

---

## Key Concepts

- Testing vs Debugging
- Software Testing Life Cycle (STLC)
- Test Activities
- Test Levels
- System Integration Testing (SIT)

---

## My Understanding

Software testing is much more than simply executing test cases. It follows a structured life cycle that begins with planning and continues through analysis, design, implementation, execution, monitoring, and completion.

I also learned that testing and debugging are different activities. Testing focuses on discovering defects, while debugging focuses on identifying the root cause and fixing those defects.

Another important concept was understanding the different levels of testing. Software is first validated at the unit level, then component integration, followed by system testing, system integration testing, and finally acceptance testing before release.

---

## STLC Overview

### Test Planning
- Define testing strategy
- Create test plan
- Determine scope, schedule, resources, risks, and tools

### Test Monitoring & Control
- Monitor testing progress
- Track defects and risks
- Adjust testing activities when necessary

### Test Analysis
- Review requirements
- Identify what needs to be tested

### Test Design
- Create test scenarios
- Write test cases
- Prepare test data

### Test Implementation
- Prepare the testing environment
- Organize test suites
- Prepare automation scripts when applicable

### Test Execution
- Execute test cases
- Compare expected and actual results
- Log and report defects

### Test Completion
- Verify exit criteria
- Prepare test summary reports
- Archive testing artifacts
- Close testing activities

---

## Test Levels

### Unit Testing
- Performed by Developers
- Tests individual functions, methods, or classes

### Component Integration Testing
- Performed by Developers and Testers
- Verifies communication between modules, APIs, databases, and services

### System Testing
- Performed by QA Testers
- Tests the complete application against business requirements

### System Integration Testing (SIT)
- Performed by QA Testers
- Verifies communication between multiple complete systems after each has passed System Testing

### Acceptance Testing (UAT)
- Performed by Clients or End Users
- Confirms that the software satisfies business requirements before production release

---

## QA Perspective

A QA Engineer contributes throughout the Software Testing Life Cycle, not only during test execution. Planning, requirement analysis, test design, execution, and reporting all play important roles in delivering quality software.

Understanding the different test levels also helps testers know where defects originate and which team should investigate them.

---

## Real-World Examples

**Unit Testing**
- Verify that a `calculateTax()` function returns the correct value.

**Component Integration Testing**
- Verify that the Login page successfully communicates with the database.

**System Testing**
- Verify that a customer can register, log in, place an order, complete payment, and receive a confirmation email.

**System Integration Testing**
- Verify that the Customer App, Restaurant App, Driver App, and Payment Gateway work together correctly.

**Acceptance Testing**
- Verify that the final product satisfies the client's business requirements before release.

---

## Interview Questions

- What is the Software Testing Life Cycle (STLC)?
- What is the difference between testing and debugging?
- Explain the stages of the STLC.
- What is the difference between Test Analysis and Test Design?
- What is the difference between Unit, Integration, System, and Acceptance Testing?
- What is the difference between Component Integration Testing and System Integration Testing?
- Who performs each test level?

---

## Key Takeaways

- Testing and debugging have different responsibilities.
- Software testing follows a structured life cycle known as the STLC.
- Testing begins long before execution.
- Different test levels validate software from individual components to complete business systems.
- Understanding the testing process helps QA Engineers collaborate effectively with the entire development team.
