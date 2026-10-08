# Verifica completa - versione 21 - 8 ottobre 2026

Confronto fra upload/index.html (identico al secondo HTML allegato) e l’ultima versione dell’app, normalizzando soltanto i ritorni a capo per l’analisi.

## Risultato del confronto delle funzioni
123 funzioni dichiarate nel file originale: 107 hanno corpo invariato; 14 sono adattate per i requisiti approvati; 2 sono rimosse per richieste esplicite. Nessuna ulteriore funzione originale risulta assente.

| Area | Esito |
| --- | --- |
| Destinazione, date, ricerca, meteo | Conservati; Interessi modificabili con virgole e autosave |
| Generazione Gemini, approfondimento e ottimizzazione | Codice originale conservato |
| Importazione itinerario da testo/PDF/DOCX, anteprima e applicazione | Codice originale conservato |
| Ricerca tappe, correzione posizione, riordino, tappe irrinunciabili | Conservati |
| Orari, durate, trasporti e segmenti multipli | Conservati |
| Modalità Oggi | Conservata senza completamento/arrivo effettivo, come richiesto |
| Percorso Maps giornaliero | Disponibile in entrambe le viste, anche per una tappa; parti consecutive oltre il limite |
| Prenotazioni e checklist | Conservati; salvataggio delle voci predefinite corretto |
| Budget e quota per persona | Conservati |
| Stampa dettagliata/compatta e opzioni | Codice originale conservato; avvisi esclusi dalla stampa |
| Installazione, chiavi API, manuale | Conservati |
| Gestione viaggi | Home, elenco unico, identificativi stabili e IndexedDB come approvato |
| Salva manuale in Archivio | Sostituito dall’automatico, come approvato |

## Correzioni di questa revisione
- Nome modificabile anche dall’elenco I miei viaggi, oltre che dalla Home.
- Aggiornamento dati tra finestre ripristinato usando IndexedDB e notifiche locali; rilevamento del conflitto se entrambe scrivono.
- Avvisi offline e salvataggio esclusi dalla stampa.
- Dati validi IndexedDB apribili anche se i vecchi valori legacy sono corrotti.
- Creazione, apertura, eliminazione e importazione protette da azioni simultanee.

## Collaudo effettivamente eseguito
Chromium reale su viewport mobile 390x844: ricerca destinazione con risposta simulata, date, digitazione interessi con virgole, opzioni e riordino tappe, modalità Oggi e link giornaliero, checklist, budget, stampa preparata e avvisi nascosti, cambio nome nell’elenco, caricamento offline tramite service worker, modifica e riapertura offline, aggiornamento fra finestre e conflitto. Nessun errore JavaScript durante questi controlli.

Test aggiuntivi jsdom/fake-indexeddb: migrazione senza cancellare localStorage, separazione viaggi, riapertura IndexedDB, importazioni JSON singolo e backup v1/v2, importazione invalida senza modifiche, eliminazione e percorsi lunghi senza perdita delle tappe.

Icone confrontate byte per byte con gli allegati originali: identiche.

## Limiti
Non collaudati sul telefono personale: installazione Android/iOS, passaggio effettivo a Google Maps, servizi Gemini/OpenRouteService/meteo con credenziali e risposte reali. Il confronto verifica la conservazione del codice di queste funzioni, non garantisce disponibilità o correttezza dei servizi esterni. Il manuale PDF non è stato ulteriormente aggiornato: si attende l’aggiornamento unico richiesto.

## Correzione versione 22
Pulsante 🔄 per correggere indirizzo e posizione e sezione Aggiungi una nuova tappa disponibili sia in Programma sia in Modalità Oggi. Test Chromium superato con click sul pulsante, conferma della posizione simulata, ricerca e aggiunta effettiva di una tappa in Oggi e verifica dei comandi in Programma. Manuale PDF in attesa.

## Riesame finale versione 23: date e variazioni
Problema riprodotto: il gestore del cambio data ricreava la schermata e sostituiva i campi, togliendo il focus. Il gestore era rimasto identico a quello del file originale; il confronto del codice non era sufficiente a dimostrare che l’interazione funzionasse. I precedenti test riempivano il valore completo e non coprivano la digitazione per segmenti.

Correzione: nessuna ricreazione dei campi data durante il cambio; aggiornamento mirato del riepilogo, navigazione, avviso e partenze giornaliere. Il calendario nativo è conservato.

Test reale Chromium: digitazione cifra per cifra di partenza e ritorno; mantenimento del focus e degli stessi elementi; modifica di una data con evento change; conteggio giornate; riapertura con recupero di entrambe le date. Esito positivo.

Ulteriore controllo visibile rispetto all’originale nelle schede Viaggio, Itinerario (Programma e Oggi), Preparativi, Budget e Impostazioni: nessun comando mancante al di fuori del completamento tappe espressamente rimosso. Le varianti del link Maps e dell’editor interessi sono controllate come sostituzioni richieste. I comandi di ricerca e correzione sono verificati anche in Oggi.

### Classificazione delle variazioni
- Richieste approvate: Home, salvataggio automatico, elenco unico, IndexedDB e migrazione, backup compatibili, rimozione completamento in Oggi, link itinerario, interessi con virgole, correzione e aggiunta in entrambe le viste.
- Correzioni necessarie alla conservazione delle funzioni: nome nell’elenco, aggiornamento fra finestre, avvisi esclusi dalla stampa, protezione del viaggio durante operazioni asincrone, aggiornamento cache, stabilità dei campi data.
- Conservati: codice dei servizi Gemini, cartografia, importazione documenti, calcolo percorsi e tempi, dettagli tappe, prenotazioni, checklist, budget, preparazione della stampa.
- Nessuna nuova sezione, servizio o scelta progettuale introdotta in questo riesame.

Non si certifica il funzionamento di chiamate reali ai servizi esterni: i test cartografici usano risposte simulate e il test è in Chromium, non sul telefono personale.
