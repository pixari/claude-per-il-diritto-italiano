# Profilo — privacy / GDPR

> Compilare con `/privacy-gdpr:cold-start-privacy`. Valori di esempio sotto sono **fittizi** per test.

## Ruoli e contatti

- Titolare principale: Alfa S.r.l. (committente servizi digitali)
- DPO: dpo@alfa-fittizio.example (esterno)
- Legale privacy: studio associato — `[da verificare]` contatto reale

## Registro sistemi (DSAR)

| Sistema | Ruolo | Categorie dati | Query DSAR |
| --- | --- | --- | --- |
| CRM (cloud EU) | Responsabile | Clienti B2B, lead | Export ticket + API |
| HR (on-prem) | Titolare | Dipendenti, candidati | HR + DPO |
| Sito web / analytics | Titolare/Resp. misto | Visitatori, cookie | Marketing + IT |
| Email aziendale | Titolare | Comunicazioni | Ricerca limitata retention |
| Backup | Responsabile interno | Snapshot | Solo se policy prevede |

## Processo DSAR

- **Canale:** privacy@alfa-fittizio.example e PEC privacy@pec.alfa-fittizio.example
- **Verifica identità:** email da anagrafica CRM; per cancellazione → documento ID
- **SLA interno:** 25 giorni lavorativi (confrontare art. 12 GDPR `[da verificare]`)
- **Approvatori:** DPO prima invio; legale se rifiuto parziale o dati particolari

## Playbook DPA

- Template: `skills/revisione-dpa/references/` + allegato standard commessa
- **Red lines:** audit on-site illimitato; trasferimenti USA senza SCC 2021; sub-responsabile libero senza lista
- **Trasferimenti accettati:** SEE + SCC UE modulo 2021 con TIA documentata `[da verificare]`

## Escalation

- Minori, dati sanitari, larga scala → legale + DPO entro 24h
- Violazioni → `/privacy-gdpr:violazione-dati` + IT incident response
- Contenzioso o conservazione per legge → non cancellare senza parere legale

## Fonti verifica

- Garante per la protezione dei dati personali — garanteprivacy.it `[da verificare]`
- Reg. UE 2016/679, d.lgs. 196/2003 — Normattiva / EUR-Lex su testo vigente
- Linee WP29/EDPB — `[da verificare]` per DPIA e trasferimenti

## Note operative

- Output sempre **bozza**; non inviare risposte DSAR senza revisione
- Citazioni normative non verificate: `[da verificare]`
- Fascicoli test: `testatti/privacy-fittizio/`
