---
name: metodo-giuridico
description: Applica il metodo giuridico italiano (qualificazione, norma, subsunzione, conclusione) per atti di parte, pareri interni o note al cliente. Usare per analisi civile, lavoro, privacy. Diritto italiano only; no US common law. Nessuna consulenza legale.
argument-hint: "[tipo: atto|parere|nota-cliente] [quesito o fatto sintetico]"
---

# Metodo giuridico (Italia)

## Obbligatorio

1. Leggi `CLAUDE.md` del profilo studio se presente.
2. Dichiara **rito** e **tipo documento** richiesto.
3. Apri con disclaimer bozza (vedi `avvertenze-legali`).

## Evitare

- Struttura "brief" US, BGB/tedesco copiato senza adattamento.
- Conclusioni come sentenza o parere definitivo.

## Workflow

### 1. Qualificazione

- Fatto rilevante e quesito.
- Confini del mandato e dati mancanti (elenca domande all'utente).

### 2. Norma

- Individua fonti: Costituzione, legge, d.lgs., regolamento UE, contratto.
- Gerarchia: promemoria su specialità, posteriorità, costituzionalità — **non** decidere conflitti in autonomia.
- Per ogni norma: estremi + **data di vigore** + `[da verificare]` se non da fonte live.

### 3. Subsunzione

Per ogni elemento:

- Fatto provato / da provare
- Applicazione norma
- Controargomenti

### 4. Conclusione (bozza)

- Proposta operativa chiara.
- Rischi e passi successivi (verifica fonti, deposito PCT, ecc.).

## Formati output

| Tipo | Struttura |
| --- | --- |
| **Atto di parte** | Intestazione, in fatto, in diritto, conclusioni/petitum; eccezioni preliminari se il rito lo prevede |
| **Parere interno** | Quesito, fatto, diritto, rischio, opzioni |
| **Nota cliente** | Linguaggio accessibile, stesso disclaimer |

Non fornire consulenza al cittadino senza avvocato.
