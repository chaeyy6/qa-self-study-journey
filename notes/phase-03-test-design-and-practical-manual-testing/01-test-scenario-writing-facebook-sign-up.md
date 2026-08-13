# Test Scenario Writing — Login & Search

## Objective

Practice analyzing login and search functionality and creating valid, invalid, and edge-case test scenarios based on authentication rules, search behavior, user state, and expected application behavior.

## 1. Login Feature Analysis

The login feature can be divided into several testable areas:

- Email Address
- Mobile Number
- Password
- Account State
- Password Recovery
- Sign-Up Navigation
- Password Visibility
- Network Conditions
- Browser and Device Compatibility

Each area should be evaluated using appropriate positive and negative scenarios.

## 2. Valid Login Test Scenarios

Examples of valid scenarios:

- Verify login using a registered email address and valid password.
- Verify login using a registered mobile number and valid password.
- Verify supported mobile number formats.
- Verify successful redirection after valid authentication.
- Verify navigation to the Password Recovery page.
- Verify navigation to the Sign-Up page.

## 3. Invalid Login Test Scenarios

Examples of invalid scenarios:

- Verify login with an unregistered email address.
- Verify login with an unregistered mobile number.
- Verify login using an invalid email format.
- Verify login using an invalid mobile number.
- Verify login using an incorrect password.
- Verify login when the email/mobile number field is empty.
- Verify login when the password field is empty.
- Verify login using an old password after a password reset.
- Verify login using a deactivated or suspended account.

### Account State Testing

Login scenarios should also consider different account states and authentication conditions.

Examples:

- Multiple consecutive failed login attempts.
- Login after an account lockout period.
- Login before account verification.
- Login using a newly reset password.

## 4. Login UI, Network & Compatibility

Additional scenarios can verify behavior outside of basic authentication:

- Verify show/hide password functionality.
- Verify password copy/paste behavior.
- Verify login behavior when there is no network connection.
- Verify login behavior under low-bandwidth conditions.
- Verify login across supported desktop browsers.
- Verify login on supported mobile and tablet browsers.
- Verify that browser navigation does not unexpectedly expose login information.

## 5. Search Feature Analysis

Search functionality can be divided into several testable areas:

- Category Search
- Course Search
- Instructor Search
- Topic/Lecture Search
- Search Accuracy
- Search Result Relevancy
- Localization
- Pagination
- User State

Search scenarios should be based on the application's defined search behavior and expected results.

## 6. Category Search

Examples of category search scenarios:

- Verify searching for a parent category.
- Verify searching for a subcategory.
- Verify searching for popular topics within a category.
- Verify behavior when a category name is misspelled.
- Verify behavior when a subcategory name is misspelled.
- Verify category searches using synonyms.
- Verify category searches using supported languages.
- Verify category searches using non-Latin scripts.

### Synonym Testing

Search scenarios can include alternative terminology for the same concept.

For example, a tester may verify whether related terms such as "QA" and "Software Testing" produce the expected results when the application supports such relationships.

## 7. Course Search

Examples of course search scenarios:

- Verify searching using an exact course name.
- Verify searching using part of a course name.
- Verify searching using a misspelled course name.
- Verify searching using text from a course description.
- Verify searching for a specific lecture title.
- Verify searching for a topic that appears in multiple lectures.
- Verify searching using supported languages.
- Verify that search results are relevant and appropriately ranked.

Expected result ranking should be determined using the application's requirements or another appropriate test oracle.

## 8. Instructor Search

Examples of instructor search scenarios:

- Verify searching using an exact instructor name.
- Verify searching using a misspelled instructor name.
- Verify searching using an instructor name combined with a course topic.
- Verify searching for instructors using different language preferences.
- Verify searching using non-Latin scripts.
- Verify expected behavior when the user is already enrolled in a course.

### User State Testing

Search behavior may vary depending on the user's state.

Examples include:

- Verify how already enrolled courses are displayed.
- Verify whether enrolled courses are identified appropriately.
- Verify whether already purchased courses are deprioritized when applicable.

## 9. Search Result & Pagination Testing

Search results should also be evaluated beyond the initial result:

- Verify that results remain relevant across multiple pages.
- Verify that duplicate results are not displayed unexpectedly.
- Verify consistent result counts.
- Verify expected result ordering.
- Verify broad or natural-language search queries.
- Verify that relevant keywords are correctly identified from search queries.

## 10. Test Oracle

A test oracle provides a basis for determining whether the observed behavior is correct.

For an established application, the existing application can be used as a reference for expected behavior.

For a newly developed application, expected behavior should instead be based on available requirements, designs, user stories, or other project documentation.

## Key Takeaways

- Login testing should cover both valid and invalid authentication conditions.
- Account state, password behavior, network conditions, and compatibility should also be considered.
- Search testing should cover different search targets such as categories, courses, and instructors.
- Search scenarios should consider exact matches, partial matches, misspellings, synonyms, localization, and result relevancy.
- User state can influence expected search behavior.
- A test oracle helps determine what the expected result should be.
- Test scenarios should describe **what should be tested**, rather than detailed execution steps.
- Scenario coverage should be based on requirements and expected application behavior.
