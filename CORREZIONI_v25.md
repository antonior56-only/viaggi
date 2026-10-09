# Correzioni richieste - revisione 25

Modifiche limitate a index.html e alla versione cache del service worker (25). Manuale, icone, manifest e precedenti documenti conservati byte per byte.

1. Il percorso giornaliero Google Maps usa come origine l’indirizzo esplicito impostato in startPlace; per Posizione attuale continua a usare le coordinate GPS. Nel JSON allegato tutte e quattro le partenze avevano il nome corretto ma coordinate diverse. Non sono state inventate o modificate coordinate: per il link è autorevole l’indirizzo scritto. Nessuna modifica alle tappe, al mezzo selezionato o al loro ordine.
2. Il confronto dei duplicati in importazione considera nome e dati del viaggio: nomi diversi con dati uguali restano distinti; importazioni ripetute dello stesso contenuto non creano altre copie.
3. Backup formato 3 con cestino, nomi e date di eliminazione. Importazione e ripristino del cestino supportati; le scadenze originali di 30 giorni restano invariate. Importazioni versione 1 e 2 ancora accettate. Le versioni precedenti dell’app non possono importare il nuovo formato 3: aggiornare prima l’app che deve ricevere il backup. Chiavi API escluse come prima.

Test Chromium superati: origini Maps delle quattro giornate del JSON, entrambe le viste e link di stampa; importazione nomi distinti; compatibilità backup v2; esportazione/importazione cestino con ripristino; importazione ripetuta senza nuove copie; date, interessi e riapertura. Nessun errore JavaScript. La destinazione risolta dal servizio Google Maps sul dispositivo personale non è stata verificata direttamente.
