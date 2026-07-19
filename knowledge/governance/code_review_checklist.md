# Purpose

Define the minimum verification steps that AI agents and software developers should perform before implementation is considered complete.

---

# Functional Review

- Requirements have been fully implemented.
- Existing functionality remains unchanged unless intentionally modified.
- Edge cases have been considered.
- Error handling has been validated.

---

# Security Review

- Authentication is preserved where applicable.
- Authorization is enforced where applicable.
- Sensitive data is never exposed.
- Input validation exists where applicable.
- Database access uses secure, parameterized queries where applicable.
- Secrets are never hardcoded.
- Client-facing error responses are properly sanitized.

---

# API Review

When applicable:

- API behavior is consistent.
- Response formats follow established standards.
- Backward compatibility has been preserved whenever practical.
- Public endpoints do not modify data unless explicitly intended.

---

# Logging Review

When applicable:

- Standardized logging and event logging have been implemented.
- Sensitive information is never logged.
- Correlation identifiers are included where appropriate.
- Event codes follow established standards.

---

# Database Review

When applicable:

- Data integrity is preserved.
- Data access is appropriately scoped.
- Transactions are used where appropriate.
- Schema changes include the required migration or deployment artifacts.

---

# Documentation Review

- Project documentation has been updated when behavior, architecture, or operational procedures have changed.
- Governance documents have been updated when permanent standards have changed.
- New event codes or logging behaviors have been documented where applicable.

---

# Maintainability Review

- The implementation follows the Engineering Principles.
- The solution remains simple, readable, and maintainable.
- Existing architectural patterns have been preserved unless intentionally changed.
- Unnecessary complexity has not been introduced.