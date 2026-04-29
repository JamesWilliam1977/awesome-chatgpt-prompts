```markdown
# awesome-chatgpt-prompts Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill covers the core development patterns, coding conventions, and collaborative workflows for contributing to the `awesome-chatgpt-prompts` repository. The project is a Next.js application written in TypeScript, featuring prompt management, internationalization (i18n), and community-driven contributions. The repository emphasizes clear commit conventions, modular code organization, and streamlined processes for updating prompts, translations, and contribution guidelines.

---

## Coding Conventions

### File Naming

- Use **camelCase** for file names.
  - Example: `infinitePromptList.tsx`, `mcpConfigTabs.tsx`

### Import Style

- Use **alias imports** for modules.
  - Example:
    ```typescript
    import { PromptList } from '@/components/prompts/infinitePromptList'
    ```

### Export Style

- Use **named exports**.
  - Example:
    ```typescript
    export function PromptList(props: Props) { ... }
    ```

### Commit Message Patterns

- Prefixes: `feat`, `chore`, `fix`, `refactor`
- Messages are concise (~44 characters on average).
  - Example: `feat: add new prompt for SQL generation`

---

## Workflows

### Update or Add Prompt

**Trigger:** When you want to add a new prompt or update an existing prompt in the `prompts.csv` file.  
**Command:** `/add-prompt`

1. Open `prompts.csv`.
2. Add a new row for your prompt, or update the content of an existing row.
3. Save your changes.
4. Commit with a message indicating the prompt added or updated.
   - Example: `feat: add prompt for creative writing`
5. Submit your pull request.

---

### Update Multiple i18n Language Files

**Trigger:** When you need to add or update translations for new features, prompts, or UI elements.  
**Command:** `/update-i18n`

1. Edit the relevant language JSON files in the `messages/` directory:
    - `ar.json`, `de.json`, `el.json`, `en.json`, `es.json`, `fr.json`, `he.json`, `it.json`, `ja.json`, `ko.json`, `pt.json`, `ru.json`, `tr.json`, `zh.json`
2. Optionally, update related UI or feature files to use the new translations.
3. Commit all changes together.
   - Example: `fix: update i18n for new prompt categories`
4. Submit your pull request.

---

### Update Contributing or Issue Templates

**Trigger:** When you want to clarify, update, or add contribution instructions or issue reporting templates.  
**Command:** `/update-contributing`

1. Edit `CONTRIBUTING.md` and/or files in `.github/ISSUE_TEMPLATE/`:
    - `config.yml`, `new_prompt.yml`
2. Commit the changes together.
   - Example: `chore: update contributing guidelines`
3. Submit your pull request.

---

### Feature or Refactor Multiple Related Components

**Trigger:** When you want to implement a new feature or refactor logic across several files/components.  
**Command:** `/feature-refactor`

1. Edit or create the relevant files, such as:
    - `src/app/[username]/page.tsx`
    - `src/app/categories/[slug]/page.tsx`
    - `src/app/prompts/page.tsx`
    - `src/app/tags/[slug]/page.tsx`
    - `src/app/api/user/notifications/route.ts`
    - `src/app/api/leaderboard/route.ts`
    - `src/components/mcp/mcp-config-tabs.tsx`
    - `src/components/mcp/mcp-server-popup.tsx`
    - `src/components/prompts/infinite-prompt-list.tsx`
    - `src/components/prompts/private-prompts-note.tsx`
2. Update logic, UI, or data fetching as needed.
3. Commit all related changes together.
   - Example: `refactor: unify prompt list pagination`
4. Submit your pull request.

---

## Testing Patterns

- **Framework:** [vitest](https://vitest.dev/)
- **Test File Pattern:** Files end with `.test.ts`
  - Example: `promptUtils.test.ts`
- **Test Example:**
    ```typescript
    import { describe, it, expect } from 'vitest'
    import { getPromptById } from '@/utils/promptUtils'

    describe('getPromptById', () => {
      it('returns the correct prompt', () => {
        const prompt = getPromptById('123')
        expect(prompt).toBeDefined()
      })
    })
    ```

---

## Commands

| Command           | Purpose                                                      |
|-------------------|--------------------------------------------------------------|
| /add-prompt       | Add or update a prompt in `prompts.csv`                      |
| /update-i18n      | Add or update translations in multiple language files         |
| /update-contributing | Update contribution guidelines or issue templates          |
| /feature-refactor | Implement or refactor a feature across multiple components   |
```
