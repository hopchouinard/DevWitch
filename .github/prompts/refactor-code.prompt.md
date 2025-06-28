---
mode: "agent"
tools: ['context7']
description: "Improve performance, readability, and modularity of a given code block or file"
---

# Refactor Code

Improve the selected code while maintaining its functionality. Follow these guidelines:

## Refactoring Goals

Focus on these improvements:

1. **Performance** - Optimize algorithms and reduce complexity
2. **Readability** - Make code clearer and more understandable
3. **Modularity** - Break down large functions, improve separation of concerns
4. **Maintainability** - Reduce code duplication, improve structure
5. **Best Practices** - Apply language-specific conventions and patterns

## Refactoring Rules

- Preserve existing functionality and behavior
- Maintain or improve test coverage
- Follow SOLID principles where applicable
- Use appropriate design patterns
- Eliminate code smells (long methods, duplicated code, etc.)
- Improve variable and function naming

## Output Format

Provide:

1. **Refactored code** with clear improvements
2. **Summary of changes** explaining what was improved and why
3. **Breaking changes** if any (should be minimal)
4. **Recommendations** for further improvements or testing

## Quality Checks

Ensure the refactored code:

- Compiles/runs without errors
- Maintains the same public interface when possible
- Improves at least one aspect (performance, readability, or structure)
- Follows the project's coding standards
- Includes updated documentation if needed
