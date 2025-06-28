# Test Generation Instructions

## Test Planning and Strategy

### Pre-Test Generation Assessment

- **Analyze code under test**: Understand functionality, inputs, outputs, and side effects
- **Identify test scenarios**: Happy path, edge cases, error conditions, and boundary values
- **Determine test types**: Unit, integration, end-to-end, performance, and security tests
- **Review existing tests**: Understand current coverage and avoid duplication
- **Consider dependencies**: Identify external dependencies that need mocking or stubbing

### Test Coverage Strategy

- **Function coverage**: Test all public functions and methods
- **Branch coverage**: Test all code paths and conditional branches
- **Statement coverage**: Ensure all executable statements are tested
- **Edge case coverage**: Test boundary conditions and limit values
- **Error path coverage**: Test exception handling and error scenarios
- **Integration coverage**: Test component interactions and data flow

## Test Structure and Organization

### Test File Organization

- **Naming conventions**: Use consistent naming patterns (e.g., `test_*.py`, `*.test.js`)
- **File structure**: Mirror source code structure in test directories
- **Test grouping**: Group related tests logically (by feature, class, or module)
- **Test separation**: Separate unit tests from integration and end-to-end tests
- **Shared utilities**: Create reusable test utilities and helper functions
- **Test data management**: Organize test data and fixtures appropriately

### Test Case Structure

- **Descriptive names**: Use clear, descriptive test names that explain what is being tested
- **AAA pattern**: Arrange (setup), Act (execute), Assert (verify) structure
- **Single responsibility**: Each test should verify one specific behavior
- **Test independence**: Tests should not depend on other tests or execution order
- **Clear assertions**: Use specific assertions that clearly indicate what is expected
- **Meaningful failure messages**: Provide helpful error messages when tests fail

## Test Quality Guidelines

### Comprehensive Test Coverage

- **Happy path testing**: Test normal, expected usage scenarios
- **Edge case testing**: Test boundary conditions, empty inputs, maximum values
- **Error testing**: Test invalid inputs, network failures, and exception scenarios
- **State testing**: Test different system states and state transitions
- **Concurrency testing**: Test thread safety and race conditions where applicable
- **Performance testing**: Test response times and resource usage for critical paths

### Test Data Management

- **Realistic test data**: Use data that reflects real-world usage patterns
- **Data variety**: Test with different data types, sizes, and formats
- **Test isolation**: Each test should use independent test data
- **Data cleanup**: Ensure tests clean up after themselves
- **Fixtures and factories**: Use test fixtures and data factories for consistent setup
- **Sensitive data**: Never use real sensitive data in tests

### Mock and Stub Strategy

- **External dependencies**: Mock external services, databases, and APIs
- **Slow operations**: Mock time-consuming operations for faster test execution
- **Non-deterministic behavior**: Mock random number generation, current time, etc.
- **Mock verification**: Verify that mocks are called with expected parameters
- **Mock isolation**: Ensure mocks don't affect other tests
- **Realistic mocks**: Make mocks behave like real dependencies

## Test Implementation Best Practices

### Assertion Quality

- **Specific assertions**: Use the most specific assertion available
- **Multiple assertions**: Group related assertions logically within tests
- **Custom assertions**: Create custom assertions for domain-specific validations
- **Assertion messages**: Include helpful messages explaining what went wrong
- **Negative testing**: Test that invalid operations fail as expected
- **Exception testing**: Verify specific exceptions are thrown with correct messages

### Test Performance

- **Fast execution**: Keep tests fast to encourage frequent running
- **Parallel execution**: Design tests to run in parallel when possible
- **Resource efficiency**: Minimize memory and CPU usage in tests
- **Test timeout**: Set appropriate timeouts for async operations
- **Cleanup efficiency**: Efficient setup and teardown procedures
- **Test selection**: Allow running subsets of tests for different scenarios

### Test Maintainability

