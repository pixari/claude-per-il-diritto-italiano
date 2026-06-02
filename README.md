# Claude per il diritto italiano

> [!WARNING]
> **Skill sperimentali — non consulenza legale.** Ogni output è una **bozza** da verificare da un professionista abilitato. Il repository **non contiene testi di legge**. Leggi [AVVERTENZE.md](AVVERTENZE.md) prima di usare dati di mandato reali.

Skill e plugin per [Claude Code](https://docs.anthropic.com/en/docs/claude-code) orientati alla **pratica giuridica in Italia** (v**0.2**). Contenuti **originali in italiano**; architettura ispirata a [claude-for-legal](https://github.com/anthropics/claude-for-legal) e [claude-fuer-deutsches-recht](https://github.com/Klotzkette/claude-fuer-deutsches-recht).

Repository: [github.com/pixari/claude-per-il-diritto-italiano](https://github.com/pixari/claude-per-il-diritto-italiano)

## In sintesi

| Cosa | Dettaglio |
| --- | --- |
| **Cos’è** | Workflow multi-step (DSAR, contratti, licenziamenti, DPIA, …) via skill Markdown |
| **v0.2** | ~30 skill invocabili, playbook `CLAUDE.md`, fascicoli `testatti/` |
| **Cos’è un plugin** | Pacchetto installabile — comandi `/nome-plugin:nome-skill` |
| **Cos’è non** | Database legale, parere al cittadino, sostituto del giudice |
| **Fonti** | Verifica su abbonamenti, atti caricati, Normattiva/EUR-Lex — `[da verificare]` in bozza |

## Plugin e skill (v0.2)

| Plugin | Skill (principali) |
| --- | --- |
| `diritto-italiano-hub` | `cold-start-interview`, `metodo-giuridico`, `citazione-italiana`, `avvertenze-legali`, `fascicolo-mandato`, `personalizzazione-playbook`, `skills-qa` |
| `diritto-civile` | `cold-start-civile`, `revisione-contratto-b2b`, `revisione-nda`, `revisione-contratto-saas`, `subsunzione-civile`, `cronologia-contenzioso`, `sintesi-cliente-stakeholder` |
| `lavoro` | `cold-start-lavoro`, `revisione-licenziamento`, `checklist-licenziamento`, `hiring-review-lavoro`, `indagine-interna-disciplinare`, `qa-rapida-lavoro`, `bozza-memo-disciplinare`, `fascicolo-lavoro` |
| `privacy-gdpr` | `cold-start-privacy`, `risposta-diritti-interessato`, `revisione-dpa`, `triage-trattamento`, `generazione-dpia`, `violazione-dati`, `gap-normativo-privacy`, `monitoraggio-informativa` |

Dettaglio per plugin: README in ogni cartella (`privacy-gdpr/README.md`, …).

## Installazione

```text
/plugin marketplace add pixari/claude-per-il-diritto-italiano
/plugin install diritto-italiano-hub@pixari-italian-legal-skills
/plugin install diritto-civile@pixari-italian-legal-skills
/plugin install lavoro@pixari-italian-legal-skills
/plugin install privacy-gdpr@pixari-italian-legal-skills
```

Poi **skill**, non plugin: `/diritto-italiano-hub:metodo-giuridico` — vedi [TROUBLESHOOTING.md](TROUBLESHOOTING.md).

## Avvio rapido

1. `/diritto-italiano-hub:avvertenze-legali`
2. `/diritto-italiano-hub:cold-start-interview`
3. Cold-start verticali: `cold-start-privacy`, `cold-start-lavoro`, `cold-start-civile`
4. Prova fascicoli in [`testatti/`](testatti/) — vedi [QUICKSTART.md](QUICKSTART.md)

## Migrazione da v0.1

| v0.1 | v0.2 |
| --- | --- |
| `bozza-risposta-esercizio-diritti` | `risposta-diritti-interessato` |
| `checklist-clausole-privacy-contratto` | `revisione-dpa` |

Vedi [CHANGELOG.md](CHANGELOG.md).

## Contribuire

[CONTRIBUTING.md](CONTRIBUTING.md) — skill workflow nuovi: minimo **100 righe**, disclaimer, test su `testatti/`.

## Licenza

[MIT](LICENSE) — [NOTICE](NOTICE).
