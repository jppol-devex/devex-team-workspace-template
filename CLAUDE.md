# CLAUDE.md

Fælles instruktioner til agenten i dette workspace. Tilpas til jeres team. Ændringer går via PR.

## Workspace

- Start altid agenten i roden af dette workspace.
- `repositories/`: uafhængige git-repos med egen historik og eget PR-flow. Mappen er gitignored.
- `wiki/`: fælles viden på tværs af repos. Læs ved behov.
- `.claude/skills/`: team-skills. Repo-specifikke skills ligger i repoet selv, og skills for hele DUT ligger i marketplace.

## Teamets repos

Mangler et repo lokalt, så klon det til stien. Kør flere agenter, så brug en worktree i repoet.

| Repo | Sti | Git | Hvad |
|---|---|---|---|
| <navn> | `repositories/<navn>` | `git@github.com:jppol/<navn>.git` | <én linje> |

Ved mange repos: gruppér tabellen (frontend, backend, internt).

## Team-aftaler

Udfyldes af teamet. Se `wiki/` for detaljer.

- Review af AI-kode: <fx den, der åbner PR'en, ejer koden fuldt ud>
- Krav før merge: <fx tests og grøn CI>
- PR-størrelse: <fx små PR'er, atomare commits>

## Arbejdsregler

- Nye PR'er åbnes som drafts.
- Hold historikken ren: atomare commits.
- Skriv kort og præcist.
- Ingen secrets i workspace. Proxyen injicerer dem.
