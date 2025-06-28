# Commit Message Instructions

## Standard Format

Use the **Conventional Commits** format for all commit messages:

```plaintext
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

## Commit Types

### Primary Types

- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation only changes
- **style**: Formatting changes (spaces, commas, etc.)
- **refactor**: Refactoring without adding features or fixing bugs
- **test**: Adding or modifying tests
- **chore**: Maintenance tasks (build, tools, dependencies)

### Specialized Types

- **perf**: Performance improvements
- **ci**: Changes to CI/CD configuration
- **build**: Changes affecting the build system
- **revert**: Reverting a previous commit

## Writing Rules

### Description (line 1)

- **Maximum length**: 50 characters
- **Tense**: Imperative present ("add", not "added" or "adds")
- **Capitalization**: First letter lowercase
- **Punctuation**: No ending period
- **Language**: English preferred

### Body (optional)

- **Separation**: Blank line after description
- **Line length**: Maximum 72 characters
- **Content**: Explain the "why" and "how"
- **Format**: Use bullet points if necessary

### Footer (optional)

- **Breaking changes**: `BREAKING CHANGE: description`
- **Issues**: `Fixes #123`, `Closes #456`
- **Co-authors**: `Co-authored-by: Name <email>`

## Correct Examples

```plaintext
feat(auth): add OAuth2 integration

- Implement Google and GitHub providers
- Add user session management
- Update login UI components

Fixes #142
```

```plaintext
fix(api): resolve timeout in user endpoint

The user fetch operation was timing out due to missing
async/await in the database query. Added proper error
handling and increased timeout threshold.

Closes #89
```

```plaintext
docs: update installation guide

Add Docker setup instructions and troubleshooting section
```

```plaintext
refactor(utils): simplify date formatting functions

- Consolidate multiple date utilities into single module
- Remove deprecated moment.js dependency
- Maintain backward compatibility

BREAKING CHANGE: DateUtils.format() now requires ISO string input
```

## Incorrect Examples

❌ `Fixed stuff` - Too vague  
❌ `feat: Added new feature for users to login with social media` - Too long  
❌ `Update documentation.` - Unnecessary period  
❌ `WIP: working on login` - Avoid temporary commits

## Scope Guidelines

### Recommended Scopes

- **Components**: `auth`, `ui`, `api`, `config`
- **Features**: `login`, `dashboard`, `reports`
- **Tools**: `build`, `test`, `deploy`
- **Files**: `readme`, `package`, `tsconfig`

### Scope Rules

- Use short and descriptive names
- Be consistent within the project
- Omit if too generic or obvious

## Special Commits

### Merge Commits

```plaintext
Merge branch 'feature/oauth' into main

feat(auth): add OAuth2 integration
```

### Revert Commits

```plaintext
revert: feat(auth): add OAuth2 integration

This reverts commit 1234567 due to security concerns.
```

### Release Commits

```plaintext
chore(release): bump version to 2.1.0

- New OAuth2 integration
- Performance improvements
- Bug fixes in user management
```

## Pre-Commit Checklist

Before committing, verify:

- [ ] Message follows Conventional Commits format
- [ ] Description is clear and concise
- [ ] Type matches the changes made
- [ ] Breaking changes are documented
- [ ] Related issues are referenced
- [ ] Commit is atomic (single responsibility)

## Recommended Tools

- **Commitizen**: Interactive guide for messages
- **Conventional Changelog**: Automatic changelog generation
- **Husky + commitlint**: Automatic message validation
