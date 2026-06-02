# Claude per il diritto italiano

> [!WARNING]
> **Esperimento open source — non consulenza legale.** Ogni output è una **bozza** da verificare da un professionista abilitato. Il repository **non contiene testi di legge**. Leggi [AVVERTENZE.md](AVVERTENZE.md) prima di usare dati di mandato reali.

Skill e plugin per [Claude Code](https://docs.anthropic.com/en/docs/claude-code) (e, con ZIP, Claude Cowork/Desktop) orientati alla **pratica giuridica in Italia**: metodo, citazioni, civile, lavoro, privacy/GDPR. Contenuti **originali in italiano**; architettura ispirata a [claude-for-legal](https://github.com/anthropics/claude-for-legal) e [claude-fuer-deutsches-recht](https://github.com/Klotzkette/claude-fuer-deutsches-recht).

Repository: [github.com/pixari/claude-per-il-diritto-italiano](https://github.com/pixari/claude-per-il-diritto-italiano)

## In sintesi

| Cosa | Dettaglio |
| --- | --- |
| **Cos’è** | Istruzioni (skill) che guidano Claude su workflow da studio — contratti, subsunzione, lavoro, GDPR |
| **Cos’è un plugin** | Pacchetto installabile con più skill e comandi `/nome-plugin:nome-skill` |
| **Cosa non è** | Database legale, parere online al cittadino, sostituto del giudice |
| **Fonti** | Le verifichi tu su abbonamenti, atti caricati, database dello studio |

## A chi serve

| Profilo | Uso tipico | Come contribuire |
| --- | --- | --- |
| **Avvocato** | Bozze atti, checklist, revisione contratti | Modifica `SKILL.md`, apri PR |
| **Praticante** | Metodo, esercitazione supervisionata | Testa `testatti/`, Issue con feedback |
| **Legale interno / DPO** | Privacy, contratti | Plugin `privacy-gdpr` |
| **Consulente del lavoro** | Licenziamenti, Q&A | Plugin `lavoro` |
| **Sviluppatore** | Marketplace, integrazioni | Plugin structure, [MCP opzionale](docs/MCP-OPZIONALE.md) |

**Non è pensato per:** consulenza diretta al pubblico senza avvocato; attività del PM o del giudice.

## Cosa trovi qui

| Cartella / plugin | Contenuto |
| --- | --- |
| `diritto-italiano-hub` | Metodo, citazione, avvertenze, profilo studio, template skill |
| `diritto-civile` | Subsunzione, revisione contratto B2B |
| `lavoro` | Checklist licenziamento, Q&A rapida |
| `privacy-gdpr` | Risposta interessato, checklist clausole privacy |
| [`testatti/`](testatti/) | Mandati **fittizi** per provare i workflow |

## Installazione rapida

1. Installa [Claude Code](https://docs.anthropic.com/en/docs/claude-code).
2. Nel progetto o globalmente, aggiungi il marketplace:

```text
/plugin marketplace add pixari/claude-per-il-diritto-italiano
```

3. Installa hub + plugin di interesse:

```text
/plugin install diritto-italiano-hub@pixari-italian-legal-skills
/plugin install diritto-civile@pixari-italian-legal-skills
/plugin install lavoro@pixari-italian-legal-skills
/plugin install privacy-gdpr@pixari-italian-legal-skills
```

4. Configura il profilo: `/diritto-italiano-hub:cold-start-interview`
5. Leggi [QUICKSTART.md](QUICKSTART.md) e prova un fascicolo in `testatti/`.

**Claude Cowork / Desktop:** scarica o crea uno ZIP del plugin e caricalo da *Customize → Plugins* (vedi QUICKSTART).

## Esempio d’uso

```text
/lavoro:qa-rapida-lavoro qual è il termine per impugnare un licenziamento individuale? (verifica le date)
```

L’output inizia con l’avviso **bozza / non consulenza** e marca le citazioni non verificate con `[da verificare]`.

## Contribuire

**Non serve saper programmare** per migliorare un workflow: i skill sono file Markdown in `skills/<nome>/SKILL.md`.

Vedi [CONTRIBUTING.md](CONTRIBUTING.md) — passi per Issue e PR, standard per il diritto italiano, codice di condotta.

## Aree in cui cerchiamo aiuto

- Contenzioso civile (c.p.c., cautelare, esecuzione)
- Amministrativo (TAR, Consiglio di Stato)
- Societario e M&A
- Famiglia, tributario, diritto dell’UE

Apri un’Issue con il template **nuova area** (materia + riferimenti normativi tipici).

## Licenza

[MIT](LICENSE) — vedi anche [NOTICE](NOTICE).

*English abstract: experimental Claude Code plugins for Italian legal practice; no legal advice; no statute database in repo.*
