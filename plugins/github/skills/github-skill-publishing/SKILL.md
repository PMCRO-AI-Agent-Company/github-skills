---
name: github-skill-publishing
description: >-
  Publish and validate Agent Skills and plugin metadata in GitHub repositories.
  Use when adding SKILL.md packages, marketplace entries, manifests, releases,
  or cross-repository skill catalogs.
---

# GitHub Skill Publishing

A skill must follow the open Agent Skills directory contract: `SKILL.md` with valid `name` and `description` frontmatter plus optional resources.

## Publish gate

1. Validate skill directory and frontmatter.
2. Inspect scripts/references/assets for supply-chain risk.
3. Update the plugin manifest/catalog.
4. Add or update tests/evals where available.
5. Run CI and inspect the resulting commit.
6. Publish only from the verified branch/commit.

Keep runtime instance state out of distributable skill repositories.
