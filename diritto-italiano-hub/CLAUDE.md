# Profilo studio — hub (esempio compilabile)

> Sostituire con `/diritto-italiano-hub:cold-start-interview`. Valori sotto **fittizi**.

## Identità

- Organizzazione: Studio Rossi & Associati (fittizio)
- Utenti tipici: 4 soci, 12 associate, legale interno M&A clienti
- Lingua: italiano tecnico; note cliente in tono semplice

## Materie e riti

| Materia | Rito | Priorità |
| --- | --- | --- |
| Civile contratti | Ordinario / mediazione | Alta |
| Lavoro contenzioso | Giudizio del lavoro | Media |
| Privacy committenti | Amministrativo/Garante | Media |
| Amministrativo | TAR `[da verificare]` | Bassa (escalation) |

## Stile citazioni e fonti

- Cass.: estremi completi o `[da verificare]`
- Database: DeJure (nome solo, no credenziali in file)
- UE: EUR-Lex per regolamenti

## Playbook e red lines

- Contratti: penale >25% fee annua → escalation socio
- Licenziamenti art. 18 → sempre socio
- DSAR con dati sanitari → DPO entro 24h

## Escalation

| Trigger | Azione |
| --- | --- |
| Sanzioni penali | Penalista esterno |
| Class action / gruppo | Comitato soci |
| AI output su mandato reale | Revisione umana obbligatoria |

## Strumenti

- Fascicoli: cartelle locali + `/diritto-italiano-hub:fascicolo-mandato`
- Test: `testatti/` only

## Plugin collegati

- `privacy-gdpr`, `lavoro`, `diritto-civile` — cold-start verticali se materia attiva

## Note sessione

- Ultimo aggiornamento playbook: (data cold-start)
- v0.2 marketplace
