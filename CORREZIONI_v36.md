# Versione 36 — 16 ottobre 2026

- Tutte e cinque le richieste AI usano il modello scelto in Impostazioni: 2.5 Flash per l'uso esistente, oppure 3.8 Flash. Scelta locale per dispositivo; le chiavi non entrano nel pacchetto.
- Il service worker lascia sempre passare app-version.json alla rete, anche con query di controllo, senza leggere o scrivere quella risposta nella Cache API.
- README aggiornato alla versione 36; manuale PDF aggiornato e incorporato.
- Verifiche: parsing dello script, cinque chiamate instradate tramite selezione comune, selezione valida/non valida, simulazione del service worker con due controlli aggiornamento senza nuove voci cache, asset ordinari ancora memorizzati, PDF di 16 pagine renderizzato e controllato. Non è stata usata una chiave Gemini reale; nessuna pubblicazione sul sito.
