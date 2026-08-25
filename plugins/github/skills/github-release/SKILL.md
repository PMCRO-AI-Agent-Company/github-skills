---
name: github-release
description: >-
  Prepare and publish GitHub releases and release evidence, including version
  metadata, tags, changelogs, artifacts, and post-release verification. Use for
  production release work.
---

# GitHub Release

Release only from a verified commit. Ensure version metadata, changelog, CI, and artifact provenance agree.

## Gate

1. Confirm target commit and branch.
2. Confirm required checks.
3. Generate release notes from actual changes.
4. Create tag/release using repository policy.
5. Verify published assets and source commit.
6. Record release evidence and rollback path.

Never infer a successful release from a successful build alone.
