# Gemini Code Assistant Guidance for the DevWitch Project

This document provides instructions for Gemini and other code assistants on how to interact with the DevWitch repository. Adhering to these guidelines is crucial for maintaining the project's modular structure, consistency, and overall vision.

## 1. Project Overview

DevWitch is not a typical software project with source code to be compiled or run. Instead, it is a **modular configuration library** for Visual Studio Code and AI-powered development tools like GitHub Copilot and Gemini. Its primary purpose is to provide a centralized, version-controlled repository of reusable environment scaffolds for various development scenarios (e.g., Python, JavaScript, AI).

The core philosophy is **modularity and reusability**. Developers using DevWitch are expected to copy specific scenario folders (e.g., `python-project/`) into their own projects to bootstrap a consistent and intelligent development environment.

## 2. Core Principles for AI Interaction

When assisting with tasks in this repository, always adhere to the following principles:

*   **Respect the Modular Structure:** Never add project-specific logic or code directly to the root. All configurations must be placed within the appropriate scenario folder (e.g., `python-project`, `ai-project`). Global settings in the root `settings.json` should be transversal and applicable to all scenarios.
*   **Follow Existing Conventions:** Before adding or modifying any file, analyze the existing structure and style. New prompts, instruction files, and VS Code settings must match the established format.
*   **Prioritize Reusability:** Any new configuration or prompt should be designed to be as reusable and generic as possible within its context. Avoid hardcoding project-specific paths or values.
*   **Explain Changes Clearly:** When modifying any configuration, provide a clear and concise explanation of the change and its purpose. This is especially important for changes to global files like `settings.json`.
*   **Do Not Introduce Build Steps:** This project does not have a build process. Do not add any tools or scripts that require compilation or bundling.

## 3. Key Files and Their Purpose

Your interactions will primarily involve the following files and directories. Understand their purpose before making any changes.

### Global Configurations (Root Level)

*   **`settings.json`**: Contains **global** VS Code settings. Only add settings here that are universally applicable across all development scenarios.
*   **`.github/`**:
    *   **`copilot-*-instructions.md`**: These files provide instructions to GitHub Copilot for various tasks (e.g., code generation, commit messages). When modifying these, ensure the instructions are generic and align with best practices.
    *   **`prompts/`**: This directory contains globally applicable prompt templates (`.prompt.md`). Prompts here should be useful for any type of project.

### Scenario-Specific Configurations (e.g., `python-project/`)

*   **`[scenario-name]/`**: Each of these folders represents a self-contained development environment.
    *   **`.vscode/extensions.json`**: A list of recommended VS Code extensions for that specific scenario.
    *   **`.github/copilot-*-instructions.md`**: Copilot instructions tailored to the specific language or framework of the scenario.
    *   **`.github/prompts/`**: Prompt templates specific to the scenario.

## 4. How to Handle Common Requests

### Adding a New Scenario

1.  Create a new directory with a descriptive name (e.g., `go-project/`).
2.  Inside the new directory, create the standard subdirectories: `.vscode/` and `.github/prompts/`.
3.  Add an `extensions.json` file to `.vscode/` with a list of recommended extensions for the new scenario.
4.  Add scenario-specific `copilot-*-instructions.md` and `.prompt.md` files as needed.

### Adding a New Prompt

1.  Determine if the prompt is **global** or **scenario-specific**.
2.  Place global prompts in the root `.github/prompts/` directory.
3.  Place scenario-specific prompts in the appropriate `[scenario-name]/.github/prompts/` directory.
4.  Ensure the prompt file follows the correct format:
    *   Ends with `.prompt.md`.
    *   Includes YAML front matter with `mode`, `tools`, and `description`.

### Modifying VS Code Settings

1.  Determine if the setting is **global** or **scenario-specific**.
2.  For global settings, add them to the root `settings.json` with a comment explaining their purpose.
3.  For scenario-specific settings, add them to a `settings.json` file within the appropriate `[scenario-name]/.vscode/` directory.

## 5. Final Reminders

*   **Always verify file paths.** Ensure you are editing the correct file, especially when dealing with nested configurations.
*   **Do not treat this as a monolithic project.** Think of it as a collection of independent modules.
*   **When in doubt, ask for clarification.** If you are unsure where a particular configuration should go, ask the user for more information about their intent.

By following these guidelines, you will help maintain the integrity and usability of the DevWitch project.
