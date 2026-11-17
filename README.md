# Team workspace template

Skabelon til et team-workspace (et "home repo"): det sted, teamets agent altid startes fra.
Herfra arbejder agenten ud i teamets øvrige repos, med de samme skills, settings og aftaler for alle.
Bygger på anbefalingen fra DevEx' team-udrulning ("Jeres workspace").

## Struktur

| Sti | Formål |
|---|---|
| `CLAUDE.md` | Landkort til teamets repos og team-aftaler |
| `.claude/skills/` | Team-skills (på tværs af teamets repos) |
| `.claude/settings.json` | Fælles, versionerede Claude Code-settings |
| `wiki/` | Fælles viden og noter |
| `repositories/` | Teamets repos, klonet ind efter behov (gitignored) |

## Kom i gang

1. Brug "Use this template" på GitHub.
2. Udfyld "Teamets repos" og "Team-aftaler" i `CLAUDE.md`.
3. Start agenten i roden af workspace. Den kloner de repos, den mangler.

## Hvorfor ikke git submodules?

Submodules låser til et commit, så workspace skal have et nyt commit, hver gang et repo ændrer sig.
De giver detached HEAD og spiller dårligt sammen med worktrees, og alle skal hente alle repos.
Det fælles er listen over repos i `CLAUDE.md`. Hver person kloner kun det, hen arbejder i.

## Hvor hører en skill hjemme?

| Niveau | Sted |
|---|---|
| Personlig | `~/.claude/skills` |
| Repo | `.claude/skills` i repoet selv |
| Team | `.claude/skills` her |
| DUT | jppol-skills-marketplace |

Start lavt, og flyt en skill op, når mere end én har brug for den.
