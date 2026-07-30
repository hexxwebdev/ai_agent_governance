# Repository AI Agent Instructions

## AI Agent Governance

Before implementing any code changes, review the applicable governance documents under:

`knowledge/governance/`

These documents define the permanent engineering standards for the project and are the authoritative source for implementation decisions.

At a minimum, review and follow:

- engineering_principles.md
- architecture_principles.md
- development_standards.md
- security_standards.md
- database_standards.md
- api_standards.md
- logging_standards.md
- event_logging_standards.md
- code_review_checklist.md

Also review any additional documentation under `/knowledge` that is relevant to the requested work before making implementation changes.

Apply the guidance from the governance documents throughout implementation, code review, validation, and documentation updates.

Do not duplicate governance content elsewhere unless a project-specific exception is required.

---

## AI Agent Runtime Governance

The `/knowledge/governance/agents` folder contains runtime governance standards for AI agents.

These documents define how AI agents should operate within a project, including execution boundaries, permissions, approval requirements, security guardrails, and other runtime expectations.

AI agents should review both:

1. The engineering standards in `/knowledge/governance`.
2. The runtime governance documents in `/knowledge/governance/agents`.

The runtime governance documents complement the engineering standards by defining how agents should behave while performing work, rather than how software should be designed or implemented.

---

# Project-Specific Standards

This section is intentionally reserved for repository-specific instructions that extend or customize the AI Agent Governance Library.

---

# Development Workflow

Unless explicitly instructed otherwise:

- Review the applicable governance documents and any relevant documentation under `/knowledge` before making code changes.
- Review the existing implementation before modifying any file.
- Preserve unrelated logic and existing application behavior unless the task explicitly requires otherwise.
- Keep changes limited to the requested scope.
- Complete all required code changes before considering the task complete.
- Perform appropriate local validation such as builds, syntax checks, unit tests, application startup, API testing, or other relevant verification.
- Report the validation results.
- Pause after successful validation for user testing and approval before proceeding to the next task.
- Never commit changes unless explicitly instructed.
- Before considering the task complete, update any applicable documentation under `/knowledge` and any relevant governance documents to reflect architectural, security, operational, API, database, or workflow changes introduced by the implementation. Keep documentation synchronized with the codebase. If no documentation updates were required, explicitly state that none were necessary.

---

# Non-Production Validation

Projects should be validated in a non-production environment unless explicitly instructed otherwise.

Validation should be appropriate for the technology being modified and may include:

- Application startup
- Build verification
- Syntax validation
- Unit or integration tests
- API testing using `curl` or similar tools
- Database validation where applicable
- End-to-end workflow validation when practical

Do not consider a task complete until the requested functionality has been validated in a non-production environment or any validation limitations have been clearly documented.

---

# Non-Interactive Editing

- Never invoke interactive editors such as `vi`, `vim`, or `nano`.
- Use non-interactive patch-based editing whenever practical.
- If a patch cannot be applied due to conflicting changes, retry using smaller, more targeted patches.
- If editing fails because of an environment, sandbox, or tooling issue, stop immediately and report the failure.
- Do not bypass environment or sandbox failures using alternative editing techniques.
- When an alternative non-interactive edit is appropriate, use the least invasive method that modifies only the requested sections while preserving all unrelated logic and formatting.
- Full-file rewrites are a last resort and should only be used when they are the safest option.
- Before performing a full-file rewrite, verify that the existing file is preserved except for the requested changes.
- If the requested edit cannot be completed safely, stop and explain why rather than risking unintended modifications.
- Complete file modifications without requiring user interaction whenever practical.

---

# Command Approval

- Avoid commands that require user approval when an equivalent non-interactive approach exists.
- Batch related file edits into as few commands as practical.
- Request approval only when required by the execution environment or when elevated privileges are genuinely necessary.

---

# Command Execution

- Prefer read-only commands for inspection and analysis.
- Use non-interactive commands whenever possible.
- Batch related inspections into as few commands as practical.
- Avoid commands that require approval when an equivalent read-only or non-interactive command exists.
- Never use interactive editors.
- Diagnose patch failures before attempting an alternative editing method.
- Distinguish between patch conflicts and environment or tooling failures:
  - For patch conflicts, retry using smaller scoped patches.
  - For environment or tooling failures, stop and report the issue rather than attempting a workaround.
- When an alternative editing method is necessary, use the least invasive approach possible.
- Never remove, refactor, or alter unrelated logic outside the requested scope.
- Preserve existing application behavior unless the requested task explicitly requires a functional change.

---

# Environment Failures

If a file edit fails because of an execution environment or sandbox failure (for example permission restrictions or infrastructure errors), stop immediately and report the failure.

Do not attempt to bypass infrastructure failures using alternative editing techniques.

Infrastructure failures are environmental issues, not repository issues, and should be resolved before implementation continues.
