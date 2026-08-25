---
name: github-pull-requests
description: >-
  Create, inspect, review, update, and merge GitHub pull requests with diff,
  review-thread, approval, and CI evidence. Use for governed PR lifecycle work.
---

# GitHub Pull Requests

Treat a PR as a verifiable change proposal, not merely a merge button.

## Workflow

1. Inspect base/head refs and current diff.
2. Validate changed files and tests.
3. Review inline comments and unresolved threads.
4. Check required Actions/status checks.
5. Merge only when policy and evidence permit.

Prefer squash/rebase/merge according to repository policy; never invent the repository's preferred method.

## Evidence

Capture PR number, head SHA, review state, CI state, unresolved concerns, and final merge SHA when applicable.
