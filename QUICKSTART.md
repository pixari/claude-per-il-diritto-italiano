# Quickstart v0.2

Prima installazione e **tre prove** (~30 minuti) con dati **solo fittizi**.

## Installazione

```text
/plugin marketplace add pixari/claude-per-il-diritto-italiano
/plugin install diritto-italiano-hub@pixari-italian-legal-skills
/plugin install diritto-civile@pixari-italian-legal-skills
/plugin install lavoro@pixari-italian-legal-skills
/plugin install privacy-gdpr@pixari-italian-legal-skills
```

Errore `not found`? → [TROUBLESHOOTING.md](TROUBLESHOOTING.md) (installare **plugin**, invocare **skill**).

## Configurazione (10 min)

```text
/diritto-italiano-hub:avvertenze-legali
/diritto-italiano-hub:cold-start-interview
/privacy-gdpr:cold-start-privacy
/lavoro:cold-start-lavoro
/diritto-civile:cold-start-civile
```

## Percorso 1 — Privacy (~10 min)

1. Apri `testatti/privacy-fittizio/01_richiesta_accesso_DSAR.md`
2. Esegui:

```text
/privacy-gdpr:risposta-diritti-interessato
```

3. Prova `02_bozza_DPA_commessa.md` con `/privacy-gdpr:revisione-dpa`
4. Verifica: disclaimer, `[da verificare]`, nessuna sentenza inventata

## Percorso 2 — Lavoro (~10 min)

1. Apri `testatti/licenziamento-fittizio/`
2. Esegui:

```text
/lavoro:revisione-licenziamento
```

(incolla fatti da `01_timeline_fatti.md` e lettera `02_lettera_licenziamento.md`)
3. Opzionale: `/lavoro:indagine-interna-disciplinare` con `04_verbale_audizione.md`

## Percorso 3 — Civile (~10 min)

1. Apri `testatti/contratto-b2b-fittizio/`
2. Esegui:

```text
/diritto-civile:revisione-contratto-b2b
```

ruolo committente
3. Opzionale NDA: `testatti/nda-fittizio/` + `/diritto-civile:revisione-nda`

## Comandi utili

| Comando | Uso |
| --- | --- |
| `/diritto-italiano-hub:fascicolo-mandato` | Struttura cartella mandato |
| `/diritto-italiano-hub:metodo-giuridico` | Analisi strutturata |
| `/privacy-gdpr:triage-trattamento` | Nuovo trattamento dati |
| `/diritto-italiano-hub:skills-qa` | Checklist prima di PR |

## Prossimi passi

- [AVVERTENZE.md](AVVERTENZE.md) prima di mandati reali
- [CONTRIBUTING.md](CONTRIBUTING.md)
- [CHANGELOG.md](CHANGELOG.md)
