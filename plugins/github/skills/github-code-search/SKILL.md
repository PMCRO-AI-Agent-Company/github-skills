---
name: github-code-search
description: >-
  Search GitHub repositories for implementation patterns, APIs, errors, and
  configuration before changing code. Use for evidence-first discovery and
  cross-repository consistency checks.
---

# GitHub Code Search

Search before inventing. Narrow by repository or organization whenever possible and use exact symbols/error strings for implementation investigations.

## Rules

- Search current code, not only README claims.
- Validate the target branch/ref before relying on a match.
- Prefer authoritative repository sources and recent commits.
- Treat copied code as evidence, not permission to reproduce obsolete patterns.
- Cross-check package/API versions before implementing a match.

## Evidence

Record query intent, repositories searched, relevant paths/commits, and the reason the selected implementation is current.
