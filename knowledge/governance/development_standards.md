# Development Standards

## Purpose

Define the standard software development practices that AI agents and software developers should follow when implementing, modifying, and maintaining software.

---

## General Development

- Keep solutions simple.
- Do not introduce new architecture unless required.
- Preserve established architectural patterns.
- Never remove existing functionality unless explicitly instructed.
- Review existing implementations before making changes.
- Minimize code changes to the requested scope.
- Prefer readable code over clever code.

---

## Development Workflow

For each implementation:

1. Analyze the existing implementation.
2. Review the affected files before making changes.
3. Implement only the requested scope.
4. Validate the implemented functionality.
5. Update documentation when applicable.
6. Pause for testing or review before proceeding to the next task.

Do not combine unrelated work into a single implementation unless explicitly instructed.

---

## Code Quality

- Follow established naming conventions.
- Keep functions and classes focused on a single responsibility.
- Eliminate dead code when directly related to the implementation.
- Avoid unnecessary duplication.
- Keep dependencies to a minimum.
- Favor maintainability over unnecessary abstraction.

---

## File Modifications

- Update existing files instead of creating new ones when practical.
- New files should have a clearly defined purpose.
- Keep related functionality together.
- Preserve existing formatting and project conventions whenever practical.

---

## Comments

- Follow the project's established commenting conventions.
- Explain intent rather than obvious implementation details.
- Keep comments synchronized with the code.

---

## Error Handling

- Fail gracefully.
- Validate inputs as early as practical.
- Return consistent responses.
- Never expose internal implementation details.

---

## Documentation

- Update project documentation when behavior, architecture, or operational procedures change.
- Keep project knowledge synchronized with the implementation.
- Update governance documents when permanent engineering standards change.

---

## Maintainability

- Optimize for long-term readability and maintainability.
- Avoid premature optimization.
- Favor explicit behavior over hidden complexity.
- Prefer consistency with the existing codebase over introducing new patterns without clear justification.

---

## AI Agent Governance

Development practices should remain consistent with the Engineering Principles, Architecture Principles, Security Standards, Database Standards, API Standards, Logging Standards, and other applicable governance documents contained within the AI Agent Governance Library.
