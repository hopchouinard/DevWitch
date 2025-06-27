# DevWitch Project Specification

## Overview

DevWitch is a modular configuration library for Visual Studio Code, designed as a developer's toolbox to enable rapid project setup and environment consistency. Rather than being a template repository to clone, DevWitch serves as a curated archive of reusable environment scaffolds tailored to different types of development scenarios (e.g., Python, AI, JavaScript). The user selectively copies elements into their working projects.

## Objectives

* Maintain a central repository of reusable, scenario-specific VS Code configurations.
* Streamline project setup with preconfigured `.vscode`, `.github`, `mcp.json`, and prompt templates.
* Eliminate configuration duplication and allow clear separation of concerns.
* Empower developers with prompt-driven interactions and Copilot behavior customization.

## Top-Level Structure

```plaintext
DevWitch/
├── settings.json                   # Global VS Code settings
├── global-extensions.md           # Optional list of transversal extensions
├── .github/
│   ├── copilot-instructions.md    # Global instructions for GitHub Copilot
│   └── prompts/                   # Shared prompt templates for all scenarios
├── [scenario-folders]/            # E.g. python-project/, ai-project/, etc.
│   └── .vscode/
│       ├── extensions.json        # Scenario-specific recommended extensions
│       └── mcp.json               # MCP configuration for that scenario
│   └── .github/
│       ├── copilot-instructions.md
│       └── prompts/               # Scenario-specific prompts
└── README.md                      # Project documentation and usage guide
```

## Configuration Files

### settings.json

Centralized VS Code configuration shared across all workspaces. Includes themes, editor preferences, terminal setup, Git behavior, Copilot settings, and spell checker dictionaries.

### .vscode/

Contains per-scenario configuration:

* `extensions.json`: VS Code will recommend installing these extensions.
* `mcp.json`: Defines Model Context Protocol server endpoints and settings.

### .github/

Holds project instruction files and prompt templates:

* `copilot-instructions.md`: Project-level behavioral configuration for GitHub Copilot.
* `prompts/*.prompt.md`: Structured markdown files with YAML front matter for use in chat-based prompt commands.

## Prompt Structure (.prompt.md)

* Stored in `.github/prompts/`
* File suffix: `.prompt.md`
* Supports front matter metadata:

```md
---
mode: "edit"
tools: ["codebase"]
description: "Generate unit tests"
---
Prompt content here...
```

## Instruction Files (.instructions.md)

* Stored in `.github/` or `.github/instructions/`
* File names must end in `.instructions.md` or be named `copilot-instructions.md`
* YAML front matter can define scope using `applyTo`

## Usage

* Copy scenario folder(s) into your new project.
* VS Code will suggest extensions.
* Prompts and instructions will be automatically picked up.

## Contributing

* Add new prompt templates to the appropriate scenario folder.
* Update `settings.json` with transversal changes only.
* Maintain descriptive comments and categorization for all JSON files.

## Future Enhancements

* Add starter `.devcontainer` files.
* Include project-specific `snippets/` directories.
* Build a simple merge script for combining `settings.json` and MCP configs.

---

**DevWitch** is for developers who love control, clarity, and a touch of configuration sorcery.
