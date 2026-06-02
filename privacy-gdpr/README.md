# privacy-gdpr

Plugin per legale interno, DPO e studi: DSAR, DPA, DPIA, violazioni, gap e policy. **Ogni output è bozza** — revisione DPO/legale obbligatoria.

## Per chi è

| Ruolo | Workflow principali |
| --- | --- |
| DPO / privacy officer | DSAR, DPIA, violazioni, gap |
| Legale interno | Revisione DPA, triage trattamenti |
| Studio esterno | Risposta diritti, supporto committente titolare |

## Prima esecuzione

```
/privacy-gdpr:cold-start-privacy
```

Compila `CLAUDE.md` (sistemi, processo DSAR, playbook DPA). La configurazione resta nel progetto.

## Prerequisiti

- Fonti aggiornate (Garante, EUR-Lex/Normattiva) — il plugin **non** incorpora testi di legge
- Registro trattamenti e policy reali da caricare in sessione
- Per trasferimenti extra-SEE: documentazione SCC/TIA `[da verificare]`

## Skill

| Skill | Comando |
| --- | --- |
| Cold-start profilo | `/privacy-gdpr:cold-start-privacy` |
| Risposta diritti interessato | `/privacy-gdpr:risposta-diritti-interessato` |
| Revisione DPA | `/privacy-gdpr:revisione-dpa` |
| Triage nuovo trattamento | `/privacy-gdpr:triage-trattamento` |
| Bozza DPIA | `/privacy-gdpr:generazione-dpia` |
| Violazione dati | `/privacy-gdpr:violazione-dati` |
| Gap documentazione | `/privacy-gdpr:gap-normativo-privacy` |
| Revisione informativa | `/privacy-gdpr:monitoraggio-informativa` |
| Fascicolo matter | `/privacy-gdpr:fascicolo-privacy` |
| Personalizza playbook | `/privacy-gdpr:personalizzazione-privacy` |

## Test (fittizi)

Cartella [`testatti/privacy-fittizio/`](../testatti/privacy-fittizio/) — DSAR, DPA, nota violazione.

## Migrazione da v0.1

| v0.1 | v0.2 |
| --- | --- |
| `bozza-risposta-esercizio-diritti` | `risposta-diritti-interessato` |
| `checklist-clausole-privacy-contratto` | `revisione-dpa` |
