# Security Standards

## Purpose

Define the baseline security standards that AI agents and software developers should follow when designing, implementing, and maintaining software.

---

# Security Philosophy

- Build with security by default.
- Follow practical, risk-based security practices.
- Prefer simple, secure solutions over unnecessary complexity.
- Apply defense in depth where appropriate.
- Treat security as a continuous engineering responsibility.

---

# Industry Guidance

When practical, align implementations with recognized industry guidance, including:

- OWASP Application Security Verification Standard (ASVS)
- OWASP API Security Top 10
- OWASP Top 10
- NIST Cybersecurity Framework (CSF)

Projects may adopt additional regulatory or industry-specific requirements as needed.

---

# Secure Development

All applications should:

- Validate all external input.
- Sanitize user-supplied data when appropriate.
- Use parameterized queries or prepared statements for database access.
- Never trust client-supplied data.
- Follow the principle of least privilege.
- Use secure defaults whenever practical.
- Return generic client-facing error messages.
- Keep internal implementation details private.

---

# Sensitive Data

Protect sensitive information including:

- Passwords
- Secrets
- API keys
- Access tokens
- Session tokens
- Database credentials
- Personally identifiable information (PII)
- Protected Health Information (PHI) subject to HIPAA
- Financial information
- Confidential business information

Sensitive information must never be exposed in logs, error messages, client responses, or source control.

---

# Authentication and Authorization

When authentication is required:

- Authenticate users before granting access to protected functionality.
- Verify authorization for restricted operations.
- Never trust client-supplied identity information.
- Perform authorization checks on the server whenever applicable.
- Deny access by default unless explicitly authorized.

---

# Database Security

- Use parameterized queries or prepared statements.
- Never construct database queries using untrusted input.
- Validate input before database operations.
- Grant applications only the permissions they require.
- Avoid unnecessary direct database access.

---

# API Security

When building APIs:

- Validate every request.
- Validate uploaded files before processing.
- Return sanitized error responses.
- Protect sensitive operations with authentication and authorization where appropriate.
- Restrict administrative functionality to authorized users.
- Use HTTPS whenever the application is accessible over a network.

---

# Abuse Protection

Applications should implement appropriate protections against abuse based on their risk profile.

Consider controls such as:

- Rate limiting
- Request throttling
- Request size limits
- File upload limits
- Input validation
- Resource quotas
- Account lockout or backoff for repeated authentication failures
- Bot or automated abuse mitigation where appropriate

Security controls should be proportional to the application's functionality, exposure, and operational risk.

---

# Secrets Management

- Store secrets using environment variables or an approved secret management solution.
- Never hardcode secrets.
- Never commit secrets to source control.
- Rotate secrets when compromise is suspected or confirmed.
- Remove unused secrets promptly.

---

# Dependency Security

- Keep dependencies reasonably up to date.
- Remove unused packages and libraries.
- Prefer actively maintained dependencies.
- Review new dependencies before introducing them into the project.
- Avoid introducing unnecessary dependencies.

---

# Error Handling

- Do not expose stack traces to end users.
- Do not expose SQL statements, database diagnostics, or internal implementation details.
- Keep diagnostic logging separate from client-facing error responses.
- Fail securely when unexpected errors occur.

---

# Security Reviews

When implementing new functionality, consider:

- Input validation
- Authentication requirements
- Authorization requirements
- Sensitive data exposure
- Injection risks
- File upload risks
- Dependency risks
- Logging of sensitive information
- Secure configuration
- Abuse protection requirements

Address identified risks before considering the implementation complete.

---

# AI Agent Governance

Security implementations should remain consistent with the Engineering Principles, Architecture Principles, Database Standards, API Standards, Logging Standards, Event Logging Standards, and other applicable governance documents contained within the AI Agent Governance Library.

---

# Continuous Improvement

Security standards should evolve as applications mature, threats change, technologies advance, and new regulatory or business requirements are introduced.
