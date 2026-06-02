---
name: storico-amendment
description: >
  Ricostruisce storico amendment / versioni contratto, conflitti tra allegati.
  EN amendment-history. Nessuna consulenza legale.
argument-hint: "[elenco file: v1, v2, amendamenti]"
---

# Storico amendment contratto

> **Bozza — non consulenza legale.**

## Input

- Versioni contratto (date, autore bozza)
- Email/PEC negoziazione
- Ordine di precedenza clausole

## Workflow

1. Timeline versioni (tabella data / file / modifiche principali)
2. Matrice diff concettuale (non sostituisce diff legale automatizzato cieco)
3. **Conflitti** tra clausola master e allegato successivo
4. Clausole ancora vigenti vs superate
5. Raccomandazione: quale versione firmare / integrare

## Output

`storico_amendment_<nome>.md` + elenco punti aperti negoziazione.

## Collegamento

`/diritto-civile:fascicolo-civile` per matter strutturato.

## Divieti

- Non inventare versioni non fornite
