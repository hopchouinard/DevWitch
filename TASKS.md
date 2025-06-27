# DevWitch Project – Task List

This document outlines all required tasks to fully implement the DevWitch configuration toolbox for Visual Studio Code. Each task includes a description and any dependencies to ensure smooth execution by any developer, regardless of access to prior discussions.

## 1. Project Initialization

* **Create the repository** named `DevWitch`, set to private.
* \*\*Add a root \*\*\`\` file with the following entries to ignore common clutter and unnecessary files:

```plaintext
# macOS
.DS_Store
.AppleDouble
.LSOverride

# VS Code settings
.vscode/
!.vscode/extensions.json
!.vscode/launch.json
!.vscode/settings.schema.json

# Node
node_modules/
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Python
__pycache__/
*.py[cod]
*.pyo
*.pyd

# Jupyter
.ipynb_checkpoints

# Build
build/
dist/
*.egg-info/

# Environment variables
.env
.env.*

# Coverage reports
coverage/
*.cover
*.coverage

# Logs
*.log

# OS generated
Thumbs.db
desktop.ini
$RECYCLE.BIN/

# Others
*.swp
*.swo
*.bak
*.tmp
```

Ensure this file is placed at the root of the repository so it applies universally.

* \*\*Initialize with a \*\*\`\` referencing this task document and the main project spec.

## 2. Core Configuration Setup

* **Create ******\`\`****** at the root** containing global configuration settings for themes, fonts, extensions, Copilot, and Git integration. This file should be complete, commented, and categorized for clarity.
* \*\*Create \*\*\`\` to document transversal VS Code extensions typically used in all environments. To generate this list based on your currently installed extensions in VS Code, open a terminal and run:

```plaintext
# Generate a list of globally installed VS Code extensions
code --list-extensions > global-extensions.md
```

This will output a plain-text list of extension identifiers. You can then review and optionally format it as a markdown list or JSON array for consistency and clarity.

## 3. Global GitHub Settings

These instructions help standardize AI-assisted coding output and support maintainable codebases.

**Create ********`.github/`******** directory** in the root of the repo.

* **Add specialized Copilot instruction files** to guide different phases of AI assistance. Each file must follow Markdown syntax and contain clear behavioral rules:

  * **`copilot-codeGeneration-instructions.md`**:
    Define coding style, file organization rules, formatting preferences, error handling best practices, and preferred libraries/frameworks. Include examples of well-structured code and specify architectural patterns to follow (e.g., MVC, microservices).

  * **`copilot-commit-message-instructions.md`**:
    Detail how to write commit messages using a consistent style guide such as Conventional Commits. Include examples of good messages and describe what to avoid (e.g., "fix stuff").

  * **`copilot-review-instructions.md`**:
    Guide how Copilot should perform code review. Include goals such as identifying missing error handling, redundant code, lack of tests, and adherence to coding conventions. Specify tone (e.g., constructive, concise).

  * **`copilot-pull-request-description-instructions.md`**:
    Define structure and tone for PR descriptions. Include checklists (e.g., "What does this PR do?", "Related issues?", "How to test?"). Indicate expected documentation and changelog update behavior.

  * **`copilot-test-instructions.md`**:
    Provide guidance for writing unit tests, integration tests, and test coverage expectations. Specify frameworks to use (e.g., Pytest, Mocha), mocking libraries, naming conventions, and test folder structure.

These modular instruction files allow fine-grained control over GitHub Copilot's behavior across the software lifecycle and help ensure consistency across all projects.

* \*\*Create \*\***`.github/prompts/`** and populate with shared `.prompt.md` templates. Each prompt must include:

  * YAML front matter (mode, tools, description)
  * Clear, concise instruction content

### Recommended General Prompt Templates

Include the following `.prompt.md` files in `.github/prompts/` as they are useful across all project types:

* **`generate-function.prompt.md`**: Generate a function based on a one-line description, with optional input/output type hints.
* **`generate-tests.prompt.md`**: Create unit tests for a file or function using the preferred testing framework (e.g., Pytest, Mocha).
* **`write-docstring.prompt.md`**: Produce a comprehensive docstring for a selected function or class, following the project’s documentation style.
* **`refactor-code.prompt.md`**: Improve performance, readability, and modularity of a given code block or file.
* **`summarize-code.prompt.md`**: Generate a high-level summary of what a code file does, including its inputs, outputs, and side effects.

Each file should contain a structured YAML front matter with `mode`, `tools`, and `description` fields, followed by concise and effective prompt content.

## 4. Scenario Templates

Create subfolders for each development scenario. For each scenario, do the following:

### Example: `python-project/`

* **Create ********`.vscode/`******** folder**:

  * Add `extensions.json` with scenario-specific recommendations.
  * Add `mcp.json` if project uses MCP agents.
* **Create ********`.github/`******** folder**:

  * Add the following files:
  * **`copilot-codeGeneration-instructions.md`**: Describe the expected code style and structure for Python code, including use of type hints, naming conventions (snake\_case), preferred libraries (e.g., requests, pandas), and expected documentation style for functions and classes.
  * **`copilot-test-instructions.md`**: Define testing strategy using Pytest, naming conventions for test files (e.g., `test_*.py`), test coverage goals, and rules for mocking or fixtures. Include examples of standard test formats.
  * Add `prompts/` with Python-specific `.prompt.md` files.

Repeat this setup for:

* `ai-project/`
* `js-project/`

## 5. Documentation

* \*\*Write a comprehensive \*\***`README.md`** with:

  * Overview of DevWitch
  * Folder structure explanation
  * Usage instructions (how to use a scenario folder)
  * Contribution guidelines
* **Include this task list** as a `TASKS.md` or `devwitch-roadmap.md` for clarity.

## 6. Prompt and Instruction File Validation

* Confirm `.prompt.md` and `.instructions.md` files follow the expected structure:

  * Correct suffix
  * Valid YAML front matter
  * Compatible locations: `.github/prompts/`, `.github/`, etc.

## 7. Optional Enhancements

* **Add ********`.devcontainer/`******** support** in relevant scenarios.
* **Create ********`snippets/`******** directory** for reusable code fragments.
* \*\*Implement a \*\***`merge-config.ps1`** or shell script to assist with merging `settings.json` and MCP values.

## 8. Final Testing

* Open each scenario in VS Code.

  * Confirm extensions are recommended properly.
  * Ensure prompts are accessible via command palette.
  * Validate Copilot behavior reflects `.instructions.md` guidance.

## 9. Versioning and Updates

* Tag initial release as `v0.1.0`
* Add changelog entries as improvements are made.
* Encourage use of branches or forks for proposing new configurations.

---

This document is the blueprint to create DevWitch as a modular, maintainable, and powerful VS Code configuration library. Follow it step-by-step to unleash its full potential.
