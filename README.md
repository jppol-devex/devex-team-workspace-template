# Team workspace template

Skabelon til et team-workspace, som Claude Code (og andre agenter) kan arbejde i.
Bygger på anbefalingen fra DevEx' team-udrulning ("Jeres workspace").

## Struktur

| Sti | Formål |
|---|---|
| `repositories/` | Uafhængige git-repos, ét pr. projekt (klones hertil, ikke committet her) |
| `documentation/` | Fælles dokumentation og noter |
| `CLAUDE.md` | Instruktioner til agenten, fælles for teamet |

## Kom i gang

1. Brug "Use this template" på GitHub, eller klon og fjern `.git`.
2. Tilpas `CLAUDE.md` til jeres team.
3. Klon jeres repos ind i `repositories/`.
4. Installer skills: `/plugin marketplace add <marketplace-repo>` og `/plugin install <skill>@<marketplace>`.

## Status

Under udvikling. Tanken er at udvide med mere end skelettet (skills, konventioner, eksempler).
