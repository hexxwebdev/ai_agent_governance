# AI Agent Governance Library

## Purpose

The AI Agent Governance Library defines the permanent engineering, architectural, security, and development standards that AI agents should follow when implementing, reviewing, or modifying software.

These documents serve as the authoritative governance reference for AI agents and software developers across any project that adopts this library.

---

# Scope

This library defines permanent engineering governance.

It does not contain:

- AI agent workflow instructions
- Repository-specific conventions
- Temporary project notes
- Feature specifications
- User documentation
- Project planning

Those belong elsewhere within the consuming repository.

---

# Governance Documents

| Document | Purpose |
|----------|---------|
| engineering_principles.md | Core engineering philosophy and decision-making principles. |
| architecture_principles.md | System architecture guidance and design philosophy. |
| development_standards.md | General coding and implementation standards. |
| security_standards.md | Security requirements and secure development practices. |
| database_standards.md | Database design, access, and integrity standards. |
| api_standards.md | API design and implementation standards. |
| logging_standards.md | Logging, diagnostics, and observability standards. |
| event_logging_standards.md | Standardized application event logging requirements. |
| code_review_checklist.md | Minimum verification checklist before implementation is considered complete. |

---

# Governance Hierarchy

When guidance overlaps, apply documents in the following order:

1. Engineering Principles
2. Security Standards
3. Architecture Principles
4. Domain-Specific Governance
5. Project Documentation

---

# Repository Consistency

The AI Agent Governance Library is intended to provide a consistent governance baseline across all repositories that adopt it.

Repository-specific additions or deviations should be rare, intentional, and documented within the affected governance document.

---

# Future Governance

Additional governance documents may be introduced as the library evolves, including:

- Frontend Standards
- UI/UX Standards
- Documentation Standards
- Knowledge Base Standards
- AI Standards
- Observability Standards
- Event Ingestion Standards
- Deployment Standards
- Testing Standards
- Performance Standards
- Accessibility Standards
- Mobile Standards
- Data Import Standards

Each governance document should have a single responsibility and avoid duplicating guidance already defined elsewhere within the governance library.

---

# Relationship to AGENTS.md

If a repository includes an `AGENTS.md` file:

- `AGENTS.md` defines AI agent workflow, repository-specific operating instructions, and repository conventions.
- The AI Agent Governance Library defines the permanent engineering, architectural, security, and development standards that AI agents should follow.

Whenever practical, project documentation should reference the AI Agent Governance Library instead of duplicating governance content.

---

# Maintenance

Governance documents should:

- Remain concise and focused.
- Follow accepted industry standards whenever practical.
- Be updated as engineering standards evolve.
- Be reviewed before introducing new architectural or development patterns.
- Remain synchronized across repositories that adopt this library unless a documented exception exists.

---

## AI Agent Runtime Governance

The `agents` folder contains runtime governance standards for AI agents.

These documents define how AI agents should operate while performing work, including permissions, execution boundaries, approval requirements, and security guardrails.

Together with the engineering standards in this folder, they provide a complete governance framework for AI-assisted software development.

---
