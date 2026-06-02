# MCP e connettori (opzionale, v2)

Questo repository **non** include un server MCP né un corpus normativo.

## Modello attuale

Gli skill chiedono all’utente di verificare norme e giurisprudenza sulle **proprie fonti**:

- Abbonamenti (database giuridici)
- Atti e fascicoli caricati nel workspace
- Gazzetta Ufficiale e atti ufficiali accessibili allo studio

Le citazioni non verificate devono essere marcate **`[da verificare]`**.

## Estensione futura (idea)

Come in [claude-for-legal](https://github.com/anthropics/claude-for-legal) (es. CourtListener per il US), si può aggiungere un **MCP configurato dall’utente** che:

- Interroga un database **già licenziato** dallo studio
- Restituisce estratti con riferimento per la verifica umana
- **Non** replica in Git testi di legge o sentenze

Requisiti per una PR MCP:

- Nessun corpus bundled nel repo
- Documentazione in italiano su rischi privacy e segreto professionale
- Istruzioni `.mcp.json` per plugin come esempio **disattivato di default**

## Contributi

Proponi un’integrazione con Issue **nuova-area** + bozza architettura. Non sostituire la verifica professionale con “citazioni automatiche” presentate come autentiche.
