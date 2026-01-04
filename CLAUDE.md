# THE CORTEX - GLOBAL SYSTEM INSTRUCTIONS

> This is a Second Brain / PKM system. Claude assists with context management, task tracking, and maintaining project continuity.

## 1. Voice & Tone (CRITICAL)

Before writing any emails, documentation, or messages, you MUST read:
`~/The_Cortex/02_Knowledge_Vault/user_voice.md`
Adopt this persona. Do not sound like a generic AI.

## 2. The "Context First" Rule

You are working inside a "Second Brain" system designed to reduce cognitive load.

- **Read First:** Before answering questions, check if a `context.md` exists in the current folder.
- **Write Back:** If we make a decision or finish a task, you MUST update the `todo.md` or `context.md` file immediately. Do not wait for instructions to do so.

## 3. Project Files: `context.md` and `todo.md` (REQUIRED)

These two files are the system of record for each project folder.

### `context.md` (state + decisions)

Use `context.md` to store the durable narrative of the project: goals, constraints, decisions, current state, and key links.

Minimum structure:

- `## Project Context` (1–5 paragraphs)
- `## Goals` (bullets; include success criteria)
- `## Current State` (what’s done, what’s next, blockers)
- `## Decisions` (append-only; date-stamp entries)
- `## References` (links, docs, tickets)

If `context.md` doesn’t exist (or is missing sections), create it / add the missing sections using the structure above.

### `todo.md` (next actions)

Use `todo.md` for actionable work only. Keep the top of the file focused on the next 3–10 concrete tasks.

Minimum structure:

- `## Now` (the next actions)
- `## Next` (queued but not immediate)
- `## Backlog` (nice-to-haves)

Tasks must be checkboxes (`- [ ]` / `- [x]`) and phrased as actions.

If `todo.md` doesn’t exist (or is missing sections), create it / add the missing sections using the structure above.

### Update Protocol (how you change them)

- At the end of any work session, update `todo.md` first (mark done items, add next actions), then update `context.md` (state + decisions).
- Do not rewrite history: append to `## Decisions` and keep changes incremental.
- If you discover new scope/constraints, capture them in `context.md` immediately.

### Source of Truth

- **`context.md` is authoritative.** If `todo.md` and `context.md` conflict, `context.md` wins.
- Tasks in `todo.md` are derived from goals, state, and decisions documented in `context.md`.

## 4. Preferred Tools & Processes

We follow specific methodologies depending on the role. Align your outputs with the defaults found in:
`~/The_Cortex/02_Knowledge_Vault/preferred_tools.md`

_Examples of standards to look for:_

- **Leadership/Ops:** Lean Six Sigma, SWOT Analysis, OKRs.
- **Product:** Agile User Stories, PRDs.
- **Devs:** Tech Stack (Python/SvelteKit), Testing Frameworks.

## 5. Do NOT

- Create new folders without checking the existing structure first
- Delete or overwrite entries in the `## Decisions` section of `context.md`
- Rewrite the history in `context.md`—always append incrementally
- Ignore conflicts between files—always defer to `context.md` as the source of truth

## 6. Company Policy & Safety (Optional but recommended)

You are responsible for following your organization’s policies. This section is a starter template—replace placeholders with your official internal policy links and requirements.

Before working with any sensitive/customer/internal data, read and follow:
`~/The_Cortex/02_Knowledge_Vault/policies.md`
