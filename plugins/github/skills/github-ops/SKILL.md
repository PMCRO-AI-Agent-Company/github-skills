---
name: github-ops
description: >-
  Governed GitHub repository and GitHub Actions operations for the PMCR-O base
  and domain packs using connected GitHub tools. USE FOR repository inspection,
  branches, commits, files, pull requests, reviews, CI/workflow runs, Actions
  reruns, skill publication and release evidence. TYPE1 for all mutations.
---

# GitHub Ops

Operate GitHub as a governed actuator, not as an implicit authority. Inspect the remote state first, make the smallest correct mutation, then verify the resulting commit/PR/Action state.

## Use for

- Inspecting repository trees, files, branches, commits, issues and PRs.
- Updating PMCR-O repositories under `PMCRO-AI-Agent-Company`.
- Creating branches, commits and PRs with traceable intent/trail identifiers.
- Reviewing diffs and CI status before merge.
- Inspecting GitHub Actions workflow runs, jobs, logs and artifacts.
- Re-running failed jobs only when the failure is understood and retry is appropriate.
- Publishing or updating Agent Skills and plugin manifests.
- Maintaining the GitHub skill catalog and its MCP tool metadata.

## Mutation protocol

1. **Inspect**: repository, branch, current file SHA, and relevant CI state.
2. **Plan**: identify the exact files and expected invariant changes.
3. **Mutate**: use the narrowest GitHub operation available.
4. **Verify**: fetch the resulting commit/file/PR and inspect CI.
5. **Evidence**: report commit SHA, changed paths, tests/Actions results and remaining gaps.

All writes are TYPE 1. Never overwrite a file without its current SHA. Never force-update a branch unless the operation explicitly requires it and the risk is accepted.

## Agent Skills

Follow the open Agent Skills shape: a skill is a directory containing `SKILL.md` plus optional scripts, references and assets. GitHub currently supports project skills in `.github/skills`, `.claude/skills`, and `.agents/skills`; prefer the repository's declared host strategy rather than duplicating the same skill arbitrarily.

Before installing or importing a third-party skill, inspect its `SKILL.md` and file tree. Skills are executable/prompt-bearing supply-chain inputs and may contain prompt injection or malicious scripts.

## GitHub Actions

Treat Actions as part of the repository execution surface. Inspect workflow definitions and the latest run before declaring a repository healthy. Distinguish:

- source-code success,
- workflow/job success,
- deployment success, and
- governance/evaluation success.

A green Action is evidence for the checks it actually executes; it is not proof of unrelated runtime behavior.

## MCP

The connected GitHub tools are the authoritative execution surface for this skill. The checked-in catalog is documentation/metadata, not permission to invent unsupported tool calls. Verify exact tool shapes against the connected host before relying on a catalog entry.

## When not to use

- Local-only filesystem changes without a GitHub remote.
- Non-GitHub remotes.
- Secret/credential management outside the repository's approved security workflow.
