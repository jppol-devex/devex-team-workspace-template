# Team workspace template

Template for a team workspace (a "home repo"): the place the team's agent is always started from.
From here the agent works across the team's other repos, with the same skills, settings and agreements for everyone.
Based on the recommendation from DevEx' team rollout ("Your workspace").

## Structure

| Path | Purpose |
|---|---|
| `CLAUDE.md` | Agent instructions: repo map and rules |
| `.claude/settings.json` | Shared settings, including which marketplace skills the team uses |
| `wiki/` | Shared knowledge and notes |
| `repositories/` | The team's repos, cloned in as needed (gitignored) |

## Getting started

1. Use "Use this template" on GitHub.
2. Add your repos to `CLAUDE.md`, plus any team agreements the agent must follow (review, tests, PR size). Keep it short: it loads into every session.
3. Enable your team's skills in `enabledPlugins` in `.claude/settings.json` as `<skill>@litellm`. The sandbox registers the LiteLLM skills gateway as the `litellm` marketplace; browse it with `/plugin`.
4. Start the agent at the root of the workspace. It clones the repos it is missing.

## How repos are shared

`repositories/` is gitignored. Each repo keeps its own history and PRs.
The repo table in `CLAUDE.md` is what the team shares: the agent clones any repo it needs, so each person only has what they work on.

## Where does a skill belong?

| Level | Location |
|---|---|
| Personal | `~/.claude/skills` |
| Repo | `.claude/skills` in the repo itself |
| Team and DUT | jppol-skills-marketplace, served by the LiteLLM skills gateway and enabled in `.claude/settings.json` here |

Team skills live in the marketplace, so every team can find and reuse them.
Start low, and move a skill up when more than one person needs it.
