---
mode: "agent"
tools: ['context7']
description: "Create unit tests for a file or function using the preferred testing framework"
---

# Generate Tests

Create comprehensive unit tests for the selected code. Follow these guidelines:

## Requirements

- Use the appropriate testing framework (Pytest for Python, Mocha/Jest for JavaScript, etc.)
- Cover all public methods and functions
- Include edge cases and error conditions
- Follow naming conventions (test\_\* for Python, describe/it for JavaScript)
- Aim for high code coverage

## Test Structure

Generate tests that include:

1. **Happy path tests** - Normal expected usage
2. **Edge cases** - Boundary conditions and limits
3. **Error cases** - Invalid inputs and exception handling
4. **Mock tests** - For external dependencies when needed

## Test Organization

- Group related tests logically
- Use descriptive test names that explain what is being tested
- Include setup and teardown when necessary
- Add comments for complex test scenarios

## Output Format

Provide:

- Complete test file with proper imports
- Test fixtures and data when needed
- Assertions that validate expected behavior
- Documentation for any special test requirements

Ensure tests are independent and can run in any order.
