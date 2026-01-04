# 🧠 The Cortex

_A Second Brain for High-Performance Technical Leaders_

The Cortex system is a "Second Brain" designed to keep track of your work and provide persistent context for your AI. By offloading memory to the system, you free yourself up for creative thinking and high-level strategy.

You no longer need to remember where you left off or context-switch painfully between tasks. Your AI—powered by the `CLAUDE.md` rules—manages that cognitive load for you.

**Who is this for?**
This is primarily designed for **Technical Business Roles** (Management, Product Managers, Project Managers, Program Managers, etc.).

_Note for Developers: You will also find this system potentially useful, especially by adapting the tools section to your specific stack and workflow._

---

## 🚀 Getting Started

### 1. Installation

1.  **Get The Cortex on your machine:**

    - **Option A (no git required):** Copy/unzip this folder to `~/The_Cortex`
    - **Option B (with git):** Clone from wherever your team hosts it:
      ```bash
      cd ~
      git clone [repo-url] The_Cortex
      cd The_Cortex
      ```

2.  **Install Claude Code:**

    ```bash
    npm install -g @anthropic-ai/claude-code
    ```

    _Important: When logging in, ensure you use your **WORK EMAIL**, not your personal email._

3.  **The Voice Setup (IMPORTANT):**

    This step customizes Claude to write in YOUR voice, not generic AI-speak.

    **Option A: Analyze your existing writing**

    - Place 3–5 examples of your best writing (emails, strategy docs, memos) in `00_Inbox`.
    - Run `claude` from the repo root
    - Ask: _"Analyze the files in 00_Inbox and write a comprehensive style guide for me in 02_Knowledge_Vault/user_voice.md that captures my tone, vocabulary, and structure preferences."_

    **Option B: Use existing LLM history**

    - If you have an existing ChatGPT or Claude chat that knows your style, ask it to generate a `user_voice.md` file.
    - **Tip:** Paste the content of this repo's setup prompt into that chat so it understands the system context.
    - Copy the result into `02_Knowledge_Vault/user_voice.md`.

---

## 🔄 Daily Workflow

### Loading The Cortex Instructions

The Cortex system relies on the rules in `~/The_Cortex/CLAUDE.md` to work properly. Here are two ways to use it:

**Method 1: Simple Workflow (Recommended for Getting Started)**

At the start of each Claude session, paste this prompt:

```
Read ~/The_Cortex/CLAUDE.md and follow those instructions. Check this directory for context.md and todo.md.
```

**Method 2: Shell Alias (Advanced - One-Time Setup)**

For power users who want it automated, add this to your `~/.bashrc` or `~/.zshrc`:

```bash
alias cortex='claude --prompt "Read ~/The_Cortex/CLAUDE.md and follow those instructions. Check this directory for context.md and todo.md."'
```

Then just type `cortex` instead of `claude` and the instructions auto-load.

---

### Starting a New Project

1. `cd ~/The_Cortex` (or navigate to your Cortex root)
2. Run `claude` (or `cortex` if using the alias)
3. Paste the startup prompt (Method 1) or it loads automatically (Method 2)
4. Ask: _"Create a new project called Strategy_Q3 in 01_Active_Projects with context.md and todo.md files following the structure in CLAUDE.md"_

Claude will scaffold the folder and files for you.

### Resuming Work

1. `cd ~/The_Cortex/01_Active_Projects/Strategy_Q3`
2. Run `claude` (or `cortex`)
3. Paste the startup prompt (Method 1) or it loads automatically (Method 2)
4. Ask: _"Look at todo.md and context.md, where did we leave off?"_

## 📂 The Structure

- **00_Inbox:** The "Dump Zone" for quick ideas/URLs.
- **01_Active_Projects:** Where work happens (Research & Ideation live here).
- **02_Knowledge_Vault:** The Source of Truth (Voice, Tools, Processes).
- **03_Archive:** Cold Storage (Organized by Year).
- **04_Development:** A dedicated space for code repositories, scripts, and development labs.

### Git Strategy for `04_Development`

The Cortex repository itself is tracked by one git repository (the entire `The_Cortex` folder).

**For code projects in `04_Development`:**

- Each project can be its own separate git repository
- Add subdirectories to `.gitignore` if they're separate repos:
  ```
  # In your root .gitignore
  04_Development/my-app/
  04_Development/my-tool/
  ```
- Or keep them as regular folders if they're just scripts/experiments you want tracked in the main Cortex repo

**Example:**

```
The_Cortex/               (git repo #1 - your Cortex)
├── 04_Development/
│   ├── quick-scripts/    (tracked in Cortex repo)
│   └── my-app/          (separate git repo #2, ignored in Cortex)
```

---

## 🏗️ Distribution Options (Choose One)

### Option 1: Local-only (no git required)

**Use Case:** You want a simple folder you can use immediately without any source control tooling.

**Workflow:**

1. Copy/unzip the folder to `~/The_Cortex`
2. Follow the "Getting Started" section above

### Option 2: Local git (recommended for versioning)

**Use Case:** You want history/rollback, but don’t need or want any remote hosting.

**Workflow:**

1. In the repo root, run `git init`
2. Run `git add .`
3. Commit with message: "Initial commit: The Cortex Starter Kit"

### Option 3: Team distribution (offline-friendly)

**Use Case:** Coworkers need a copy but may not have access to any external hosting.

**Workflow:**

- Share a `.zip` of the folder, or publish it on an internal shared drive / internal source control system per your org’s policy.
