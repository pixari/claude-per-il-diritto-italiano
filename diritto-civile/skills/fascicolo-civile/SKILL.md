---
name: fascicolo-civile
description: >
  Matter workspace civile: contratti, negoziazione, pre-contenzioso. Collega
  contenzioso-civile se lite. Nessuna consulenza legale.
argument-hint: "[slug] [tipo: contratto|negoziazione|precontenzioso]"
---

# Fascicolo civile (matter workspace)

> **Bozza — non consulenza legale.**

## Path

- `matters/<slug>/` nel workspace
- Doc: `~/.claude/plugins/config/pixari-italian-legal-skills/diritto-civile/matters/<slug>/`

## Intake

| Campo | Valore |
| --- | --- |
| Slug | `civile_<cliente_codice>_<oggetto>` |
| Tipo | contratto / negoziazione / precontenzioso |
| Ruolo cliente | committente / prestatore / attore / convenuto |
| Foro / legge applicabile | da `CLAUDE.md` |

## Struttura

```
matters/<slug>/
  matter.md
  contratti/
  negoziazione/
  bozze/
  cronologia.md      # o link contenzioso-civile
```

## Skill per tipo

| Tipo | Skill |
| --- | --- |
| B2B / SaaS / NDA | `revisione-contratto-b2b`, `revisione-nda`, `revisione-contratto-saas` |
| Fornitore | `revisione-fornitore` |
| Amendment | `storico-amendment` |
| Lite contenzioso | `cronologia-contenzioso` → poi `/contenzioso-civile:*` se lite |
| Sintesi | `sintesi-cliente-stakeholder` |

## Se diventa contenzioso

Migrare o collegare slug a `/contenzioso-civile:fascicolo-contenzioso`.

## Divieti

- Segreti commerciali non in repo git
