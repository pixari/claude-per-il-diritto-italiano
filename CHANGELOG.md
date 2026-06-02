# Changelog

## [0.2.0] — 2026-06-02

### Added

- **privacy-gdpr:** 8 skill workflow (DSAR, DPA, DPIA, triage, violazione, gap, monitoraggio, cold-start); fascicolo `testatti/privacy-fittizio/`
- **lavoro:** 8 skill (revisione licenziamento, hiring, indagine, memo, fascicolo, cold-start); testatti licenziamento arricchiti
- **diritto-civile:** 7 skill (B2B, NDA, SaaS, cronologia, sintesi, cold-start); `testatti/nda-fittizio/`
- **diritto-italiano-hub:** `fascicolo-mandato`, `personalizzazione-playbook`; skill hub espansi
- **CI:** workflow `validate-plugins.yml`
- **CHANGELOG.md** e README plugin per verticale

### Changed

- Skill privacy rinominate: `risposta-diritti-interessato`, `revisione-dpa` (sostituiscono v0.1)
- `CLAUDE.md` per plugin con playbook esempio compilabile
- Marketplace e plugin version **0.2.0**

### Migration

| v0.1 | v0.2 |
| --- | --- |
| `/privacy-gdpr:bozza-risposta-esercizio-diritti` | `/privacy-gdpr:risposta-diritti-interessato` |
| `/privacy-gdpr:checklist-clausole-privacy-contratto` | `/privacy-gdpr:revisione-dpa` |

## [0.1.0] — 2026

- Marketplace iniziale: hub, civile, lavoro, privacy (2 skill ciascuno verticale)
- testatti licenziamento e contratto B2B
