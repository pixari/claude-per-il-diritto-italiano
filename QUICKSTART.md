# Quickstart (v0.6)

## Install

```text
/plugin marketplace add pixari/claude-per-il-diritto-italiano
/plugin install diritto-italiano-hub@pixari-italian-legal-skills
/plugin install privacy-gdpr@pixari-italian-legal-skills
/plugin install lavoro@pixari-italian-legal-skills
/plugin install diritto-civile@pixari-italian-legal-skills
/plugin install contenzioso-civile@pixari-italian-legal-skills
```

(opzionale: `societario`, `amministrativo`, `prodotto-servizi`)

## Setup EN-style (15 min)

```text
/diritto-italiano-hub:avvertenze-legali
/diritto-italiano-hub:cold-start-interview
/privacy-gdpr:cold-start-privacy
/privacy-gdpr:fascicolo-privacy dsar-test-2026 dsar
```

## Percorsi test

| Materia | Testatto | Matter + workflow |
| --- | --- | --- |
| Privacy | `testatti/privacy-fittizio/` | `fascicolo-privacy` → `risposta-diritti-interessato` |
| Lavoro | `testatti/licenziamento-fittizio/` | `fascicolo-lavoro` → `revisione-licenziamento` |
| Civile | `testatti/contratto-b2b-fittizio/` | `fascicolo-civile` → `revisione-contratto-b2b` |
| Contenzioso | `testatti/contenzioso-fittizio/` | `fascicolo-contenzioso` → `bozza-diffida` |
| Societario | `testatti/assemblea-fittizia/` | `verbale-assemblea-bozza` |
| Amministrativo | `testatti/ricorso-tar-fittizio/` | `ricorso-tar-bozza` |

## Verifica output

- Disclaimer bozza in testa
- `[da verificare]` su norme non da fonte live
- Nessuna sentenza inventata

Vedi [docs/CONNETTORI.md](docs/CONNETTORI.md).
