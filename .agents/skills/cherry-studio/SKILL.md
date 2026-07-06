```markdown
# cherry-studio Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill introduces the core development patterns and conventions used in the `cherry-studio` repository. The codebase is built with TypeScript and React, following consistent file naming, import/export styles, and commit message conventions. It also outlines how to structure tests and provides suggested commands for frequent workflows.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `userProfile.tsx`, `appHeader.ts`

### Import Style
- Use **relative imports** for referencing modules.
  - Example:
    ```typescript
    import { UserProfile } from './userProfile';
    ```

### Export Style
- Prefer **named exports**.
  - Example:
    ```typescript
    // userProfile.tsx
    export const UserProfile = () => { /* ... */ };
    ```

### Commit Messages
- Use **conventional commit** format.
- Common prefix: `ci`
- Example:
  ```
  ci: update build pipeline to support new environment variables
  ```

## Workflows

### Commit Code
**Trigger:** When making any code changes that need to be committed.
**Command:** `/commit`

1. Stage your changes:
   ```
   git add .
   ```
2. Write a conventional commit message, e.g.:
   ```
   git commit -m "ci: update build pipeline to support new environment variables"
   ```
3. Push your changes:
   ```
   git push
   ```

## Testing Patterns

- Test files use the pattern: `*.test.*`
  - Example: `userProfile.test.tsx`
- Testing framework is not specified; follow the established file naming for tests.
- Place test files alongside the code they test or in a dedicated `__tests__` directory.

Example test file:
```typescript
// userProfile.test.tsx
import { render } from '@testing-library/react';
import { UserProfile } from './userProfile';

test('renders user profile', () => {
  render(<UserProfile />);
  // Add assertions here
});
```

## Commands
| Command   | Purpose                                   |
|-----------|-------------------------------------------|
| /commit   | Guide for committing code changes         |
```
