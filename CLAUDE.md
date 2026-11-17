# CLAUDE.md

Shared instructions for the agent in this workspace. Adapt them to your team. Changes go through PRs.

## Workspace

- Always start the agent at the root of this workspace.
- `repositories/`: independent git repos, each with its own history and PR flow. Gitignored.
- `wiki/`: shared knowledge across repos. Read when needed.
- `.claude/skills/`: team skills. Repo-specific skills live in the repo itself; skills for all of DUT live in the marketplace.

## Team repos

If a repo is missing locally, clone it to its path. When several agents run at once, use a worktree in the repo.

| Repo | Path | Git | What |
|---|---|---|---|
| <name> | `repositories/<name>` | `git@github.com:jppol/<name>.git` | <one line> |

With many repos, group the table (frontend, backend, internal).

## Team agreements

To be filled in by the team. See `wiki/` for details.

- Reviewing AI code: <e.g. whoever opens the PR fully owns the code>
- Required before merge: <e.g. tests and green CI>
- PR size: <e.g. small PRs, atomic commits>

## Working rules

- Open new PRs as drafts.
- Keep history clean: atomic commits.
- Write short and to the point.
- No secrets in the workspace. The proxy injects them.
