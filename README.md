# DevWitch

DevWitch is a modular, reusable Visual Studio Code configuration toolbox built to help developers quickly bootstrap consistent and intelligent environments for a wide variety of project types including Python, AI, and JavaScript.

Rather than being cloned and used as a starting point like traditional templates, DevWitch acts as a curated **library**. You selectively copy the configuration pieces you need—from prompts to `.vscode/` settings—to empower your projects with pre-tuned workflows, extensions, Copilot instructions, and more.

---

## 📁 Repository Structure

```plaintext
DevWitch/
├── settings.json                   # Global VS Code settings applied across all projects
├── global-extensions.md           # List of recommended extensions for all environments
├── .github/
│   ├── copilot-codeGeneration-instructions.md
│   ├── copilot-commit-message-instructions.md
│   ├── copilot-review-instructions.md
│   ├── copilot-pull-request-description-instructions.md
│   ├── copilot-test-instructions.md
│   └── prompts/                   # Global prompt templates (reusable in all scenarios)
├── python-project/                # Scenario-specific setup
│   ├── .vscode/                   # Extensions and MCP config for Python
│   └── .github/                   # Scenario-specific Copilot behavior and prompts
│       └── prompts/
├── ai-project/                    # Similar to python-project but tailored for AI work
├── js-project/                    # JavaScript development configuration
└── README.md                      # This file
```

---

## 🚀 How to Use DevWitch

### Copying a Scenario Folder

1. Navigate to the scenario folder that fits your project (`python-project/`, `ai-project/`, etc.).
2. Copy the entire folder structure into your new project repo.
3. VS Code will automatically detect and offer to install extensions listed in `.vscode/extensions.json`.

### Required Files for Full Functionality

* **`.vscode/`**: For extensions, workspace settings, and MCP integration.
* **`.github/`**:

  * Copilot instruction files to guide AI-generated code.
  * `prompts/` folder containing `.prompt.md` templates for direct use in Copilot Chat.

### Prompt and Extension Activation

* **Prompt Templates**: Use commands like `Run Prompt` in Copilot Chat to invoke `.prompt.md` files.
* **Extension Suggestions**: VS Code will prompt you to install recommended extensions when you open a folder with `.vscode/extensions.json`.

---

## 🤝 Contributing to DevWitch

### Add or Update a Scenario

* Create a new folder following the structure of `python-project/`.
* Include `.vscode/`, `.github/`, and `prompts/` as necessary.
* Keep configurations modular and well-commented.

### Formatting and Validation

* **`.prompt.md` files**:

  * Must include front matter: `mode`, `tools`, and `description`
  * Must end with `.prompt.md`
* **`.instructions.md` files**:

  * Use Markdown syntax
  * Include clearly scoped behavioral instructions for Copilot

### Document Changes

* Update `settings.json` if you change or add transversal configurations.
* Log any new extensions in `global-extensions.md`.
* If your prompt is general-purpose, place it in the root `.github/prompts/` folder.

---

DevWitch is your config spellbook. Use it wisely, tweak it freely, and share the magic when it grows.
