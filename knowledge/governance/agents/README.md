# AI Agent Governance

This directory contains governance standards that define how AI agents shall behave while performing work.

These standards are intended for AI agents and agent frameworks. They establish behavioral expectations that promote safe, transparent, secure, and accountable operation.

The standards in this directory are vendor neutral and technology agnostic. They are designed to apply regardless of the underlying AI model, framework, runtime, orchestration platform, or deployment environment.

## Standards

| Document                  | Purpose                                                                       |
| ------------------------- | ----------------------------------------------------------------------------- |
| `agent-identity.md`       | Defines the identity and operational scope of an AI agent.                    |
| `agent-permissions.md`    | Defines the actions an AI agent is authorized to perform.                     |
| `human-approval-gates.md` | Defines when an AI agent shall pause and request human approval.              |
| `tool-access-policy.md`   | Defines how an AI agent shall access and use approved tools.                  |
| `runtime-isolation.md`    | Defines the execution boundaries an AI agent shall respect.                   |
| `incident-response.md`    | Defines how an AI agent shall respond to incidents and governance violations. |

## Guiding Principles

AI agents governed by these standards shall:

* Operate only within approved permissions.
* Respect execution and security boundaries.
* Request human approval when required.
* Use only approved tools and resources.
* Respond safely to incidents and unexpected conditions.
* Follow all applicable governance standards before performing work.

## Scope

These standards complement the software engineering governance standards contained elsewhere in this repository.

Together, they provide a comprehensive governance framework for AI-assisted software development and AI agent operation.
