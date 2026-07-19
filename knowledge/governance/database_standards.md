# Purpose

Define the database standards that AI agents and software developers should follow when designing, implementing, and maintaining data storage.

---

# Database Principles

- Maintain data integrity.
- Protect data by default.
- Favor simple, normalized schemas.
- Minimize unnecessary complexity.
- Design for long-term maintainability.

---

# Data Access

- Use parameterized queries whenever supported.
- Never construct queries by concatenating untrusted input.
- Validate all external input before performing database operations.
- Validate identifiers, enumerations, and numeric ranges.
- Prevent injection attacks appropriate to the underlying database technology.

---

# Data Integrity

- Use appropriate primary keys.
- Define foreign key constraints where appropriate.
- Preserve referential integrity.
- Use transactions for multi-step operations where supported.
- Fail atomically whenever practical.

---

# Schema Design

- Keep schemas normalized unless denormalization provides measurable value.
- Use descriptive table and column names.
- Avoid unnecessary duplicate data.
- Keep nullable fields to a minimum.
- Maintain consistent naming conventions throughout the schema.

---

# Security

- Scope data access to the authenticated user unless explicitly administrative.
- Never expose internal identifiers unnecessarily.
- Never trust client-supplied ownership or authorization information.
- Protect sensitive data using appropriate encryption or platform security features.
- Store database credentials using secure secret management provided by the platform.

---

# Migrations

- All schema changes should be managed through version-controlled migrations.
- Migrations should be repeatable and reversible whenever practical.
- Avoid manual changes to production schemas except during documented operational procedures.

---

# Performance

- Create indexes only when justified by measured usage.
- Avoid unnecessary database operations.
- Prevent N+1 query patterns where applicable.
- Optimize based on measured performance rather than assumptions.

---

# AI Agent Governance

Database implementations should remain consistent with the Engineering Principles, Security Standards, Architecture Principles, API Standards, Logging Standards, and other applicable governance documents contained within the AI Agent Governance Library.