- **DRY principle**: Avoid duplicating test setup and assertion logic
- **Test utilities**: Create reusable helper functions for common operations
- **Clear documentation**: Document complex test scenarios and setup requirements
- **Version compatibility**: Ensure tests work across different environment versions
- **Regular maintenance**: Update tests when production code changes
- **Refactoring tests**: Refactor tests to improve clarity and efficiency

## Language-Agnostic Testing Principles

### Universal Testing Concepts

- **Test-driven development**: Write tests before or alongside implementation
- **Behavior verification**: Test what the code does, not how it does it
- **Interface testing**: Test public interfaces rather than implementation details
- **Regression prevention**: Ensure tests prevent future regressions
- **Documentation value**: Tests should serve as living documentation
- **Continuous integration**: Tests should run automatically in CI/CD pipelines

### Testing Patterns

- **Setup/Teardown**: Consistent setup and cleanup patterns
- **Test factories**: Patterns for creating test objects and data
- **Page object model**: For UI testing, encapsulate page interactions
- **Repository pattern**: For data layer testing, abstract data access
- **Builder pattern**: For complex test object creation
- **Strategy pattern**: For testing different implementations of same interface

## Test Categories and Guidelines

### Unit Tests

- **Scope**: Test individual functions, methods, or classes in isolation
- **Speed**: Should be fast (milliseconds) and run frequently
- **Dependencies**: Mock all external dependencies
- **Coverage**: Aim for high code coverage (80%+ for critical code)
- **Granularity**: Test one logical unit of functionality per test
- **Deterministic**: Should produce consistent results every time

### Integration Tests

- **Scope**: Test interaction between multiple components or modules
- **Real dependencies**: Use real implementations where possible
- **Data persistence**: Test with actual databases or file systems
- **Network communication**: Test API calls and service interactions
- **Configuration**: Test with realistic configuration settings
- **Environment**: Run in environment similar to production

### End-to-End Tests

- **User scenarios**: Test complete user workflows and business processes
- **Full stack**: Test entire application stack from UI to database
- **Real environment**: Run against production-like environments
- **User perspective**: Focus on user goals and outcomes
- **Critical paths**: Prioritize most important user journeys
- **Maintenance**: Keep small number of high-value E2E tests

### Performance Tests

- **Load testing**: Test behavior under expected load
- **Stress testing**: Test behavior under extreme conditions
- **Baseline establishment**: Establish performance baselines
- **Resource monitoring**: Monitor CPU, memory, and network usage
- **Scalability testing**: Test horizontal and vertical scaling
- **Regression detection**: Detect performance regressions

## Test Documentation and Reporting

### Test Documentation

- **Test purpose**: Document what each test validates and why
- **Test scenarios**: Describe the scenarios being tested
- **Prerequisites**: Document any setup requirements or dependencies
- **Expected outcomes**: Clearly state expected test results
- **Troubleshooting**: Include common issues and solutions
- **Maintenance notes**: Document known limitations or future improvements

### Test Reporting

- **Coverage reports**: Generate and review code coverage reports
- **Test results**: Provide clear pass/fail status with details
- **Performance metrics**: Track test execution time and resource usage
- **Trend analysis**: Monitor test health and coverage trends over time
- **Failure analysis**: Provide detailed information for test failures
- **Quality metrics**: Track test quality indicators and improvements

## Continuous Testing Integration

### CI/CD Integration

- **Automated execution**: Tests run automatically on code changes
- **Fast feedback**: Provide quick feedback to developers
- **Quality gates**: Block deployments if critical tests fail
- **Test environments**: Maintain consistent test environments
- **Parallel execution**: Run tests in parallel to reduce execution time
- **Result reporting**: Integrate test results with development workflow

### Test Maintenance

- **Regular review**: Regularly review and update test suites
- **Obsolete test removal**: Remove tests that no longer provide value
- **Test refactoring**: Improve test quality and maintainability
- **Coverage analysis**: Regularly analyze and improve test coverage
- **Performance monitoring**: Monitor and optimize test execution performance
- **Tool updates**: Keep testing tools and frameworks up to date
