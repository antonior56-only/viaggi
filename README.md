# I miei viaggi - pubblicazione PWA

Questa cartella contiene soltanto l’app pronta da pubblicare: HTML, manifest, service worker, metadati, icone, manuale PDF e questa guida.

## Aggiornamento su GitHub Pages
1. Esporta un backup completo dall’app già utilizzata e verifica di aver conservato il JSON.
2. Pubblica il contenuto di questa cartella nella stessa posizione GitHub Pages già usata. Non cambiare dominio, protocollo o sottocartella.
3. Sostituisci insieme tutti i file. Non occorre pubblicare Materiali_sviluppo_I_miei_viaggi.
4. Apri il sito online, usa l’avviso di aggiornamento e controlla che i viaggi siano presenti. Conserva il backup.

Il manifest e il service worker usano percorsi relativi. Il manuale PDF è parte dell’app e della shell offline. I dati locali sono associati all’origine del sito: cambiare dominio non trasferisce i viaggi.

## Uso e dati
- In Itinerario → Prepara → Strumenti della giornata → Riordina le tappe sono disponibili Per orario, Per vicinanza e Con Gemini. Per orario propone la sequenza cronologica senza ricalcolare gli orari, anche automatici o prenotati; a parità di ora mantiene l’ordine attuale. Le tappe senza orario valido restano in fondo. Funziona offline e senza coordinate. Anteprima, conferma e Annulla restano disponibili.
- Un orario non ancora definito resta vuoto anche nei campi e durante l’importazione JSON, senza trasformarsi in un falso 09:00. Se cambia la tappa precedente, i dati della tratta vengono azzerati per consentire nuove stime: controlla fattibilità, mezzi e tempi. Il riordino non modifica le prenotazioni esterne.
- Nuovo avvio: viene scelto il viaggio salvato con destinazione e date valide e partenza più vicina, da oggi a oggi più dieci giorni inclusi. A parità di partenza prevale il salvataggio più recente. I viaggi nel cestino non partecipano.
- Se nessun viaggio rientra nel periodo, si apre Viaggio con una scheda vuota. Viene riutilizzata solo una scheda senza nome e identica ai valori iniziali, evitando duplicati vuoti senza sovrascrivere preferenze o dati inseriti. Tutti gli altri viaggi rimangono nei Viaggi salvati.
- Ricaricare la pagina, tornare indietro o aggiornare l’app conserva il lavoro corrente. Tornare da Maps senza un nuovo caricamento non rilancia la selezione. Il criterio riguarda la data di partenza: viaggi iniziati prima di oggi o più lontani si aprono manualmente dall’elenco.
- Percorso di creazione: compila la scheda principale in Viaggio, apri facoltativamente Interessi e tappe imperdibili e Da dove parti ogni giorno?, poi premi Crea itinerario. Scegli Genera con AI, Incolla o carica un programma oppure Aggiungi le tappe personalmente. Una funzione AI senza chiave apre il campo corretto nelle impostazioni; l’aggiunta manuale non richiede Gemini.
- La proposta resta separata dal programma attivo fino alla conferma. Ogni giornata dell’anteprima si può espandere per controllare e modificare le tappe. Dopo l’applicazione, Controlla il programma raccoglie avvisi e correzioni; Apri il mio itinerario porta alla consultazione. L’assenza di incompletezze evidenti non garantisce che prezzi, orari e percorsi siano corretti.
- Strumenti della giornata raccoglie riordino, nuove proposte, approfondimenti, stampa e condivisione. Riordina le tappe riguarda la giornata; Rigenera con AI propone invece tutte le giornate e richiede conferma per sostituire il programma. La stampa continua a includere il viaggio secondo le opzioni scelte.
- In Modifica della tappa trovi Sposta in un altro giorno: scegli destinazione e orario, confronta entrambe le giornate e conferma. La tappa viene aggiunta in fondo senza riordinare le altre. Note e prenotazioni restano conservate, ma i biglietti non cambiano data e le tratte coinvolte vanno ricontrollate. Puoi annullare lo spostamento.
- Il meteo spiega i periodi non disponibili e, per viaggi coperti solo in parte, consulta le date utilizzabili senza cambiare quelle del viaggio. Errori di richiesta, limiti del servizio e connessione hanno messaggi distinti.
- Spuntare la checklist e aprire i dettagli aggiorna solo gli elementi interessati. Le aperture dei dettagli non invalidano le anteprime; modifiche effettive ai dati continuano a bloccare proposte obsolete.
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
