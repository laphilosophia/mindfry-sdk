# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 0.1.x   | :white_check_mark: |

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them via email to: **erdemarslan@ymail.com**

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Resolution Target**: Within 30 days (depending on severity)

### What to Expect

1. **Acknowledgment**: We will confirm receipt of your report
2. **Investigation**: We will investigate and validate the issue
3. **Communication**: We will keep you informed of our progress
4. **Credit**: We will credit you in security advisories (unless you prefer anonymity)

## SDK-Specific Security Considerations

When using the MindFry SDK:

1. **Connection Security**: The SDK uses raw TCP. For production, use TLS termination.
2. **Input Validation**: Validate user input before passing to SDK methods.
3. **Timeout Configuration**: Set appropriate timeouts to prevent resource exhaustion.
4. **Backpressure**: Configure `maxPending` to limit memory usage under load.

## Security Advisories

Published advisories will be listed here and on the GitHub Security tab.
