# I miei viaggi - PWA versione 21

Caricare il contenuto di questa cartella nella stessa cartella pubblicata su GitHub Pages. Non cambiare dominio o percorso se si vogliono ritrovare i dati locali. Prima dell’aggiornamento esportare il backup dalla vecchia app. Non è stata eseguita alcuna pubblicazione.

## Novità
Home con riepilogo e nome del viaggio attivo; nuovo viaggio senza sostituire il precedente; elenco unico con filtri; salvataggio automatico IndexedDB con indicatore di completamento; migrazione conservativa da tp_v1 e tp_trips. I valori precedenti restano intatti in localStorage. Nessuna sincronizzazione fra dispositivi.

## Backup
Esporta backup completo dall’elenco I miei viaggi. Importazione compatibile con JSON singolo e backup versione 1 e 2; gli import ricevono identificativi nuovi e non sostituiscono dati esistenti. Le chiavi API non sono esportate. Se due finestre modificano dati in concorrenza, la seconda scrittura viene bloccata: esportare la copia di emergenza e ricaricare.

## Installazione e offline
Richiede HTTPS (o localhost). Il service worker versione 21 include pagina, manifest, manuale e tutte le icone. Primo caricamento online necessario. Gemini, geocodifica, meteo, OpenRouteService e prenotazioni richiedono Internet. Le chiavi API restano locali, non devono essere inserite nel repository.

## Manuale
Il PDF include le nuove istruzioni nelle prime pagine; queste sostituiscono le parti precedenti su Home, Archivio e salvataggio. Il resto del manuale originale è conservato.

## Correzione itinerario versione 18
Link Google Maps ripristinato subito sotto le tappe, in Programma e Modalità Oggi, anche per una sola tappa. Percorsi oltre il limite del collegamento vengono suddivisi in parti consecutive senza scartare tappe.

## Versione 19
Modalità Oggi senza pulsante Fatta ora, registrazione dell’arrivo effettivo, stati di completamento o barra di avanzamento. Manuale PDF in attesa dell’aggiornamento unico richiesto.

## Versione 20
Campo Interessi come area di testo modificabile, con istruzioni per separare più interessi tramite virgola e salvataggio automatico durante la digitazione. Il PDF resta in attesa dell’aggiornamento unico.

## Revisione completa versione 21
Confrontata con l’HTML originale allegato. Ripristinati cambio nome nell’elenco e aggiornamento fra finestre; corretta stampa degli avvisi; avvio da IndexedDB indipendente da vecchi valori legacy non leggibili. Collaudo Chromium completato per gestione viaggio, tappe, preparativi, budget, stampa e offline. Manuale differito come richiesto.

## Correzione versione 22
Pulsante 🔄 per correggere indirizzo e posizione e sezione Aggiungi una nuova tappa disponibili sia in Programma sia in Modalità Oggi. Test Chromium superato con click sul pulsante, conferma della posizione simulata, ricerca e aggiunta effettiva di una tappa in Oggi e verifica dei comandi in Programma. Manuale PDF in attesa.

## Versione 23 - Date
Corretto il cambio date per evitare ricreazione dei campi e perdita del focus. Collaudo Chromium superato con digitazione cifra per cifra, passaggio tra partenza e ritorno e riapertura. Ripetuti tutti i controlli descritti in VERIFICA_CONFRONTO.md. Manuale PDF ancora differito.

## Versione 24 - Cestino, duplicazione e promemoria backup
Base: versione 23. Aggiunte:
- Eliminazione di un viaggio senza conferma: il viaggio va nel cestino per 30 giorni, con avviso "Annulla" per 9 secondi. Nell'elenco "I miei viaggi" c'è la sezione Cestino con Ripristina, Elimina definitivamente e Svuota cestino. Il cestino è salvato in IndexedDB insieme ai viaggi.
- Pulsanti 📄 Duplica e ⬇️ Esporta per ogni viaggio dell'elenco.
- Promemoria di backup in Home e in "I miei viaggi" dopo 30 giorni dall'ultima esportazione (o dal primo avvio). La data dell'ultimo backup è mostrata in elenco.
- Importazione senza doppioni: i viaggi già presenti non vengono aggiunti di nuovo; la conferma indica quanti vengono ignorati.
Il manuale PDF non è stato aggiornato (resta differito).

Collaudo di questa versione: test automatici con jsdom e IndexedDB simulato (migrazione, eliminazione e annulla, ripristino dopo riavvio, duplicazione, cestino, promemoria, importazione). Non è stato eseguito un collaudo in un browser reale.
