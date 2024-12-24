# Writing Test Cases

## Structure

Each test case should include:

1. **Metadata** (YAML frontmatter):
   ```yaml
   ---
   title: Test Case Title
   id: TC-XXX
   component: Component Name
   priority: High/Medium/Low
   status: Active/Draft/Deprecated
   tags: [tag1, tag2]
   ---
   ```

2. **Test Objective**
   - Clear statement of what is being tested
   - One sentence, specific and measurable

3. **Prerequisites**
   - System state before test execution
   - Required data or configurations
   - Dependencies on other test cases

4. **Test Steps**
   - Use table format for clarity
   - Each step should be atomic
   - Include test data
   - Clear expected results

5. **Post-conditions**
   - System state after test execution
   - Cleanup steps if needed

## Best Practices

1. **Naming Convention**
   - Use descriptive names
   - Follow the pattern: `[Feature]_[Scenario].md`
   - Example: `login_valid_credentials.md`

2. **Test Data**
   - Use realistic data
   - Separate test data from test steps
   - Use variables for reusable data

3. **Reusability**
   - Use shared steps for common actions
   - Reference prerequisites clearly
   - Keep test cases atomic

4. **Documentation**
   - Include relevant screenshots or diagrams
   - Document edge cases
   - Keep test cases up to date

## Example

See [Login Test Case](../test-cases/functional/login.md) for a complete example.
