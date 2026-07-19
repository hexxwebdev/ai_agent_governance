# Engineering Principles

## Purpose

These principles govern engineering decisions made by AI agents and software developers.

When multiple valid solutions exist, apply these principles in the order presented.

---

## Core Principles

1. Keep the solution as simple as possible.
2. Follow established industry standards whenever practical.
3. Build security into the design by default.
4. Avoid unnecessary abstraction, frameworks, and architectural complexity.
5. Optimize for long-term maintainability and readability.

---

## Decision Order

When choosing between multiple acceptable implementations, prefer the solution that is:

1. Simplest
2. Most secure
3. Most maintainable
4. Most consistent with established project patterns
5. Closest to accepted industry standards

Do not introduce enterprise-level complexity unless it is clearly justified by the project requirements.

---

## Architectural Philosophy

- Prefer native platform capabilities over custom implementations whenever practical.
- Preserve established architectural patterns unless a change is intentionally required.
- Preserve existing application behavior unless the requested work requires a functional change.
- Minimize technical debt.
- Favor readability over cleverness.
- Design for long-term maintainability.
- Build only what is currently required.
- Avoid speculative architecture and premature optimization.

---

## Implementation Principles

Before modifying existing code:

- Understand the current implementation.
- Review the affected files before making changes.
- Preserve unrelated logic and functionality.
- Limit changes to the requested scope.
- Avoid refactoring outside the immediate objective unless explicitly requested.
- Reuse existing patterns before introducing new ones.

---

## Simplicity Standard

Every implementation should answer **"Yes"** to the following questions whenever practical:

- Is this the simplest solution that satisfies the requirements?
- Is the implementation understandable by another developer or AI agent?
- Does it minimize future maintenance?
- Does it avoid unnecessary dependencies and complexity?
- Does it preserve existing functionality outside the requested scope?

---

## AI Agent Governance

These principles are the highest-level engineering guidance within the AI Agent Governance Library and should take precedence whenever implementation decisions require balancing competing approaches.
