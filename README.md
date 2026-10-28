# I miei viaggi - pubblicazione PWA

Questa cartella contiene soltanto l’app pronta da pubblicare: HTML, manifest, service worker, metadati, icone, manuale PDF e questa guida.

## Aggiornamento su GitHub Pages
1. Esporta un backup completo dall’app già utilizzata e verifica di aver conservato il JSON.
2. Pubblica il contenuto di questa cartella nella stessa posizione GitHub Pages già usata. Non cambiare dominio, protocollo o sottocartella.
3. Sostituisci insieme tutti i file. Non occorre pubblicare Materiali_sviluppo_I_miei_viaggi.
4. Apri il sito online, usa l’avviso di aggiornamento e controlla che i viaggi siano presenti. Conserva il backup.

Il manifest e il service worker usano percorsi relativi. Il manuale PDF è parte dell’app e della shell offline. I dati locali sono associati all’origine del sito: cambiare dominio non trasferisce i viaggi.

## Uso e dati
- Salvataggio automatico IndexedDB nel browser, senza sincronizzazione tra dispositivi. Backup e importazione JSON restano disponibili nei Viaggi salvati.
- Dopo un salvataggio con dati di viaggio l’app verifica e richiede, quando disponibile, l’archiviazione persistente. Il browser decide; l’esito compare in Impostazioni → App e aggiornamenti. Un rifiuto non blocca il salvataggio. La protezione non sostituisce i backup né recupera dati eliminati dall’utente.
- Chiavi Gemini e OpenRouteService facoltative, inserite dall’utente e conservate nel browser. Non incluse nel backup e da non pubblicare.
- In Durante il viaggio, Solo prossima tappa nasconde il resto del programma; Mostra giornata lo ripristina. Non modifica o completa tappe. Il suggerimento segue gli orari del programma, non il GPS.
- Condividi giornata prepara orari, nomi, indirizzi e link Maps. Usa la condivisione del dispositivo oppure Copia testo. Note personali e riferimenti prenotazione sono esclusi. Rileggi il messaggio prima di inviarlo.
- Nelle alternative scegli Al coperto, All’aperto o Non specificato e filtra l’elenco. Con previsioni già consultate nelle ultime 24 ore, probabilità giornaliera di pioggia almeno 60% e alternative indicate al coperto, l’app propone di valutarle. Non sostituisce visite automaticamente. Dopo un’importazione aggiorna le previsioni.
- Ho un’ora libera confronta alternative, cammino stimato, visita, trasferimento successivo o ritorno e margine. Inserimento con anteprima e conferma, annullabile. Verifica percorsi reali, aperture, pause e prenotazioni.

## Offline e limiti
L’app già caricata può consultare e modificare i dati locali. Preparare il testo da condividere e confrontare alternative con coordinate non richiede servizi esterni. Invio dei messaggi, Maps, ricerche, nuovi dati meteo, aggiornamenti e Gemini richiedono Internet o dipendono dalle applicazioni esterne. Audio e schermo acceso dipendono dal dispositivo; ascolto a schermo bloccato non garantito.

Il pacchetto tecnico separato contiene documentazione storica, viaggio dimostrativo e test ripetibili. Il viaggio di prova non viene aggiunto automaticamente all’app.
