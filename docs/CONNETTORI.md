# Connettori e fonti esterne

Equivalente IT di [CONNECTORS.md](https://github.com/anthropics/claude-for-legal/blob/main/CONNECTORS.md) nel repo Anthropic.

## Principio

Questo marketplace **non** incorpora testi di legge né database giuridici. Gli skill producono **bozze** con citazioni `[da verificare]` finché l'utente non verifica su fonti autorevoli.

## Fonti tipiche (configurate dallo studio)

| Tipo | Esempi | Uso |
| --- | --- | --- |
| Norme vigenti | Normattiva, EUR-Lex | Articoli, vigore, novelle |
| Giurisprudenza | Database abbonamento (DeJure, Lexis, …) | Cass., merito, TAR |
| Prassi | Garante privacy, Agenzia Entrate, CNF | Orientamenti |
| Atti mandato | PCT, fascicolo workspace | Fatto e strategia |

## MCP opzionale (futuro)

Vedi [MCP-OPZIONALE.md](MCP-OPZIONALE.md). Modello analogo a CourtListener (US): connettore configurato dall'utente verso DB **già licenziato** dallo studio.

Requisiti:

- Nessun scraping illegale di portali a pagamento
- Output MCP etichettato `[fonte: nome-tool]`
- Verifica umana prima di citare in atto o lettera

## Configurazione profilo

Path documentati (solo istruzioni):

```
~/.claude/plugins/config/pixari-italian-legal-skills/
  diritto-italiano-hub/CLAUDE.md
  privacy-gdpr/CLAUDE.md
  lavoro/CLAUDE.md
  diritto-civile/CLAUDE.md
  …/matters/<slug>/
```

Cold-start popola i `CLAUDE.md` nel workspace del progetto; la copia sotto config è opzionale per persistenza tra sessioni.

## Sicurezza

- Non inviare fascicoli clienti a connettori non approvati dal studio
- Valutare DPA con fornitore AI e sub-responsabili cloud
