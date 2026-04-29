---
name: update-multiple-i18n-language-files
description: Workflow command scaffold for update-multiple-i18n-language-files in awesome-chatgpt-prompts.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-multiple-i18n-language-files

Use this workflow when working on **update-multiple-i18n-language-files** in `awesome-chatgpt-prompts`.

## Goal

Add or update translations for multiple languages, often in response to new features or UI changes.

## Common Files

- `messages/ar.json`
- `messages/de.json`
- `messages/el.json`
- `messages/en.json`
- `messages/es.json`
- `messages/fr.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit multiple language JSON files in the messages/ directory.
- Optionally update related UI or feature files to use the new translations.
- Commit all changes together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.