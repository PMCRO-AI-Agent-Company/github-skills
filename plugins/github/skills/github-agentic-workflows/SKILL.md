---
name: github-agentic-workflows
description: >-
  Design GitHub Actions agentic workflows using the current GitHub Agentic
  Workflows tooling and repository skills. Use when an AI coding agent must
  author or operate an Actions workflow from natural-language intent.
---

# GitHub Agentic Workflows

Use GitHub's current agentic-workflow authoring flow and keep the workflow itself explicit, reviewable, and least-privilege.

## Rules

- Initialize the repository with the supported agentic workflow tooling rather than inventing a parallel convention.
- Use the dedicated agentic-workflows skill when authoring workflow files.
- Keep secrets in GitHub Actions/Agents secret storage, never in workflow text.
- Review generated workflow permissions and tool access before enabling it.
- Test with a narrow task first and preserve logs/artifacts.

## PMCRO

Agentic Actions can execute work, but PMCRO governance still requires Planner intent, bounded mutation, Checker evidence, and Reflector disposition where the workflow participates in a governed cycle.
