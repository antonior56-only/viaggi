# Controlli versione 17 - 8 ottobre 2026

## Eseguiti e superati
- Sintassi JavaScript dell’app e service worker; parsing del manifest.
- Migrazione simulata da tp_v1 e tp_trips verso IndexedDB, conservando i valori originali.
- Identificativi distinti per nuovo viaggio e viaggi migrati; riapertura corretta.
- Separazione tra budget, checklist e tappe di viaggi differenti.
- Salvataggio automatico e recupero dopo nuova apertura della pagina.
- Generazione DOM delle sezioni Home, Viaggio, Itinerario, Preparativi, Budget e I miei viaggi.
- Importazioni JSON singolo, backup versione 1 e versione 2; conservazione dei viaggi esistenti.
- Rifiuto di un’importazione non valida senza modificare i dati.
- Eliminazione del viaggio e rilevamento dei conflitti fra due finestre.
- Dimensioni delle icone: Apple 180, icona 192, icone standard e maskable 512.
- Manuale PDF aggiornato: integrazione iniziale renderizzata e verificata visivamente.

I test di gestione dati usano jsdom e fake-indexeddb: verificano la logica, ma non sostituiscono il collaudo nel browser reale.

## Da verificare nel browser reale
Chromium non era disponibile e il download non è riuscito. Non sono stati collaudati: layout a tutte le larghezze, attivazione/aggiornamento del service worker, caricamento offline completo, installazione Android/iOS, stampa del browser e servizi online con le chiavi personali.

## Procedura prima dell’uso quotidiano
1. Esportare il backup completo dalla vecchia versione.
2. Caricare tutti i file, mantenendo lo stesso repository e percorso pubblicato.
3. Chiudere e riaprire l’app; verificare Home e presenza dei viaggi precedenti.
4. Creare un viaggio di prova, aggiungere budget e checklist, attendere “Salvato”, riaprire e verificare i dati.
5. Esportare un backup e provarne l’importazione: vengono aggiunte copie, non sostituiti i viaggi.
6. Dopo un caricamento completo online, attivare modalità aereo e verificare consultazione e modifica.
7. Verificare mappe, itinerario, Gemini e stampa con rete disponibile.

## Scelte conservative
Le copie precedenti dell’Archivio e il viaggio attivo vengono conservati come schede separate, anche quando simili. Nessuna deduplicazione automatica. I dati locali non sono sincronizzati tra dispositivi. Il manuale conserva integralmente le pagine precedenti dopo la nuova integrazione, che prevale sulle vecchie istruzioni di salvataggio.

## Correzione versione 18
Test DOM e URL superati: link con una sola tappa, entrambe le viste, partenza dall’hotel, inclusione di 24 tappe suddivise in tre parti, posizione sotto le tappe e prima della ricerca. Restano i limiti del collaudo browser descritti sopra.

## Versione 19
Rimossi pulsante Fatta ora e funzioni di completamento in Modalità Oggi. Verificate assenza del gestore, barra di avanzamento e arrivo effettivo; ripetuti con esito positivo i controlli dati e link Maps. Il PDF resta in attesa dell’aggiornamento unico.

## Versione 20
Test superati sul campo Interessi: testo modificabile, evento di digitazione, virgole conservate, salvataggio IndexedDB, mantenimento del focus e rilettura dopo navigazione. Ripetuti i test dati e link Maps.

## Revisione versione 21
La precedente indisponibilità di Chromium è stata risolta in questa revisione. Collaudo reale di service worker/offline, input, tappe, checklist, budget, stampa e finestre multiple superato. Per il confronto completo e i limiti residui leggere VERIFICA_CONFRONTO.md.

## Correzione versione 22
Pulsante 🔄 per correggere indirizzo e posizione e sezione Aggiungi una nuova tappa disponibili sia in Programma sia in Modalità Oggi. Test Chromium superato con click sul pulsante, conferma della posizione simulata, ricerca e aggiunta effettiva di una tappa in Oggi e verifica dei comandi in Programma. Manuale PDF in attesa.

## Versione 23 - Date
Corretto il cambio date per evitare ricreazione dei campi e perdita del focus. Collaudo Chromium superato con digitazione cifra per cifra, passaggio tra partenza e ritorno e riapertura. Ripetuti tutti i controlli descritti in VERIFICA_CONFRONTO.md. Manuale PDF ancora differito.

## Versione 24
Test automatici (jsdom + IndexedDB simulato) superati: migrazione dai dati precedenti, eliminazione del viaggio non attivo e attivo con Annulla, persistenza del cestino dopo il riavvio, ripristino, svuotamento oltre 30 giorni, duplicazione, esportazione del singolo viaggio, promemoria backup, importazione dello stesso backup senza doppioni e di un backup con un viaggio nuovo. Da verificare su telefono e in Chromium: posizione dell'avviso "Annulla" sopra il menu in basso e comportamento dei quattro pulsanti nella riga di ogni viaggio su schermi stretti.
