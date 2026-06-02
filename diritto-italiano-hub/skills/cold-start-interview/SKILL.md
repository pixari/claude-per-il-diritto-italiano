---
name: cold-start-interview
description: Intervista cold-start per compilare il profilo studio in CLAUDE.md (materie, riti, citazioni, strumenti). Usare alla prima configurazione o quando cambia organizzazione. Nessuna consulenza legale.
argument-hint: "[opzionale: path al CLAUDE.md da aggiornare]"
---

# Cold-start — profilo studio

## Obbligatorio

Output di configurazione, non consulenza. Alla fine ricordare avvertenze (`/diritto-italiano-hub:avvertenze-legali`).

## Intervista (chiedi in sequenza, adatta se l'utente ha già risposto)

1. **Organizzazione** — studio, legale interno, altro?
2. **Materie** — civile, lavoro, privacy, amministrativo, altro?
3. **Riti frequenti** — civile ordinario, lavoro, cautelare, esecutivo, amministrativo?
4. **Stile citazione** — Cass. con estremi; preferenza G.U./database?
5. **Playbook** — esiste documento interno (path sintetico, senza segreti)?
6. **Escalation** — quando coinvolgere socio/DPO?
7. **Strumenti** — database giuridici, PCT/gestionale (solo nomi, no password)?

## Output

Aggiorna `diritto-italiano-hub/CLAUDE.md` (o path indicato) con le risposte, sezioni:

- Identità
- Stile e fonti
- Calibrazione rischio
- Strumenti

Conferma all'utente che il profilo è **bozza di configurazione** e va rivisto periodicamente.
