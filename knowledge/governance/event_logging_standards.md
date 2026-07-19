# Event Logging Standards

## Purpose

Define the standard structure and practices for application event logging.

Not every application requires event logging. Implement event logging only when it provides meaningful operational, security, audit, compliance, or business value.

When event logging is implemented, follow these standards.

---

# Event Structure

Application events should use a consistent structured format, such as JSON.

Example:

```json
{
  "event_code": "AUTH-001",
  "event_name": "User Login",
  "severity": "info",
  "timestamp": "2026-07-18T14:35:22Z",
  "application": "orders",
  "module": "authentication",
  "message": "User successfully authenticated.",
  "metadata": {
    "user_id": 12345
  }
}
```

---

# Required Information

Every event should include:

| Information | Description |
|-------------|-------------|
| Event Code | Stable identifier for the event. |
| Event Name | Human-readable event name. |
| Severity | Event severity level. |
| Timestamp | UTC timestamp using ISO 8601 format. |
| Application | Application or service generating the event. |
| Module | Functional area generating the event. |
| Message | Brief description of the event. |

Projects may choose their own field names provided they remain consistent throughout the application.

---

# Optional Information

Examples include:

- Metadata
- User identifier
- Request identifier
- Session identifier
- Correlation identifier
- Duration
- Resource identifier
- Exception information

Include optional information only when it provides meaningful operational, security, or audit value.

---

# Event Codes

Use a stable event code naming convention.

Examples:

```
AUTH-001
AUTH-002
DB-001
DB-002
API-001
API-002
ORDER-001
ORDER-002
SYSTEM-001
```

Once introduced, event codes should remain stable to preserve historical consistency.

---

# Severity Levels

| Level | Usage |
|-------|-------|
| debug | Development and troubleshooting |
| info | Normal application activity |
| warning | Unexpected but recoverable condition |
| error | Failure requiring investigation |

---

# Best Practices

- Keep event messages concise and meaningful.
- Avoid duplicate or redundant events.
- Never log passwords, secrets, tokens, API keys, or sensitive personal information.
- Prefer structured logging over free-form text.
- Include only metadata that supports troubleshooting, auditing, or operational monitoring.
- Use UTC timestamps in ISO 8601 format.
- Keep event names and event codes consistent throughout the application.

---

# AI Agent Governance

Event logging implementations should remain consistent with the Logging Standards, Security Standards, Engineering Principles, and other applicable governance documents contained within the AI Agent Governance Library.
