# Security Policy

PatchPilot is a security scanning tool — it would be ironic to be careless about its own security. We take vulnerability reports seriously and aim to respond quickly.

---

## Supported versions

| Version | Supported |
|---|---|
| `main` branch | ✅ Active development, all fixes applied here |
| Older tagged releases | ⚠️ Critical fixes only, on a best-effort basis |

---

## Reporting a vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, report them privately using one of:

- **GitHub private vulnerability reporting** — go to the [Security tab](https://github.com/ionfwsrijan/PatchPilot/security) → "Report a vulnerability". This is the preferred method as it keeps the report confidential and creates a tracked advisory.
- **Direct message** — contact the maintainer [@ionfwsrijan](https://github.com/ionfwsrijan) via GitHub if the above isn't available.

### What to include in your report

A useful report contains:

- A description of the vulnerability and its potential impact
- The component affected (backend, frontend, a specific endpoint or ML module)
- Step-by-step reproduction instructions
- Any proof-of-concept code or payload
- Your assessment of severity (critical / high / medium / low)

The more detail you provide, the faster we can triage and fix it.

---

## What to expect after reporting

| Timeframe | What happens |
|---|---|
| Within 48 hours | Acknowledgement of your report |
| Within 7 days | Initial assessment and severity confirmation |
| Within 30 days | Fix or mitigation for confirmed vulnerabilities |
| After fix is released | Public disclosure coordinated with you |

We follow responsible disclosure — we'll coordinate the public disclosure timing with you and credit you in the advisory unless you prefer to remain anonymous.

---

## Scope

The following are **in scope** for vulnerability reports:

- Remote code execution via the scan, fix, or verify endpoints
- Path traversal or arbitrary file read/write in ZIP upload or GitHub URL import
- Secret or credential leakage in API responses or logs
- Authentication bypass (if auth is ever added)
- Dependency vulnerabilities with a realistic exploitation path in PatchPilot's context
- Supply chain issues in the ML model loading pipeline

The following are **out of scope:**

- Vulnerabilities in the external CLI tools PatchPilot wraps (Semgrep, OSV-Scanner, Gitleaks) — report those to their respective projects
- Issues that require physical access to the machine running PatchPilot
- Social engineering
- Theoretical vulnerabilities without a working proof of concept

---

## Our commitment

We will not take legal action against researchers who report vulnerabilities in good faith and follow this policy. We appreciate the work of the security research community and will publicly thank reporters (with permission) in release notes.
