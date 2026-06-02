---
name: skills-qa
description: Checklist qualità per nuovi o modificati SKILL.md (diritto italiano, disclaimer, citazioni, rito). Usare prima di PR o release. Nessuna consulenza legale.
user-invocable: true
---

# QA skill — checklist

## Obbligatorio in ogni skill

- [ ] Frontmatter `name` e `description` (description ≤ 1024 char, contiene "Nessuna consulenza legale" o equivalente)
- [ ] Box disclaimer bozza all'inizio del corpo
- [ ] Nessun testo che prometta parere vincolante o consulenza al pubblico

## Diritto italiano

- [ ] Riferimenti a c.c., c.p.c., d.lgs., l. — non BGB/US brief
- [ ] Rito indicato se rilevante (civile, lavoro, cautelare, …)
- [ ] Citazioni con estremi + vigore + `[da verificare]` dove serve
- [ ] No numeri di sentenza inventati

## Contributi

- [ ] Esempi fittizi; no mandati reali in repo/Issue/PR
- [ ] Coerenza con `AVVERTENZE.md` e NOTICE

## Test

- [ ] Prova su fascicolo in `testatti/` se applicabile
- [ ] Output inizia con disclaimer bozza

Segnala esito: **OK** / **da correggere** con elenco punti.
