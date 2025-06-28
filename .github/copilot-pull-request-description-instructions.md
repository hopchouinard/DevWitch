# Pull Request Description Instructions

## Standard Template

Use this structure for all pull request descriptions:

```markdown
## Summary
Brief description of what this PR accomplishes.

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Code refactoring
- [ ] Test improvements
- [ ] Build/CI improvements

## Changes Made
- Detailed list of changes
- Each change on a separate bullet point
- Include technical details when relevant

## Testing
- [ ] Tests pass locally
- [ ] New tests added for new functionality
- [ ] Manual testing performed
- [ ] Edge cases considered and tested

## Related Issues
- Fixes #123
- Relates to #456
- Closes #789

## Screenshots/Videos (if applicable)
Before/after screenshots or demo videos for UI changes.

## Additional Notes
Any additional context, concerns, or considerations for reviewers.
```

## Writing Guidelines

### Summary Section

- **Length**: 1-3 sentences maximum
- **Clarity**: Explain the main purpose and impact
- **Audience**: Write for someone unfamiliar with the context
- **Value**: Focus on user or business value, not just technical changes

### Changes Made Section

- **Specificity**: Be specific about what was modified
- **Organization**: Group related changes together
- **Technical details**: Include important implementation details
- **Breaking changes**: Clearly highlight any breaking changes

### Testing Section

- **Completeness**: Document all testing performed
- **Coverage**: Mention test coverage impact
- **Manual testing**: Describe manual testing scenarios
- **Performance**: Include performance impact if applicable

## Quality Checklist

Before submitting, ensure your PR description:

- [ ] Clearly explains the problem being solved
- [ ] Documents all significant changes
- [ ] Includes testing information
- [ ] References related issues
- [ ] Uses proper grammar and spelling
- [ ] Follows the standard template
- [ ] Provides sufficient context for reviewers

## Examples

### Feature Addition Example

```markdown
## Summary
Add user authentication with OAuth2 integration to support Google and GitHub login providers.

## Type of Change
- [x] New feature (non-breaking change which adds functionality)

## Changes Made
- Implemented OAuth2 service with Google and GitHub providers
- Added user session management with JWT tokens
- Created login/logout UI components
- Updated user model to include OAuth provider information
- Added middleware for protected routes

## Testing
- [x] Tests pass locally
- [x] New tests added for OAuth service and middleware
- [x] Manual testing performed with both providers
- [x] Edge cases tested (network failures, invalid tokens)

## Related Issues
- Fixes #142
- Relates to #89

## Screenshots
[Login screen with new OAuth buttons]

## Additional Notes
OAuth credentials need to be configured in production environment.
```

### Bug Fix Example

```markdown
## Summary
Fix memory leak in data processing pipeline that caused application crashes under high load.

## Type of Change
- [x] Bug fix (non-breaking change which fixes an issue)

## Changes Made
- Fixed memory leak in DataProcessor by properly disposing streams
- Added connection pooling for database operations
- Implemented proper error handling and cleanup in async operations
- Updated logging to track memory usage

## Testing
- [x] Tests pass locally
- [x] Added memory usage tests
- [x] Load testing performed - no crashes after 1000+ operations
- [x] Verified fix with memory profiler

## Related Issues
- Fixes #234
- Closes #567

## Additional Notes
Performance improvement of approximately 40% in high-load scenarios.
```

## Best Practices

### Do's

- ✅ Use clear, descriptive titles
- ✅ Explain the "why" behind changes
- ✅ Include visual aids for UI changes
- ✅ Reference related documentation
- ✅ Tag relevant reviewers
- ✅ Update the description if scope changes

### Don'ts

- ❌ Leave sections empty without explanation
- ❌ Use vague descriptions like "fixed stuff"
- ❌ Submit without testing information
- ❌ Forget to reference related issues
- ❌ Include sensitive information (passwords, keys)
- ❌ Make the description too technical or too simple

## Review Preparation

Help reviewers by:

- **Context**: Provide sufficient background information
- **Guidance**: Point out areas that need special attention
- **Questions**: Ask specific questions if unsure about approach
- **Dependencies**: Mention any external dependencies or requirements
- **Deployment**: Include deployment considerations or instructions

## Breaking Changes

For breaking changes, always include:

- **Migration guide**: How to update existing code
- **Deprecation timeline**: When old functionality will be removed
- **Backward compatibility**: What remains compatible
- **Impact assessment**: Who and what will be affected

## Tools Integration

Consider using:

- **Templates**: GitHub PR templates for consistency
- **Automation**: Link to CI/CD build results
- **Metrics**: Include performance metrics if relevant
- **Documentation**: Link to updated documentation
