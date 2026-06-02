# Claude per il diritto italiano

> [!WARNING]
> **Bozze sperimentali — non consulenza legale.** Nessun corpus normativo in Git. [AVVERTENZE.md](AVVERTENZE.md) | [CONNETTORI.md](docs/CONNETTORI.md)

Skill marketplace per [Claude Code](https://docs.anthropic.com/en/docs/claude-code), architettura allineata a [claude-for-legal](https://github.com/anthropics/claude-for-legal) (EN): cold-start, playbook `CLAUDE.md`, matter workspace, skill workflow lunghi.

Repository: [github.com/pixari/claude-per-il-diritto-italiano](https://github.com/pixari/claude-per-il-diritto-italiano)

## 8 plugin (parità EN verticale)

| Plugin IT | Analogo EN | Versione |
| --- | --- | --- |
| `diritto-italiano-hub` | legal-builder-hub | 0.3.0 |
| `privacy-gdpr` | privacy-legal | 0.3.0 |
| `lavoro` | employment-legal | 0.3.0 |
| `diritto-civile` | commercial-legal | 0.4.0 |
| `contenzioso-civile` | litigation-legal | 0.4.0 |
| `societario` | corporate-legal | 0.5.0 |
| `amministrativo` | regulatory-legal | 0.5.0 |
| `prodotto-servizi` | product-legal + ip-legal (lite) | 0.6.0 |

README dettagliati in ogni cartella plugin.

## Installazione

```text
/plugin marketplace add pixari/claude-per-il-diritto-italiano
/plugin install diritto-italiano-hub@pixari-italian-legal-skills
/plugin install privacy-gdpr@pixari-italian-legal-skills
/plugin install lavoro@pixari-italian-legal-skills
/plugin install diritto-civile@pixari-italian-legal-skills
/plugin install contenzioso-civile@pixari-italian-legal-skills
/plugin install societario@pixari-italian-legal-skills
/plugin install amministrativo@pixari-italian-legal-skills
/plugin install prodotto-servizi@pixari-italian-legal-skills
```

Skill (non plugin): `/privacy-gdpr:risposta-diritti-interessato` — vedi [TROUBLESHOOTING.md](TROUBLESHOOTING.md).

## Configurazione (stile EN)

1. `/diritto-italiano-hub:avvertenze-legali`
2. `/diritto-italiano-hub:cold-start-interview`
3. Cold-start per verticale: `cold-start-privacy`, `cold-start-lavoro`, `cold-start-civile`, …
4. Matter: `fascicolo-mandato`, `fascicolo-privacy`, `fascicolo-lavoro`, `fascicolo-civile`, …

Profilo opzionale persistente (documentato):

`~/.claude/plugins/config/pixari-italian-legal-skills/<plugin>/`

## Test

[`testatti/`](testatti/) — fascicoli fittizi per ogni verticale. [QUICKSTART.md](QUICKSTART.md).

## Contribuire

[CONTRIBUTING.md](CONTRIBUTING.md) — [CHANGELOG.md](CHANGELOG.md)

## Licenza

[MIT](LICENSE) — [NOTICE](NOTICE)
