# Claude per il diritto italiano

**Assistenti guidati per il lavoro giuridico in Italia** — dentro [Claude Code](https://docs.anthropic.com/en/docs/claude-code), lo strumento di Anthropic per lavorare con l’AI sul tuo computer (cartelle, documenti, bozze).

Non è un software da studio tradizionale: è una **raccolta di “ricette”** (skill) che insegnano a Claude *come* impostare un fascicolo, una risposta GDPR, una revisione contrattuale o una diffida, passo dopo passo, **in italiano** e con le cautele del nostro ordinamento.

Repository: [github.com/pixari/claude-per-il-diritto-italiano](https://github.com/pixari/claude-per-il-diritto-italiano)

> [!WARNING]
> **Solo bozze da revisionare — non consulenza legale.**  
> Nessun testo di legge è conservato in questo repository. Ogni riferimento normativo va **verificato** da te o dal tuo studio prima dell’uso in un mandato reale.  
> Leggi [AVVERTENZE.md](AVVERTENZE.md) prima del primo utilizzo.

---

## A chi serve

- **Avvocati e praticanti** che vogliono accelerare prime bozze, checklist e struttura degli atti.
- **Uffici legali, DPO, HR** che gestiscono privacy, lavoro o contratti B2B.
- **Chi non è “tecnico”**: non serve programmare; servono Claude Code installato e la voglia di seguire una procedura guidata (comandi che iniziano con `/`).

Claude **non sostituisce** il professionista abilitato: organizza il lavoro, propone **scheletri** e domande utili; la responsabilità resta tua.

---

## Cosa ottieni in pratica

Ogni **plugin** è un pacchetto per materia (privacy, lavoro, civile, contenzioso…). Dentro trovi skill come:

| Situazione tipica | Cosa chiedi a Claude (esempio) |
| --- | --- |
| Arriva una richiesta di accesso GDPR | Apri un fascicolo privacy, poi avvia la skill per la risposta all’interessato |
| Devi valutare un licenziamento | Fascicolo lavoro + skill di revisione (motivazione, tutele, `[da verificare]`) |
| Contratto fornitore da mandare in revisione | Fascicolo civile + revisione B2B o fornitore |
| Cliente vuole una diffida prima del giudizio | Plugin contenzioso: fascicolo + bozza diffida |
| Assemblea società da documentare | Verbale in bozza + checklist quorum (da verificare) |
| Ricorso al TAR | Struttura del ricorso in bozza, senza deposito automatico |

Le skill sono **lunghe e strutturate** (non risposte generiche): cold-start, playbook nella cartella del plugin, fascicoli “matter” dove tenere documenti e note del caso.

---

## Come si usa (in 4 passi)

### 1. Installa Claude Code

Segui la guida ufficiale Anthropic per il tuo sistema. Ti serve un account Claude con accesso a Claude Code.

### 2. Aggiungi questo marketplace e i plugin che ti servono

Copia e incolla in Claude Code (una riga alla volta):

```text
/plugin marketplace add pixari/claude-per-il-diritto-italiano
/plugin install diritto-italiano-hub@pixari-italian-legal-skills
/plugin install privacy-gdpr@pixari-italian-legal-skills
```

Per altre materie, installa solo ciò che ti serve (vedi tabella sotto). Puoi aggiungerne altri in seguito con lo stesso comando `/plugin install …`.

### 3. Prima sessione consigliata (5–10 minuti)

```text
/diritto-italiano-hub:avvertenze-legali
/diritto-italiano-hub:cold-start-interview
```

La **cold-start** raccoglie come lavori (studio, settori, tono delle bozze). Non è obbligatoria, ma rende le risposte successive più coerenti.

### 4. Apri un fascicolo e avvia il workflow

Un **fascicolo** è una cartella di lavoro per un caso (es. “dsar-rossi-2026”): lì tieni documenti, cronologia, bozze. Poi lanci la skill del compito.

**Esempio privacy (richiesta diritti interessato):**

```text
/privacy-gdpr:cold-start-privacy
/privacy-gdpr:fascicolo-privacy dsar-rossi-2026 dsar
```

Descrivi il caso o allega i file del fascicolo, poi:

```text
/privacy-gdpr:risposta-diritti-interessato
```

**Esempio lavoro (licenziamento):**

```text
/lavoro:fascicolo-lavoro licenziamento-bianchi-2026
/lavoro:revisione-licenziamento
```

**Esempio contratto B2B:**

```text
/diritto-civile:fascicolo-civile fornitore-alfa contratto
/diritto-civile:revisione-contratto-b2b
```

> **Nota sui comandi:** la parte prima dei `:` è il **plugin** (`privacy-gdpr`), dopo i `:` è la **skill** (`risposta-diritti-interessato`). Se un comando non funziona, vedi [TROUBLESHOOTING.md](TROUBLESHOOTING.md).

Percorsi guidati passo-passo: [QUICKSTART.md](QUICKSTART.md).

---

## I 8 pacchetti per materia

| Materia | Plugin | Esempi di skill |
| --- | --- | --- |
| Impostazioni comuni e metodo | `diritto-italiano-hub` | avvertenze, cold-start, fascicolo mandato, metodo giuridico |
| Privacy e GDPR | `privacy-gdpr` | fascicolo privacy, risposta interessato, DPA, DPIA, violazione |
| Lavoro | `lavoro` | fascicolo lavoro, licenziamento, policy interna, qualificazione rapporto |
| Contratti e commerciale | `diritto-civile` | B2B, fornitore, NDA, SaaS, rinnovi, escalation clausole |
| Contenzioso civile | `contenzioso-civile` | fascicolo, diffida, comparsa, cronologia, cautelare |
| Societario | `societario` | verbale assemblea, patto soci, operazioni, due diligence (checklist) |
| Amministrativo e PA | `amministrativo` | ricorso TAR (bozza), ADR con PA, cronologia procedimento |
| Prodotto digitale e IP leggero | `prodotto-servizi` | termini di servizio, privacy sito, marchio (pre-esame) |

Dettagli e elenco skill aggiornato in ogni cartella plugin (es. [privacy-gdpr/README.md](privacy-gdpr/README.md)).

**Installazione singola plugin** (sostituisci il nome):

```text
/plugin install contenzioso-civile@pixari-italian-legal-skills
```

---

## Fascicoli: dove “vive” il tuo caso

Pensa al fascicolo come alla **sottocartella del mandato** su cui Claude lavora in modo ripetibile:

- **Hub:** `fascicolo-mandato` — mandato generico o multi-materia  
- **Privacy:** `fascicolo-privacy` — DSAR, violazione, DPA  
- **Lavoro:** `fascicolo-lavoro` — licenziamento, indagine, policy  
- **Civile:** `fascicolo-civile` — contratti (il contenzioso pieno è nel plugin `contenzioso-civile`)  
- **Contenzioso:** `fascicolo-contenzioso` — parti, rito, atti  

Opzionale: puoi documentare preferenze persistenti sotto  
`~/.claude/plugins/config/pixari-italian-legal-skills/<plugin>/`  
(solo documentazione; nessun obbligo tecnico).

---

## Provare senza clienti reali

Nella cartella [`testatti/`](testatti/) trovi **casi fittizi** (nomi e fatti inventati) per esercitarti:

- privacy → `testatti/privacy-fittizio/`
- licenziamento → `testatti/licenziamento-fittizio/`
- contratto → `testatti/contratto-b2b-fittizio/`
- contenzioso → `testatti/contenzioso-fittizio/`

**Non** caricare in GitHub issue o pull request documenti con dati reali di clienti.

---

## Cosa aspettarsi dall’output

Ogni skill è pensata per produrre:

1. **Disclaimer** in testa (“bozza, non consulenza”).  
2. Marcatori **`[da verificare]`** su norme o giurisprudenza non confermate da fonte che hai indicato tu.  
3. **Niente sentenze inventate** — se manca la fonte, la skill deve dirlo.  
4. Sezione **Divieti** (niente pareri vincolanti, niente deposito automatico in giudizio, ecc.).

Integrazioni opzionali (Normattiva, giurisprudenza, DMS): [docs/CONNETTORI.md](docs/CONNETTORI.md) — solo se il tuo studio le usa già; non sono obbligatorie.

---

## Domande frequenti

**Devo installare tutti e 8 i plugin?**  
No. Installa hub + le materie che usi. Gli altri si aggiungono quando servono.

**È aggiornato al diritto vigente?**  
Il repository non contiene leggi. Claude può ragionare su ciò che gli fornisci o su strumenti collegati; **tu** verifichi aggiornamento e applicabilità.

**Posso usarlo in cloud Anthropic invece che in locale?**  
Questa raccolta è ottimizzata per **Claude Code** (lavoro su file e fascicoli locali). Valuta riservatezza e contratti con il fornitore AI.

**Ho un errore “plugin not found”?**  
Vedi [TROUBLESHOOTING.md](TROUBLESHOOTING.md).

---

## Contribuire e licenza

Vuoi migliorare una skill o segnalare un problema: [CONTRIBUTING.md](CONTRIBUTING.md).  
Novità per versione: [CHANGELOG.md](CHANGELOG.md).

[MIT](LICENSE) — testi originali in italiano; vedi [NOTICE](NOTICE).
