# Changelog

## [0.6.0] — prodotto-servizi

- Nuovo plugin `prodotto-servizi` (EN `product-legal` + `ip-legal` lite): ToS, privacy sito, marchio, cold-start

## [0.5.0] — societario + amministrativo

- Plugin `societario` (EN `corporate-legal`): assemblee, statuto, patto soci, DD checklist
- Plugin `amministrativo` (EN `regulatory-legal`): TAR, ADR PA, ricorsi
- Testatti: `assemblea-fittizia/`, `ricorso-tar-fittizio/`

## [0.4.0] — contenzioso + commercial

- Plugin `contenzioso-civile` (EN `litigation-legal` subset): 8 skill
- `diritto-civile`: `escalation-clausole`, `rinnovo-contratto`, `revisione-msa-fornitore`, `revisione-fornitore`, `storico-amendment`, `fascicolo-civile`
- Testatti `contenzioso-fittizio/`

## [0.3.0] — EN parity consolidation

- Matter workspace: `fascicolo-privacy`, `fascicolo-civile`, `fascicolo-lavoro` (path config doc)
- `personalizzazione-privacy`, `bozza-policy-interna`, `qualificazione-rapporto`
- Flagship skills expanded (DSAR, licenziamento, B2B, metodo)
- [docs/CONNETTORI.md](docs/CONNETTORI.md) (EN CONNECTORS)
- CI: `.github/workflows/validate-plugins.yml`

## [0.2.0] — 2026-06-02

- Espansione 4 plugin (~30 skill), testatti privacy/nda

## [0.1.0] — 2026

- Marketplace iniziale

### Benchmark EN (riferimento)

| Verticale EN | Plugin IT | Da v |
| --- | --- | --- |
| legal-builder-hub | diritto-italiano-hub | 0.3 |
| privacy-legal | privacy-gdpr | 0.3 |
| employment-legal | lavoro | 0.3 |
| commercial-legal | diritto-civile | 0.4 |
| litigation-legal | contenzioso-civile | 0.4 |
| corporate-legal | societario | 0.5 |
| regulatory-legal | amministrativo | 0.5 |
| product/ip-legal | prodotto-servizi | 0.6 |
