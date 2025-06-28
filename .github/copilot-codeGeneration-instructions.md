# Code Generation Instructions

## Pre-Code Generation Workflow

**MANDATORY STEP**: Before generating any code, you must:

1. **Create a task planning document** following the structure in `ai_docs/templates/task_template.md`
2. **Present the task document** to the user for review and approval
3. **Wait for explicit user confirmation** ("proceed", "go ahead", "approved", etc.)
4. **Only then begin code generation** following the guidelines below

This ensures proper planning, requirements validation, and user alignment before implementation.

## General Code Quality Guidelines

### Code Structure and Organization

- **Modularity**: Write modular, reusable components with single responsibilities
- **Separation of concerns**: Keep business logic, data access, and presentation layers separate
- **File organization**: Use consistent directory structure and file naming conventions
- **Dependencies**: Minimize coupling between modules and components
- **Abstractions**: Create appropriate abstractions without over-engineering

### Naming Conventions

- **Variables**: Use descriptive, self-documenting names (avoid abbreviations)
- **Functions/Methods**: Use verbs that clearly describe what the function does
- **Classes/Types**: Use nouns that represent the entity or concept
- **Constants**: Use UPPER_CASE for true constants, descriptive names for configuration
- **Files/Modules**: Use consistent naming that reflects the module's purpose

### Code Readability and Documentation

- **Comments**: Explain "why" not "what" - focus on business logic and complex algorithms
- **Documentation**: Include comprehensive docstrings/comments for public APIs
- **Code style**: Follow language-specific style guides and formatting conventions
- **Self-documenting code**: Write code that explains itself through clear structure and naming
- **Examples**: Provide usage examples for complex functions or APIs

## Error Handling and Robustness

### Error Management

- **Explicit error handling**: Handle errors explicitly, don't let them fail silently
- **Appropriate error types**: Use specific error types/exceptions for different scenarios
- **Error messages**: Provide clear, actionable error messages for users and developers
- **Graceful degradation**: Handle failures gracefully with fallback mechanisms
- **Input validation**: Validate all inputs at system boundaries

### Defensive Programming

- **Null safety**: Handle null/undefined values appropriately
- **Boundary checks**: Validate array bounds, string lengths, and numeric ranges
- **Type safety**: Use strong typing where available and validate types at runtime when needed
- **Resource management**: Properly manage resources (files, connections, memory)
- **Edge cases**: Consider and handle edge cases and unusual inputs

## Performance and Efficiency

### Optimization Principles

- **Algorithmic efficiency**: Choose appropriate algorithms and data structures
- **Resource usage**: Minimize memory allocation and CPU usage
- **Lazy loading**: Load resources only when needed
- **Caching**: Implement appropriate caching strategies for expensive operations
- **Database optimization**: Use efficient queries and minimize database round trips

### Scalability Considerations

- **Async operations**: Use asynchronous programming for I/O operations
- **Batch processing**: Process data in batches when dealing with large datasets
- **Connection pooling**: Reuse connections and resources efficiently
- **Rate limiting**: Implement rate limiting for external API calls
- **Memory management**: Avoid memory leaks and excessive memory usage

## Security Best Practices

### Input Security

- **Input sanitization**: Sanitize all user inputs to prevent injection attacks
- **Input validation**: Validate input format, length, and content
- **Parameter binding**: Use parameterized queries to prevent SQL injection
- **File uploads**: Validate file types, sizes, and scan for malicious content
- **URL validation**: Validate and sanitize URLs and redirects

### Data Protection

- **Sensitive data**: Never log or expose sensitive information (passwords, keys, tokens)
- **Encryption**: Use appropriate encryption for sensitive data at rest and in transit
- **Access control**: Implement proper authentication and authorization
- **Secrets management**: Use secure secret management systems, not hardcoded values
- **Data minimization**: Only collect and store necessary data

## Testing and Quality Assurance

### Test Coverage

- **Unit tests**: Write comprehensive unit tests for all public functions
- **Integration tests**: Test component interactions and external dependencies
- **Edge case testing**: Test boundary conditions and error scenarios
- **Performance tests**: Include performance benchmarks for critical paths
- **Security tests**: Test for common security vulnerabilities

### Test Quality

- **Test independence**: Tests should be independent and not rely on execution order
- **Test data**: Use realistic test data and avoid hardcoded test values
- **Mocking**: Use mocks for external dependencies and slow operations
- **Test naming**: Use descriptive test names that explain what is being tested
- **Test maintenance**: Keep tests updated as code evolves

## Code Generation Specifics

### Language Agnostic Principles

- **Standard libraries**: Prefer standard library functions over custom implementations
- **Design patterns**: Use appropriate design patterns (but avoid over-engineering)
- **Configuration**: Make code configurable through external configuration files
- **Logging**: Include appropriate logging at different levels (debug, info, warn, error)
- **Monitoring**: Include hooks for monitoring and metrics collection

### Dependencies and Libraries

- **Dependency management**: Use official package managers and lock file versions
- **Library selection**: Choose well-maintained, widely-used libraries
- **License compliance**: Ensure all dependencies have compatible licenses
- **Security updates**: Use recent versions and monitor for security updates
- **Minimal dependencies**: Only include necessary dependencies

## Code Review and Maintenance

### Review Checklist

- **Functionality**: Code works as intended and meets requirements
- **Performance**: No obvious performance bottlenecks or inefficiencies
- **Security**: No security vulnerabilities or data exposure risks
- **Maintainability**: Code is readable, well-structured, and documented
- **Testing**: Adequate test coverage and quality

### Long-term Maintenance

- **Documentation**: Maintain up-to-date documentation and README files
- **Deprecation**: Handle deprecated features gracefully with migration paths
- **Backwards compatibility**: Consider backwards compatibility when making changes
- **Refactoring**: Regular refactoring to improve code quality and structure
- **Technical debt**: Track and address technical debt systematically

## Compliance and Standards

### Code Standards

- **Style guides**: Follow established style guides for the target language
- **Linting**: Use automated linting tools to enforce code standards
- **Formatting**: Use consistent formatting and automated formatters
- **Code analysis**: Use static analysis tools to catch potential issues
- **Documentation standards**: Follow documentation standards for the project

### Legal and Ethical

- **Copyright**: Respect copyright and licensing requirements
- **Privacy**: Follow privacy regulations and data protection laws
- **Accessibility**: Consider accessibility requirements for user-facing code
- **Ethical AI**: Follow ethical guidelines for AI and machine learning code
- **Open source**: Follow open source best practices when applicable
