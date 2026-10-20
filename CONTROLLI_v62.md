# Controlli eseguiti
Microsoft Edge headless, dati sintetici, servizio Gemini simulato, richieste esterne bloccate.
- Tappe con stesso nome e indirizzo: una sola prenotazione resta associata alla tappa corretta e il suo orario non cambia. Controllati helper, proposta Gemini e proposta per distanza.
- Proposta Gemini con pausa generica: pausa conservata, appuntamento mantenuto, ordine vincolato e orario prenotato invariato.
- Nessuna modifica al viaggio attivo prima della conferma della proposta; indici di lavoro esclusi dalla proposta finale.
- Avviso di orario inverso collegato alla tappa corretta, riepilogo Home e controllo completo visibili.
- Backup invariato e apertura dei dettagli senza promemoria; modifica della nota personale con copia vecchia riconosciuta; protezione orario conservata nell’importazione.
- Preparazione del contenuto di stampa riuscita.
- Navigazione in Home, Viaggio, Itinerario, Preparativi, Viaggi salvati e Impostazioni alle larghezze 360, 390, 768 e 1280 px: nessun overflow orizzontale rilevato. Nessun errore JavaScript durante queste prove.
- Sintassi, risorse manifest/service worker e conservazione di tutte le funzioni nominate del pacchetto precedente controllate.
Non effettuate chiamate reali a Gemini o OpenRouteService, installazioni/aggiornamenti PWA o prove su Android fisico. Il manuale non è stato modificato da questa correzione.
