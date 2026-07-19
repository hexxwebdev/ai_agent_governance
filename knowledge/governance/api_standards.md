# Response Standards

API responses should be consistent across all endpoints.

---

# Successful Responses

Successful responses should include, when applicable:

- success
- data
- metadata

---

# Error Responses

Error responses should include, when applicable:

- success
- error
- correlation identifier (for example, a transaction ID, request ID, or trace ID)

Client-facing error messages should:

- Be clear, generic, and safe for end users.
- Never expose implementation details.
- Include a correlation identifier when available to support troubleshooting.

---

# Sensitive Information

API responses must never expose sensitive implementation details, including:

- Stack traces
- SQL statements or database diagnostics
- Internal exception messages
- File paths
- Framework or runtime diagnostics
- Infrastructure details
- Internal implementation details

Detailed diagnostics should be recorded only through the project's standardized logging and observability framework.