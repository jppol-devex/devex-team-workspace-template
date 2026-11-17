# Team workspace template

Template for a team workspace (a "home repo"): the place the team's agent is always started from.
From here the agent works across the team's other repos, with the same skills, settings and agreements for everyone.
Based on the recommendation from DevEx' team rollout ("Your workspace").

## Structure

| Path | Purpose |
|---|---|
| `CLAUDE.md` | Map of the team's repos and team agreements |
| `.claude/skills/` | Team skills (across the team's repos) |
| `.claude/settings.json` | Shared, versioned Claude Code settings |
| `wiki/` | Shared knowledge and notes |
| `repositories/` | The team's repos, cloned in as needed (gitignored) |

## Getting started

1. Use "Use this template" on GitHub.
2. Fill in "Team repos" and "Team agreements" in `CLAUDE.md`.
3. Start the agent at the root of the workspace. It clones the repos it is missing.

## Why not git submodules?

Submodules pin a commit, so the workspace needs a new commit every time a repo changes.
They cause detached HEADs, work poorly with worktrees, and everyone has to fetch every repo.
What is shared is the repo list in `CLAUDE.md`. Each person clones only what they work on.

## Where does a skill belong?

| Level | Location |
|---|---|
| Personal | `~/.claude/skills` |
| Repo | `.claude/skills` in the repo itself |
| Team | `.claude/skills` here |
| DUT | jppol-skills-marketplace |

Start low, and move a skill up when more than one person needs it.
