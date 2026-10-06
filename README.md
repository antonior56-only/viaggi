# I miei viaggi · PWA

Pacchetto statico pronto per hosting HTTPS e GitHub Pages. L'app mantiene il codice in un unico file HTML per facilitare le modifiche senza cambiare l'architettura esistente.

## Pubblicazione su GitHub Pages

1. Carica **il contenuto** di questa cartella (`index.html`, `manifest.webmanifest`, `service-worker.js` e `icons/`) nella cartella pubblicata del repository.
2. In GitHub apri **Settings → Pages** e seleziona il branch e la cartella pubblicati.
3. Apri l'indirizzo HTTPS del sito. L'installazione e il service worker non funzionano da `file://`; per la prova locale usa un server HTTP.

I percorsi sono relativi, quindi il pacchetto funziona anche in una sottocartella del dominio Pages. Non è stata modificata o pubblicata alcuna configurazione GitHub Pages in questo workspace.

## Dati e backup

- Il viaggio attivo e i viaggi salvati continuano a risiedere nel `localStorage` del browser e sul dispositivo utilizzato.
- In **Dati → Esporta backup completo** si scarica un JSON con viaggio attivo e viaggi salvati. Le chiavi API Gemini e OpenRouteService non sono incluse.
- **Importa viaggio o backup** accetta sia il vecchio JSON del singolo viaggio, sia il nuovo backup completo. Ripristinando un backup, i viaggi salvati esistenti vengono conservati; in caso di ID duplicati si crea un ID distinto.
- Conserva una copia del backup anche fuori dal dispositivo: i dati locali non si sincronizzano automaticamente tra dispositivi.

## Installazione e uso offline

- Su Android Chrome, apri il sito HTTPS e usa **Dati → Installa I miei viaggi** quando il browser rende disponibile l'installazione. In altri browser il comando potrebbe non essere esposto; è comunque possibile usare il menu del browser e “Aggiungi a schermata Home”.
- Il service worker memorizza la pagina dell'app e le icone. In assenza di rete si possono consultare e modificare i dati locali già presenti.
- Gemini, geocodifica, meteo, itinerari online, Google Maps e link di prenotazione richiedono Internet. Il service worker non intercetta né memorizza le chiamate a servizi esterni.
- Le chiavi API restano nel `localStorage` del browser, come nella versione originale. In un'app statica client-side non sono segreti e non vanno inserite nel repository pubblico.

## Aggiornamenti

Il nome della cache del service worker include una versione. Quando si modifica il pacchetto, incrementa `CACHE_NAME` in `service-worker.js` se vuoi forzare il rinnovo della cache shell.


Il manuale utente in PDF è incluso nel pacchetto e disponibile nella scheda **Dati → Manuale utente**.
