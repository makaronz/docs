```markdown
# docs Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `docs` repository, a TypeScript codebase with a focus on documentation updates and clear, maintainable code. You will learn about file organization, import/export styles, commit message formatting, and testing patterns to ensure consistency and quality across contributions.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `myComponent.ts`, `userGuide.test.ts`

### Import Style
- Use **relative imports** for modules within the codebase.
  - Example:
    ```typescript
    import { getUser } from './userService';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // userService.ts
    export function getUser(id: string) { ... }
    ```

### Commit Messages
- Follow the **conventional commit** format.
- Use the `docs` prefix for documentation-related changes.
  - Example:
    ```
    docs: update API usage examples
    ```

## Workflows

### Documentation Update
**Trigger:** When making changes to documentation files or comments  
**Command:** `/update-docs`

1. Make your documentation changes in the relevant TypeScript files or markdown files.
2. Use a commit message starting with `docs:`, describing your change.
3. Push your changes to the repository.
4. Open a pull request if required.

### Code Contribution
**Trigger:** When adding or updating TypeScript source code  
**Command:** `/contribute-code`

1. Create or update files using camelCase naming.
2. Use relative imports and named exports as per conventions.
3. Write or update corresponding tests (see Testing Patterns).
4. Commit with a clear, conventional message (e.g., `docs: add new utility function`).
5. Push your changes and open a pull request.

### Testing
**Trigger:** When verifying code correctness  
**Command:** `/run-tests`

1. Write tests in files matching the `*.test.*` pattern.
2. Use the project's preferred (unspecified) testing framework.
3. Run tests locally to ensure all pass.
4. Address any failures before pushing.

## Testing Patterns

- Test files are named using the pattern `*.test.*` (e.g., `userService.test.ts`).
- The specific testing framework is not specified; follow project or team guidance.
- Place tests alongside the code they verify, using relative imports as needed.

  Example:
  ```typescript
  // userService.test.ts
  import { getUser } from './userService';

  describe('getUser', () => {
    it('returns user data for valid ID', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command           | Purpose                                      |
|-------------------|----------------------------------------------|
| /update-docs      | Start a documentation update workflow        |
| /contribute-code  | Begin a new code contribution workflow       |
| /run-tests        | Run the test suite for the codebase          |
```