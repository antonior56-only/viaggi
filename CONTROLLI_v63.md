# Verifiche
Microsoft Edge headless con sintesi vocale e wake lock simulati, dati fittizi e richieste esterne bloccate.
- Nessuna richiesta di schermo acceso prima dell’evento di avvio voce.
- Acquisizione del blocco all’avvio; rilascio dopo fine, stop, cambio sezione ed errore del sintetizzatore.
- Concessione tardiva del blocco dopo stop: rilascio immediato senza lasciare lo schermo bloccato acceso.
- Rifiuto del wake lock: avviso visibile e sessione di lettura non bloccata.
- Note personali escluse dal testo pronunciato; dati del viaggio invariati dopo la lettura.
- Nessun errore JavaScript nelle prove; nessun overflow orizzontale a 360, 390, 768 e 1280 px. Riquadro di ascolto ispezionato visivamente.
- Sintassi HTML/JavaScript e service worker, risorse locali, manifest e funzioni precedenti controllati.
- Manuale aggiornato di dieci pagine; pagine modificate renderizzate e ispezionate visivamente.
Non verificati su dispositivo Android fisico: voce effettivamente udibile, disponibilità delle voci offline e comportamento reale del blocco schermo. Non eseguite chiamate Gemini né prove di aggiornamento di una PWA installata. I test simulati verificano la logica, non sostituiscono la prova sul telefono.
