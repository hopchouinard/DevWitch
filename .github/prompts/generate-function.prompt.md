---
mode: "agent"
tools: ['context7']
description: "Generate a function based on a one-line description with optional input/output type hints"
---

# Generate Function

Create a function based on the provided description. Follow these guidelines:

## Requirements

- Use appropriate naming conventions for the target language
- Include proper type hints where applicable
- Add comprehensive error handling
- Follow the project's coding style and conventions
- Include inline comments for complex logic

## Input Format

Provide a one-line description of what the function should do, optionally followed by:

- Input parameter types and names
- Expected return type
- Any specific constraints or requirements

## Output Format

Generate:

1. The function signature with proper type hints
2. Complete implementation with error handling
3. Brief docstring explaining purpose, parameters, and return value
4. Example usage if helpful

## Example

**Input:** "Calculate the area of a circle given its radius"
**Additional info:** radius: float, returns: float

The function should validate input and handle edge cases appropriately.
