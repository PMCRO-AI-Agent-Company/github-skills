---
name: github-actions
description: >-
  Diagnose, validate, rerun, and improve GitHub Actions workflows using workflow
  definitions, runs, jobs, logs, artifacts, and status checks. Use for CI/CD
  failures, agentic workflows, and release gates.
---

# GitHub Actions

A green workflow proves only the checks it actually executes. Separate source-code correctness, workflow health, deployment health, and governance/evaluation evidence.

## Workflow

1. Inspect the workflow definition.
2. Identify the exact run/commit.
3. Inspect failed jobs and logs.
4. Determine whether the failure is deterministic, transient, or configuration-related.
5. Rerun only an understood failed job/run when appropriate.
6. Verify the new result and record evidence.

For agentic workflows, keep permissions least-privilege, make tool access explicit, and retain artifacts/logs needed for audit.
