# Quickstart

Guida rapida per la **prima installazione** e una prova in circa 10 minuti (solo dati fittizi).

## Prerequisiti

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installato e funzionante
- Account Anthropic (o provider compatibile configurato da te)

## Installazione

### Claude Code (marketplace)

```text
/plugin marketplace add pixari/claude-per-il-diritto-italiano
/plugin install diritto-italiano-hub@pixari-italian-legal-skills
/plugin install diritto-civile@pixari-italian-legal-skills
/plugin install lavoro@pixari-italian-legal-skills
/plugin install privacy-gdpr@pixari-italian-legal-skills
```

Verifica che i plugin compaiano in `/plugin list` o nell’interfaccia plugin.

**Attenzione:** `metodo-giuridico`, `checklist-licenziamento`, ecc. sono **skill**, non plugin.  
Installa `diritto-italiano-hub@pixari-italian-legal-skills`, poi invoca `/diritto-italiano-hub:metodo-giuridico`.  
Se vedi `not found`, leggi [TROUBLESHOOTING.md](TROUBLESHOOTING.md).

### Claude Cowork / Desktop (ZIP)

1. Clona questo repository o scarica una release ZIP.
2. Comprimi una cartella plugin (es. `lavoro/`) se l’interfaccia richiede un singolo plugin per file.
3. In *Customize → Plugins / Skills*, carica lo ZIP.
4. Ripeti per `diritto-italiano-hub` (consigliato per primo).

## Configurazione profilo (5 minuti)

```text
/diritto-italiano-hub:avvertenze-legali
/diritto-italiano-hub:cold-start-interview
```

Rispondi alle domande; verrà aggiornato `diritto-italiano-hub/CLAUDE.md` nel workspace.

## Prova in 10 minuti — fascicolo fittizio

1. Apri la cartella [`testatti/licenziamento-fittizio/`](testatti/licenziamento-fittizio/) nel workspace.
2. Leggi `README.txt` nel fascicolo (personaggi inventati).
3. Esegui:

```text
/lavoro:checklist-licenziamento
```

Incolla o riassumi i fatti dal file `01_timeline_fatti.md` (solo dati fittizi).

4. Controlla che l’output:
   - Inizi con **bozza / non consulenza**
   - Usi `[da verificare]` sulle norme non verificate live
   - Non inventi sentenze con numero preciso

### Prova civile (opzionale)

```text
/diritto-civile:revisione-contratto-b2b
```

Usa i file in `testatti/contratto-b2b-fittizio/`.

## Comandi utili

| Comando | Uso |
| --- | --- |
| `/diritto-italiano-hub:metodo-giuridico` | Analisi strutturata |
| `/diritto-italiano-hub:citazione-italiana` | Regole citazione |
| `/diritto-italiano-hub:skills-qa` | Checklist prima di una PR |

## Prossimi passi

- Leggi [AVVERTENZE.md](AVVERTENZE.md) prima di usare documenti di mandato reali.
- Contribuisci con [CONTRIBUTING.md](CONTRIBUTING.md).
