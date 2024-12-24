# Naming Conventions

## Test Case IDs

Format: `TC-[NUMBER]`
Example: `TC-001`, `TC-002`

## File Names

### Test Cases
Format: `[feature]_[scenario].md`
Examples:
- `login_valid_credentials.md`
- `login_invalid_password.md`
- `profile_update_email.md`

### Test Suites
Format: `[feature]_suite.md`
Examples:
- `authentication_suite.md`
- `profile_management_suite.md`

### Shared Steps
Format: `[action]_steps.md`
Examples:
- `login_steps.md`
- `navigation_steps.md`

## Component Names
- Use PascalCase
- Be specific but concise
Examples:
- `UserAuthentication`
- `ProfileManagement`
- `OrderProcessing`

## Tags
- Use lowercase
- Use hyphens for spaces
Examples:
- `smoke-test`
- `regression`
- `high-priority`
- `needs-review`

## Test Step Actions
- Start with verb
- Be clear and concise
Examples:
- "Click login button"
- "Enter username"
- "Verify error message"

## Variables
Format: `{VARIABLE_NAME}`
Examples:
- `{USERNAME}`
- `{PASSWORD}`
- `{ERROR_MESSAGE}`
