# Test Scenario Writing — Login & Search

## Objective

Practice creating high-level test scenarios for login and search functionality by identifying valid, invalid, and feature-specific conditions that should be tested.

## 1. Login Feature Analysis

Login testing can be divided into several areas:

- Username / Email
- Password
- Login action
- Authentication
- Validation messages
- Account state
- Successful navigation

Scenarios should cover both successful and unsuccessful login attempts.

## 2. Valid Login Scenarios

Examples of valid scenarios:

- Verify login using valid credentials.
- Verify login using a valid email address and password.
- Verify that a user is redirected to the appropriate page after successful login.
- Verify that the login process works with valid credentials entered in the expected format.

## 3. Invalid Login Scenarios

Examples of invalid scenarios:

- Verify login using an incorrect password.
- Verify login using an unregistered email address.
- Verify login with an empty email field.
- Verify login with an empty password field.
- Verify login with both required fields empty.
- Verify login using an invalid email format.
- Verify that an appropriate error message is displayed after unsuccessful authentication.
- Verify that login behavior is handled correctly after repeated failed attempts.

### Single Variable Testing

When testing an invalid login condition, keep the remaining inputs valid whenever possible.

For example:

> Use a valid registered email address while changing only the password to an invalid value.

This makes it easier to identify which condition caused the failure.

## 4. Search Functionality

Search functionality should be tested using different types of search inputs and expected results.

Important areas include:

- Search input
- Search action
- Search results
- Exact matches
- Partial matches
- Invalid or unavailable searches
- Empty searches
- Search result accuracy

## 5. Search Scenarios

Examples of general search scenarios:

- Verify that a valid search term returns relevant results.
- Verify that an exact search term returns the expected result.
- Verify that a partial search term returns relevant matching results.
- Verify search behavior when no matching results exist.
- Verify search behavior when the search field is empty.
- Verify that search results are relevant to the entered keyword.
- Verify that the search action can be performed successfully.

## 6. Category Search

Category search scenarios can verify whether users can locate content based on a selected category.

Examples:

- Verify that selecting a valid category displays the appropriate results.
- Verify that the displayed results belong to the selected category.
- Verify that changing the selected category updates the results.
- Verify behavior when a category contains no matching results.
- Verify that category selection does not display results from unrelated categories.

## 7. Course Search

Course search scenarios focus on finding courses using relevant search criteria.

Examples:

- Verify that a valid course name returns the expected course.
- Verify that a partial course name returns relevant courses.
- Verify behavior when the entered course does not exist.
- Verify that search results are relevant to the entered course keyword.
- Verify that an empty course search is handled appropriately.

## 8. Instructor Search

Instructor search scenarios focus on locating courses or content associated with a particular instructor.

Examples:

- Verify that searching for a valid instructor returns relevant results.
- Verify that a partial instructor name returns appropriate results.
- Verify behavior when an instructor does not exist.
- Verify that displayed results are associated with the searched instructor.
- Verify that an empty instructor search is handled appropriately.

## 9. Scenario Organization

Search scenarios can be separated into logical groups based on the feature being tested:

- General Search
- Category Search
- Course Search
- Instructor Search

This makes the scenario set easier to review, execute, and maintain.

## Key Takeaways

- Login scenarios should cover both successful and unsuccessful authentication.
- Invalid login testing should isolate individual conditions where possible.
- Search testing should consider valid, invalid, partial, empty, and unavailable searches.
- Category, course, and instructor searches should verify both the search behavior and relevance of returned results.
- Test scenarios should describe **what should be tested** rather than providing detailed execution steps.
- Related scenarios can be grouped together to make test documentation easier to maintain.
