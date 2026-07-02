```markdown
# drawio-desktop Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `drawio-desktop` repository, a JavaScript-based application for diagramming. The repository does not use a specific framework, and follows a set of conventions for file naming, imports, exports, and testing. This guide will help you quickly understand how to contribute code, write tests, and follow the established workflows.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `diagramEditor.js`, `mainWindow.js`

### Imports
- Use **relative import paths**.
  - Example:
    ```javascript
    import { openFile } from './fileUtils.js';
    ```

### Exports
- Use **named exports**.
  - Example:
    ```javascript
    // fileUtils.js
    export function openFile(path) { ... }
    export function saveFile(path, data) { ... }
    ```

### Commit Messages
- Commit messages are **freeform**, sometimes with prefixes.
- Average length: ~48 characters.
  - Example: `Fix bug in file open dialog`

## Workflows

### Adding a New Feature
**Trigger:** When you need to implement a new feature.
**Command:** `/add-feature`

1. Create a new file using camelCase naming.
2. Write your feature using relative imports and named exports.
3. Add or update tests in a corresponding `.test.js` file.
4. Commit your changes with a clear, concise message.
5. Open a pull request for review.

### Fixing a Bug
**Trigger:** When you need to fix a bug.
**Command:** `/fix-bug`

1. Locate the relevant code using camelCase file names.
2. Make the necessary code changes.
3. Update or add tests to cover the bug fix.
4. Commit with a message describing the fix.
5. Open a pull request.

### Writing Tests
**Trigger:** When adding or updating functionality.
**Command:** `/write-test`

1. Create or update a test file matching `*.test.*` pattern.
2. Write test cases for your code changes.
3. Run tests to ensure they pass.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `fileUtils.test.js`).
- The testing framework is **unknown**; check existing tests for structure.
- Place tests alongside or near the code they test.
- Example test file:
  ```javascript
  // fileUtils.test.js
  import { openFile } from './fileUtils.js';

  test('openFile reads file contents', () => {
    // test implementation
  });
  ```

## Commands
| Command       | Purpose                                 |
|---------------|-----------------------------------------|
| /add-feature  | Start the workflow for adding a feature |
| /fix-bug      | Start the workflow for fixing a bug     |
| /write-test   | Start the workflow for writing tests    |
```
