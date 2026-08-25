---
name: github-repository
description: >-
  Inspect and manage GitHub repositories, branches, files, commits, and repository
  metadata with evidence-first mutations. Use for repository setup, structure
  audits, and controlled file changes.
---

# GitHub Repository

Inspect before mutating. Establish repository, default branch, current commit, target path, and file SHA before a write.

## Rules

- Prefer a feature branch for non-trivial changes.
- Use the narrowest mutation available.
- Never overwrite a file without its current blob SHA.
- Preserve repository conventions and CODEOWNERS/security controls.
- Verify the resulting commit and relevant Actions after mutation.

## Evidence

Report repository, branch, commit SHA, changed paths, verification, and remaining gaps.
