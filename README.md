# AI Agent Governance

A vendor-neutral governance framework and documentation structure for **AI coding agents**.

Unlike enterprise AI governance platforms that focus on organizational policies, compliance, and human oversight, this project defines the operational standards that AI agents follow while analyzing, modifying, testing, documenting, and deploying software.

It provides reusable engineering standards and a recommended repository organization that help AI coding agents and software developers build secure, maintainable, and well-documented software.

---

# Design Goals

This project is designed to be:

* **AI agent friendly** by providing documentation that AI coding assistants can easily understand and follow.
* **Vendor neutral** without depending on any specific AI provider, IDE, cloud platform, or development tool.
* **Technology agnostic** so it can be adopted by projects using any language, framework, or architecture.
* **Simple to adopt** with a lightweight structure that integrates into new or existing repositories.
* **Easy to customize** so organizations can extend or modify standards to meet their own requirements.
* **Focused on long-lived engineering guidance** rather than project-specific implementation details.

---

# What This Repository Provides

## AGENTS.md

Repository-level instructions that guide AI agents while working within a software project.

Typical responsibilities include:

* Development workflow
* Coding conventions
* Testing requirements
* Deployment procedures
* Project-specific instructions
* AI agent expectations

Each project should maintain its own customized `AGENTS.md`.

---

## Knowledge Base

The `knowledge` directory contains documentation describing an application's implementation.

Typical documents include:

* Project overview
* Architecture
* API documentation
* Database design
* Deployment
* Authentication
* Configuration
* Frontend
* Routes
* Background jobs
* Support information
* Changelog

These documents evolve alongside the application.

---

## AI Agent Governance

The `knowledge/governance` directory contains permanent engineering standards that guide implementation decisions.

These standards are intended to remain largely stable across projects and should be reviewed by both AI agents and software developers before implementing significant changes.

Current governance documents include:

* Engineering Principles
* Architecture Principles
* Development Standards
* Security Standards
* Database Standards
* API Standards
* Logging Standards
* Event Logging Standards
* Code Review Checklist

---

# Recommended Repository Structure

```text
my-project/
├── AGENTS.md
├── knowledge/
│   ├── README.md
│   ├── architecture.md
│   ├── api.md
│   ├── database.md
│   ├── deployment.md
│   ├── ...
│   └── governance/
│       ├── engineering_principles.md
│       ├── architecture_principles.md
│       ├── development_standards.md
│       ├── security_standards.md
│       ├── database_standards.md
│       ├── api_standards.md
│       ├── logging_standards.md
│       ├── event_logging_standards.md
│       └── code_review_checklist.md
```

---

## Versioning

This project follows Semantic Versioning (SemVer).

Project history is tracked through Git commits and version tags. A separate `CHANGELOG.md` is intentionally not maintained.

---

# License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

# Contributing

Contributions that improve the clarity, portability, and long-term usefulness of these governance standards are welcome.

Please review `CONTRIBUTING.md` before submitting changes.