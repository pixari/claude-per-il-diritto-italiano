# Come contribuire

Grazie per l’interesse in **Claude per il diritto italiano**. Le contribuzioni migliorano workflow reali in studio — e **non richiedono** necessariamente competenze di programmazione.

## Prima di iniziare

1. Leggi [AVVERTENZE.md](AVVERTENZE.md).
2. **Non** inserire dati reali di clienti in Issue, PR o file nel repository.
3. Rispetta il segreto professionale e le policy del tuo studio.

## Chi può contribuire cosa

| Profilo | Contributo tipico |
| --- | --- |
| **Avvocato / legale** | Testi in `SKILL.md`, checklist, correzioni metodo/citazione |
| **Praticante / studente** | Test su `testatti/`, chiarezza espositiva (no consegne universitarie come output del plugin) |
| **Consulente del lavoro** | Plugin `lavoro` |
| **Sviluppatore** | Marketplace, struttura plugin, [MCP](docs/MCP-OPZIONALE.md) |

## Senza scrivere codice

### Migliorare uno skill esistente

1. Apri `skills/<nome>/SKILL.md` nel plugin (es. `lavoro/skills/checklist-licenziamento/SKILL.md`).
2. Modifica istruzioni, checklist, esempi (**solo fittizi**).
3. Apri una Pull Request (vedi sotto).

### Creare un nuovo skill

1. Copia `diritto-italiano-hub/skills/skill-template/SKILL.md` in `skills/<nuovo-nome>/SKILL.md` del plugin adatto.
2. Compila il frontmatter:
   - `name`: identificatore breve
   - `description`: massimo **1024 caratteri**, includere *Nessuna consulenza legale*
   - `argument-hint`: opzionale
3. Esegui mentalmente `/diritto-italiano-hub:skills-qa` sulla bozza.
4. PR con titolo: `[area] Aggiunge skill …`

### Segnalare un problema

Usa i template Issue:

- **bug-skill** — comportamento errato dello skill
- **miglioramento-giuridico** — metodo, riferimento normativo, rito
- **nuova-area** — nuovo plugin o materia (civile, amministrativo, …)

## Pull Request — passi

1. **Fork** del repository.
2. **Branch** descrittivo: `lavoro-migliora-checklist-licenziamento`.
3. **Un focus** per PR (un skill o un README, non tutto insieme alla prima contribuzione).
4. Descrizione PR:
   - Area del diritto
   - Tipo: nuovo skill / correzione / documentazione
   - Test effettuato (es. fascicolo `testatti/licenziamento-fittizio/`)
5. Checklist PR (nel template): disclaimer presente, nessun dato cliente, citazioni con `[da verificare]` dove serve.

Le PR su materia giuridica possono richiedere tempo per review — nessuna urgenza imposta.

## Standard qualità (diritto italiano)

- Indica **rito** e **tipo atto** quando rilevante (comparsa, ricorso, parere interno).
- Metodo: qualificazione → norma (gerarchia fonti) → subsunzione → conclusione (**bozza**).
- Citazioni: estremi italiani (Cass., d.lgs., art. c.c.); data di vigore; **no sentenze inventate**.
- Segnala diritto UE o costituzionale senza “risolvere” il conflitto in autonomia.
- Box disclaimer in ogni skill; output sempre bozza.
- Esempi solo fittizi o da [`testatti/`](testatti/).

## Codice di condotta

- Rispetto e costruttività.
- Niente consulenza legale mascherata da prodotto finito.
- Niente dati personali identificabili.

## Sviluppatori — struttura plugin

```
<plugin>/
  .claude-plugin/plugin.json
  CLAUDE.md
  skills/<skill-name>/SKILL.md
```

Registra nuovi plugin in [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json).

## Domande

Apri una Issue con etichetta `question` o attiva Discussions se disponibile sul repository.
