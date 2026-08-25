# ⚙️ PMCRO GitHub Skills

Governed GitHub repository and GitHub Actions operations for the PMCR-O base and domain packs, using the connected GitHub tools as the execution surface.

## Capability pack

| Skill | Purpose |
|---|---|
| `github-ops` | Core repository/branch/commit/PR/CI mutation protocol. |
| `github-repository` | Repository inspection and evidence-first file changes. |
| `github-pull-requests` | PR diff, review, status, approval, and merge lifecycle. |
| `github-actions` | Workflow runs, jobs, logs, artifacts, reruns, and CI gates. |
| `github-agentic-workflows` | Current GitHub Agentic Workflows authoring and least-privilege operation. |
| `github-mcp` | GitHub MCP transport, authentication, tool allowlists, and trust. |
| `github-code-search` | Current implementation discovery and cross-repository evidence. |
| `github-issues` | Durable defect/architecture/operations tracking. |
| `github-release` | Release, tag, artifact, provenance, and rollback verification. |
| `github-security` | Actions/MCP/dependency/secrets/security-control review. |
| `github-skill-publishing` | Agent Skills validation, marketplace manifests, and publication gates. |

## Operating model

```text
INSPECT → PLAN → MUTATE → VERIFY → EVIDENCE
```

All repository mutations are TYPE 1. The skill must inspect current remote state and file SHAs before writes, then verify the resulting commit/PR and relevant Actions status.

## Current GitHub MCP baseline

GitHub documents `https://api.githubcopilot.com/mcp/` as the current remote GitHub MCP endpoint for supported hosts. Repository-level Copilot MCP configurations can allowlist tools and are autonomous once enabled, so least privilege is mandatory. citeturn3search0turn3search1

## Agent Skills

The pack follows the open Agent Skills model: `SKILL.md` plus optional `scripts/`, `references/`, and `assets/`. Third-party skills are treated as supply-chain inputs and must be inspected before installation.

## GitHub Actions

Actions are part of the execution harness. The skill distinguishes source correctness from workflow correctness, deployment correctness, and PMCR-O evaluation/governance correctness. A green workflow is evidence only for the checks it actually executes.

## Related PMCR-O repositories

- `pmcro-runtime` — execution runtime
- `pmcro-skills` — governed marketplace and laws
- `agent-skills` — Agent Skills authoring/template base
- `dotnet-skills` — .NET domain capabilities
- `figma-skills` — Figma domain capabilities
