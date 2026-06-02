---
name: personalizzazione-privacy
description: >
  Aggiorna privacy-gdpr/CLAUDE.md da feedback (DSAR, DPA, sistemi, red lines).
  Equivalente EN customize. Nessuna consulenza legale.
argument-hint: "[modifica: es. SLA 20gg, nuovo CRM]"
---

# Personalizzazione playbook privacy

> **Bozza — non consulenza legale.**

## File target

[`privacy-gdpr/CLAUDE.md`](../../CLAUDE.md)

## Sezioni modificabili

- Ruoli e contatti / DPO
- Registro sistemi (DSAR)
- Processo DSAR (verifica, SLA, approvatori)
- Playbook DPA (red lines, trasferimenti)
- Escalation

## Processo

1. Leggi file completo
2. Applica solo modifiche richieste dall'utente
3. Aggiungi `Ultimo aggiornamento: YYYY-MM-DD`
4. Suggerisci `/privacy-gdpr:cold-start-privacy` se mancano sistemi

## Esempi richieste

| Input utente | Sezione |
| --- | --- |
| Nuovo sub-responsabile cloud | Registro sistemi + Playbook DPA |
| SLA 15 giorni | Processo DSAR |
| Red line audit illimitato | Playbook DPA |

## Output

- Diff per sezione
- Reminder: rieseguire `fascicolo-privacy` su matter aperti se processo cambia

## Divieti

- Non inserire dati interessati reali
