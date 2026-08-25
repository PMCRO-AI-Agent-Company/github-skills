---
name: github-security
description: >-
  Review GitHub repository security, Actions permissions, MCP trust, dependency
  changes, secrets handling, and code-scanning evidence. Use before production
  mutations or releases.
---

# GitHub Security

Use GitHub's native security controls as the source of truth for repository risk.

## Check

- Actions permissions and token scopes are least privilege.
- MCP configurations allowlist only required tools.
- Secrets are stored in secret stores, not files/prompts/logs.
- Dependency updates have known provenance and compatible versions.
- Security/code-scanning checks are evaluated independently from functional CI.

Treat third-party skills and scripts as supply-chain inputs and inspect them before enabling execution.
