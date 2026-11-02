# Test Automation – Candidate Scenarios

These are proposed scenarios. Execute them and confirm the observed behavior before finalizing.

## Scenario 1: Login with valid credentials
**Objective:** Verify successful authentication.

**Preconditions:** User is logged out; valid test credentials are available.

**Steps:**
1. Navigate to the login page.
2. Enter valid email.
3. Enter valid password.
4. Submit the form.

**Expected result:** User is authenticated and redirected to the expected page.

**Why automate:** Login is frequently repeated and is a prerequisite for many regression tests.

## Scenario 2: Create a new Book
**Objective:** Verify Book creation for an authorized user.

**Preconditions:** Authenticated user has permission to create Books.

**Steps:**
1. Open Books.
2. Select the create-Book action.
3. Enter a unique valid title and required fields.
4. Submit.
5. Verify the Book appears in the listing and can be opened.

**Expected result:** Book is created once and its details are accessible.

**Why automate:** This is a core workflow and needs repeatable regression coverage.

## Scenario 3: Required-field validation for Book creation
**Objective:** Verify validation when required information is missing.

**Preconditions:** Authenticated user has permission to create Books.

**Steps:**
1. Open the create-Book form.
2. Leave a required field blank.
3. Submit.
4. Check validation and whether a record is created.

**Expected result:** Clear validation appears and invalid data is not saved.

**Why automate:** Validation can regress and is straightforward to verify consistently.

## Automation Notes
- Suggested tool: Playwright.
- Use stable locators.
- Use unique test data and clean up records created by tests.
- Record results only after execution.
