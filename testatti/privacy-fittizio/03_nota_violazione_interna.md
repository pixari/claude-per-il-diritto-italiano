# Nota interna — incidente sicurezza (fittizio)

**Data scoperta:** 18/03/2026  
**Segnalato da:** IT

## Fatto

Credenziali admin CRM esposte in repository Git privato per ~48h (commit errato). Possibile accesso a anagrafica clienti B2B (~1.200 record: nome, email, P.IVA, telefono). Nessuna prova di exfiltrazione; log accessi anomali: 2 IP esteri, 14 download export.

## Azioni

- Revoca credenziali, rotazione secret, scan repo
- Contenimento completato 19/03/2026 ore 09:00

---

*Usare con `/privacy-gdpr:violazione-dati`*
