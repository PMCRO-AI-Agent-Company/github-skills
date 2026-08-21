---
name: github-ops
description: >-
  GitHub repository operations for the PMCR-O base and packs using connected
  GitHub MCP tools. USE FOR create/update repos, push files, branches, PRs,
  tree inspection, and pack overlay publish. DO NOT USE for non-GitHub remotes
  or local-only files. TYPE1 for all mutations.
---

# GitHub Ops

Drives the **connected GitHub MCP** (or a future self-hosted `Pmcro.Mcp.GitHub`
built from the declarative spec). All writes are TYPE1.

## When to Use

- Publish or update `PMCRO-AI-Agent-Company/pmcro-company-template`
- Create org/personal repos for company projects
- Push bare-engine batches or pack overlay branches
- Open PRs with trail UUID in the body
- Inspect remote tree vs local bare zip
- Scaffold a custom GitHub MCP server from `plugins/pmcro/references/connectors/github-mcp-server.spec.yaml` via `create-mcp-server`

## When Not to Use

- Local-only commits with no GitHub remote → version-control
- Source dumps / zips → filesystem-agent
- Non-GitHub hosts

## MCP tool catalog

| Artifact | Role |
|----------|------|
| `assets/github-mcp-tools.json` | Machine shapes (connected tools) |
| `references/github-mcp-catalog.md` | Human ops notes |
| `plugins/pmcro/references/connectors/github-mcp-server.spec.yaml` | Declarative server matching this catalog (lives centrally with the other connector specs, same as `figma-mcp-server.spec.yaml`) |

Tool names match a standard host GitHub MCP (`github___*`). No GitHub MCP
was connected when this catalog was authored, so tool shapes were drafted
from the well-known GitHub MCP server surface, not pulled live — verify
against the actual connected host before relying on exact parameter names.
