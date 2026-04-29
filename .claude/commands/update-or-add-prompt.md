---
name: update-or-add-prompt
description: Workflow command scaffold for update-or-add-prompt in awesome-chatgpt-prompts.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-or-add-prompt

Use this workflow when working on **update-or-add-prompt** in `awesome-chatgpt-prompts`.

## Goal

Add a new prompt or update an existing prompt in the prompts.csv file.

## Common Files

- `prompts.csv`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or append a row in prompts.csv with the new or updated prompt.
- Commit the change with a message indicating the prompt added or updated.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.