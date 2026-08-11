# Test Scenario Writing — Facebook Sign Up

## Objective

Practice analyzing a sign-up feature and creating valid and invalid test scenarios based on field requirements, validation rules, and boundary conditions.

## 1. Sign-Up Feature Analysis

The sign-up form can be divided into several testable areas:

- First Name
- Surname
- Email Address / Mobile Number
- Password
- Date of Birth
- Gender
- Sign-Up action

Each field should be evaluated using appropriate valid and invalid scenarios.

## 2. Valid Test Scenarios

Examples of valid scenarios:

- Verify registration using valid required information.
- Verify registration using a valid first name and surname.
- Verify registration using a valid email address.
- Verify registration using a valid mobile number.
- Verify registration using a valid password.
- Verify registration using a valid date of birth.
- Verify that each available gender option can be selected.
- Verify successful registration when all required information is valid.

## 3. Invalid Test Scenarios

Examples of invalid scenarios:

- Verify registration when a required field is left empty.
- Verify registration using an invalid email format.
- Verify registration using an invalid mobile number.
- Verify registration using an invalid password.
- Verify registration using an invalid date of birth.
- Verify that appropriate validation feedback is displayed for invalid input.

### Single Variable Testing

When testing an invalid field, keep the remaining fields valid.

This makes it easier to determine which input caused the validation failure.

## 4. Password Validation

Password scenarios should be based on the application's defined password requirements.

Possible scenarios include:

- Password meeting all requirements.
- Password below the minimum length.
- Password missing a required character type.
- Empty password.
- Password at relevant length boundaries.

Validation rules should come from the requirements rather than assumptions made by the tester.

## 5. Date of Birth Validation

Age-related restrictions can be tested using valid and invalid age ranges.

Examples:

- Valid age.
- Age below the minimum allowed age.
- Age at the minimum boundary.
- Age above the minimum allowed age.
- Invalid date values.

Boundary conditions are particularly useful when the system has defined age restrictions.

## 6. Scenario Maintenance

Test scenarios should be reviewed when requirements or application behavior changes.

If a new requirement introduces another supported input method or validation rule, the existing scenario set should be updated accordingly.

Defects discovered during execution can also result in new scenarios being added to the regression suite.

## Key Takeaways

- Test scenarios describe **what should be tested**.
- Both valid and invalid conditions should be considered.
- Requirements should drive scenario creation.
- Invalid testing should isolate one variable whenever possible.
- Boundary conditions can reveal important validation defects.
- Test scenarios should be maintained as requirements and application behavior evolve.
