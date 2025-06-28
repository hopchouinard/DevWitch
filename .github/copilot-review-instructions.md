# Code Review Instructions

## Pre-Review Validation

**MANDATORY STEP**: Before conducting code review, you must:

1. **Locate and review the task document** referenced in the PR or commit
2. **Validate against task requirements** from `ai_docs/templates/task_template.md` structure
3. **Check task completion criteria** to ensure all requirements are addressed
4. **Verify scope alignment** between task document and actual implementation

This ensures the review validates both code quality and requirement fulfillment.

## Review Methodology

### Systematic Review Process

- **Requirements verification**: Check implementation against documented requirements
- **Architecture review**: Validate design decisions and patterns used
- **Code quality assessment**: Evaluate readability, maintainability, and best practices
- **Security analysis**: Identify potential security vulnerabilities
- **Performance evaluation**: Assess efficiency and scalability concerns
- **Testing validation**: Verify test coverage and quality

### Review Scope Prioritization

1. **Critical path functionality**: Focus on core business logic first
2. **Security-sensitive areas**: Authentication, authorization, data handling
3. **Performance-critical sections**: Algorithms, database queries, loops
4. **Public APIs**: External interfaces and contracts
5. **Error handling paths**: Exception handling and edge cases
6. **Configuration and deployment**: Infrastructure and setup code

## Task Document Validation

### Requirement Verification

- **Functional requirements**: All specified features are implemented correctly
- **Non-functional requirements**: Performance, security, usability requirements met
- **Acceptance criteria**: Each criterion from task document is satisfied
- **Scope boundaries**: Implementation stays within defined scope
- **Dependencies**: Required dependencies are correctly implemented or integrated

### Task Completion Checklist

- [ ] All user stories from task document are implemented
- [ ] Acceptance criteria are met and testable
- [ ] Technical requirements are fulfilled
- [ ] Documentation requirements are completed
- [ ] Testing requirements are satisfied
- [ ] Deployment/integration requirements are addressed

## Code Quality Assessment

### Structure and Design

- **Single Responsibility Principle**: Each class/function has one clear purpose
- **Separation of concerns**: Logical separation between different responsibilities
- **DRY principle**: No unnecessary code duplication
- **SOLID principles**: Adherence to object-oriented design principles
- **Design patterns**: Appropriate use of established patterns
- **Modularity**: Good module boundaries and cohesion

### Code Readability

- **Naming conventions**: Clear, descriptive names for variables, functions, classes
- **Code organization**: Logical file and folder structure
- **Comment quality**: Meaningful comments explaining "why" not "what"
- **Code complexity**: Functions and classes are appropriately sized
- **Consistency**: Consistent style and patterns throughout codebase
- **Self-documenting code**: Code that explains itself through structure

### Error Handling and Robustness

- **Exception handling**: Proper try-catch blocks with specific error types
- **Input validation**: All inputs validated at appropriate boundaries
- **Edge cases**: Boundary conditions and unusual inputs handled
- **Resource management**: Proper cleanup of resources (files, connections, memory)
- **Graceful degradation**: System continues to function when components fail
- **Error messages**: Clear, actionable error messages for users and developers

## Security Review

### Common Vulnerabilities

- **Injection attacks**: SQL injection, XSS, command injection prevention
- **Authentication flaws**: Proper authentication implementation
- **Authorization issues**: Correct access control and permissions
- **Data exposure**: No sensitive data in logs, responses, or client-side code
- **Cryptography**: Proper use of encryption and hashing
- **Input sanitization**: All user inputs properly sanitized

### Security Best Practices

- **Least privilege principle**: Minimal required permissions granted
- **Defense in depth**: Multiple layers of security controls
- **Secure defaults**: Secure configuration by default
- **Input validation**: Whitelist validation over blacklist
- **Output encoding**: Proper encoding for different contexts
- **Session management**: Secure session handling and timeout

## Performance Review

### Efficiency Analysis

- **Algorithm complexity**: Appropriate time and space complexity
- **Database optimization**: Efficient queries and proper indexing
- **Memory usage**: No memory leaks or excessive memory consumption
- **I/O operations**: Efficient handling of file and network operations
- **Caching strategies**: Appropriate use of caching mechanisms
- **Resource pooling**: Proper connection and resource pooling

### Scalability Considerations

- **Concurrent access**: Thread safety and race condition prevention
- **Load handling**: Ability to handle increased load
- **Resource scaling**: Efficient resource utilization
- **Bottleneck identification**: Potential performance bottlenecks identified
- **Async operations**: Proper use of asynchronous programming
- **Rate limiting**: Implementation of rate limiting where appropriate

## Testing Validation

### Test Coverage Analysis

- **Unit test coverage**: Adequate coverage of individual functions/methods
- **Integration test coverage**: Testing of component interactions
- **End-to-end testing**: Complete user workflow testing
- **Edge case testing**: Testing of boundary conditions
- **Error path testing**: Testing of error handling scenarios
- **Performance testing**: Load and stress testing where appropriate

### Test Quality Assessment

- **Test independence**: Tests don't depend on each other
- **Test clarity**: Tests are readable and well-documented
- **Test data**: Realistic and varied test data used
- **Mock usage**: Appropriate use of mocks and stubs
- **Test maintenance**: Tests are maintainable and update with code changes
- **Assertion quality**: Meaningful assertions that validate expected behavior

## Documentation Review

### Code Documentation

- **API documentation**: Complete documentation for public interfaces
- **Inline comments**: Appropriate comments for complex logic
- **README updates**: Project documentation reflects changes
- **Architecture documentation**: High-level design documentation
- **Deployment documentation**: Setup and deployment instructions
- **Troubleshooting guides**: Common issues and solutions documented

### Documentation Quality

- **Accuracy**: Documentation matches actual implementation
- **Completeness**: All necessary information included
- **Clarity**: Documentation is clear and easy to understand
- **Examples**: Practical examples provided where helpful
- **Maintenance**: Documentation is up-to-date with latest changes
- **Accessibility**: Documentation is accessible to target audience

## Review Feedback Guidelines

### Constructive Feedback

- **Specific issues**: Point to specific lines or sections with issues
- **Explanation**: Explain why something is a problem
- **Suggestions**: Provide alternative approaches or solutions
- **Priority levels**: Indicate severity (critical, major, minor, suggestion)
- **Learning opportunities**: Share knowledge and best practices
- **Positive reinforcement**: Acknowledge good practices and improvements

### Feedback Categories

- **Must fix**: Critical issues that must be addressed before merge
- **Should fix**: Important issues that should be addressed
- **Consider**: Suggestions for improvement
- **Nitpick**: Minor style or preference issues
- **Question**: Request for clarification or explanation
- **Praise**: Recognition of good practices

## Review Completion Checklist

### Final Validation

- [ ] All task requirements verified and implemented
- [ ] Code quality meets project standards
- [ ] Security considerations addressed
- [ ] Performance requirements satisfied
- [ ] Testing coverage and quality adequate
- [ ] Documentation complete and accurate
- [ ] No blocking issues remain
- [ ] Feedback provided constructively
- [ ] Review summary completed

### Sign-off Criteria

- Code fulfills all requirements from task document
- No critical security or performance issues
- Adequate test coverage with quality tests
- Documentation is complete and accurate
- Code follows project standards and conventions
- All reviewer feedback has been addressed satisfactorily
