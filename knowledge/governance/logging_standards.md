# Logging Standards

## Purpose

Define consistent logging standards that AI agents and software developers should follow when implementing application logging.

---

# Logging Principles

- Log information that is useful for troubleshooting, auditing, operational monitoring, and application health.
- Prefer structured logging whenever practical.
- Keep log messages concise and meaningful.
- Avoid duplicate, excessive, or unnecessary logging.
- Logging must never interrupt normal application execution.

---

# Sensitive Data

Never log sensitive information such as:

- Passwords
- Secrets
- API keys
- Access tokens
- Session tokens
- Cookies
- Database connection strings
- Personally identifiable information (PII)
- Protected Health Information (PHI) subject to HIPAA
- Financial information
- Request or response bodies containing sensitive data

Redact or omit sensitive values before writing logs.

---

# Log Levels

Use the appropriate log level for each message.

| Level | Usage |
|-------|-------|
| DEBUG | Development and troubleshooting details |
| INFO | Normal application activity |
| WARNING | Recoverable or unexpected conditions |
| ERROR | Application failures requiring investigation |

---

# Structured Logging

When practical, log entries should use a consistent structured format.

Example:

```json
{
  "timestamp": "2026-07-18T15:22:41Z",
  "level": "INFO",
  "application": "orders",
  "module": "customer",
  "message": "Customer record created.",
  "metadata": {
    "customer_id": 1234
  }
}
```

---

# Recommended Information

Include applicable information such as:

- Timestamp
- Log level
- Application or service
- Module or component
- Message
- Request identifier
- Correlation identifier
- User identifier
- Duration
- Metadata

Not every log entry requires every item.

Projects may choose their own field names provided they remain consistent throughout the application.

---

# Error Logging

- Log enough information to diagnose the problem.
- Keep client-facing error messages separate from diagnostic logs.
- Never expose stack traces or internal implementation details to end users.
- Never log sensitive application data.

---

# Console Logging

- Console logging is acceptable during local development.
- Use a consistent logging approach throughout the application.
- Avoid temporary or excessive debug logging in completed features.
- Remove obsolete debugging statements when modifying existing code.

---

# Performance

- Logging should have minimal impact on application performance.
- Avoid excessive logging inside loops or frequently executed code paths.
- Log meaningful events rather than every operation.

---

# Retention

- Follow the application's log retention requirements.
- Do not retain sensitive information longer than necessary.
- Retain only the information required for operational, security, audit, or compliance purposes.

---

# AI Agent Governance

Logging implementations should remain consistent with the Event Logging Standards, Security Standards, Engineering Principles, and other applicable governance documents contained within the AI Agent Governance Library.
