---
name: handoff
description: Draft a complete Handoff.md transfer document for ending a work session. Use when the user wants a self-contained transfer note for another AI or human, especially to capture what the work is about, what is done, what is blocked, what comes next, and critical pitfalls.
---

# Handoff Writer

Use this skill to produce a single `Handoff.md` document that lets a fresh receiver continue the work without prior chat history.

## Workflow

### 1. Get the main name and save location first

If the user did not provide the main name or the save location, ask one short question first.

Use those values in the document title, context fields, and saved file path.

### 2. Reconstruct context before writing

Before drafting, gather the minimum concrete state:

- what the task or project is
- what files, outputs, or decisions already exist
- what is unfinished or blocked
- what the next operator should do first
- what mistakes would cause rework, regressions, or lost context

If facts are uncertain, mark them explicitly as `Unknown` or `Needs verification`.

### 3. Write exactly one handoff document

Write a finished `Handoff.md` using the structure in [references/Handoff.md](references/Handoff.md).

The document should explain, in plain language:

- what we are doing
- what has already been completed
- where progress is currently blocked or fragile
- what should happen next, in order
- what must not be changed, retried blindly, or misunderstood

### 4. Quality bar

- Be concrete about filenames, commands, environment facts, branches, URLs, credentials locations, or output artifacts when known.
- Prefer dated facts and explicit status over relative phrases like "just now" or "recently".
- Record decisions and rationale, not just actions.
- Separate facts from assumptions.
- Include warnings for irreversible actions, flaky workflows, hidden dependencies, and misleading dead ends.
- Keep the tone direct and utilitarian.

## Output rules

- Output the document content only, unless the user asks for commentary.
- The file name is `Handoff.md`.
- The save location must be explicit in the final output or header notes.
- Keep all required sections even if some are brief.
- If a section has no confirmed facts, write `Unknown` and say what should be checked.

## Resource

Read [references/Handoff.md](references/Handoff.md) before drafting so the section order and detail level stay consistent.
