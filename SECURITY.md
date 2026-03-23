# Security Policy

## Supported Versions

| Version | Supported          |
|---------|--------------------|
| 1.0.x   | ✅ Yes             |
| < 1.0   | ❌ No              |

## Reporting a Vulnerability

If you discover a security vulnerability in Lnr, please report it responsibly.

**⚠️ Do NOT open a public GitHub issue for security vulnerabilities.**

### How to Report

1. **Email**: Send details to the project maintainer via GitHub (use the private vulnerability reporting feature if available)
2. **GitHub Security Advisory**: Use the [Security Advisories](https://github.com/ArtemTykhonuk/LnrPlugin-Public/security/advisories/new) feature to privately report the vulnerability

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

### Response Timeline

- **Acknowledgment**: Within 48 hours
- **Initial assessment**: Within 5 business days
- **Fix release**: As soon as possible, depending on severity

### Scope

The following are in scope:

- API key handling and storage
- Data transmission security (HTTPS, GraphQL)
- AI provider credential handling
- Plugin update mechanism
- Any data leakage or unauthorized access

### Out of Scope

- Issues in Linear.app itself (report to [Linear](https://linear.app/security))
- Issues in JetBrains IDEs (report to [JetBrains](https://www.jetbrains.com/legal/terms/responsible-disclosure.html))
- Issues in third-party AI providers (OpenAI, etc.)

## Security Best Practices for Users

- Keep your Linear API key confidential
- Use a dedicated API key for the plugin (not your personal one)
- Keep your IDE and Lnr plugin updated to the latest version
- If using OpenAI-compatible AI, ensure your endpoint uses HTTPS
