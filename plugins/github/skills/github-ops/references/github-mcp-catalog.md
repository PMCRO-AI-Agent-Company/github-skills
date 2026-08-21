# GitHub MCP tool catalog — ops notes

Human-readable companion to `assets/github-mcp-tools.json`. Tool names match
the connected host GitHub MCP; the declarative spec at
`references/github-mcp-server.spec.yaml` is the fallback contract if a
self-hosted `Pmcro.Mcp.GitHub` is ever scaffolded via `create-mcp-server`.

## TYPE2 — reads (auto-approve)

| Tool | Use |
|------|-----|
| `github___whoami` | Confirm identity/org/scopes before any write |
| `github___get_repository` | Check default branch, visibility before touching it |
| `github___get_file_contents` | Read a file or list a directory tree at a ref |
| `github___list_commits` | Inspect history for a branch or path |
| `github___list_branches` | Enumerate branches before creating/targeting one |
| `github___list_pull_requests` | Check open/closed PRs before opening a duplicate |

## TYPE1 — mutations (stub-and-halt, HIL required)

| Tool | Use |
|------|-----|
| `github___create_repository` | New org/personal repo for a company project |
| `github___create_branch` | Branch for a pack overlay or bare-engine batch |
| `github___push_files` | Multi-file commit in one call — prefer over repeated single-file writes |
| `github___create_or_update_file` | Single-file commit when only one file changes |
| `github___create_pull_request` | Open PR — **body must carry the trail UUID** |
| `github___merge_pull_request` | Merge only after Check/Reflect have sealed ACCEPT |

## Rules

1. `whoami` before the first write of a session — never assume identity/org.
2. Every mutation is TYPE1: stub the intended call, halt, wait for `/approve`.
3. PR bodies always include the trail UUID so the Colony can trace the change
   back to its sealed cycle.
4. Prefer `push_files` for multi-file commits over N calls to
   `create_or_update_file` — fewer TYPE1 halts, one clean commit.
5. This skill never touches non-GitHub remotes or local-only commits — that's
   version-control, not github-ops.
