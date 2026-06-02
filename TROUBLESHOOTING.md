# Risoluzione problemi installazione

## Errore: `Plugin "…" not found in marketplace "pixari-italian-legal-skills"`

### Causa più frequente: confondere **skill** e **plugin**

Si **installano i plugin**, non i singoli skill.

| Sbagliato (skill) | Corretto (plugin) |
| --- | --- |
| `metodo-giuridico@pixari-italian-legal-skills` | `diritto-italiano-hub@pixari-italian-legal-skills` |
| `checklist-licenziamento@pixari-italian-legal-skills` | `lavoro@pixari-italian-legal-skills` |
| `subsunzione-civile@pixari-italian-legal-skills` | `diritto-civile@pixari-italian-legal-skills` |

Dopo l’installazione del plugin, **usi** lo skill con:

```text
/diritto-italiano-hub:metodo-giuridico
/lavoro:checklist-licenziamento
/diritto-civile:subsunzione-civile
```

### Procedura completa

```text
/plugin marketplace add pixari/claude-per-il-diritto-italiano
/plugin marketplace update pixari-italian-legal-skills
/plugin install diritto-italiano-hub@pixari-italian-legal-skills
/plugin install lavoro@pixari-italian-legal-skills
```

Il nome del marketplace è **`pixari-italian-legal-skills`** (dal file `marketplace.json`), non il nome del repository GitHub.

### Altri casi

| Problema | Soluzione |
| --- | --- |
| Marketplace non aggiunto | `/plugin marketplace add pixari/claude-per-il-diritto-italiano` |
| Clone vecchio | `/plugin marketplace update pixari-italian-legal-skills` |
| Repo sbagliato (`open-avvo`) | Usa `pixari/claude-per-il-diritto-italiano` |
| Skill non in elenco | Installa prima il plugin che lo contiene |
| Cache corrotta | `rm -rf ~/.claude/plugins/cache` e reinstalla |

### Verifica da terminale

```bash
claude plugin marketplace list
claude plugin install diritto-italiano-hub@pixari-italian-legal-skills
```

Validazione locale (opzionale):

```bash
git clone https://github.com/pixari/claude-per-il-diritto-italiano.git
cd claude-per-il-diritto-italiano
claude plugin validate diritto-italiano-hub
```

## Plugin disponibili

| Plugin da installare | Skill inclusi (esempi) |
| --- | --- |
| `diritto-italiano-hub` | `metodo-giuridico`, `fascicolo-mandato`, `personalizzazione-playbook`, … |
| `diritto-civile` | `revisione-contratto-b2b`, `revisione-nda`, `revisione-contratto-saas`, … |
| `lavoro` | `revisione-licenziamento`, `hiring-review-lavoro`, `fascicolo-lavoro`, … |
| `privacy-gdpr` | `risposta-diritti-interessato`, `revisione-dpa`, `triage-trattamento`, … (v0.2) |

### Skill rinominati in v0.2

| v0.1 (non più valido) | v0.2 |
| --- | --- |
| `bozza-risposta-esercizio-diritti` | `risposta-diritti-interessato` |
| `checklist-clausole-privacy-contratto` | `revisione-dpa` |
