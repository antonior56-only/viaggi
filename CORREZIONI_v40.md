# Modifiche versione 40

- Gemini 2.5 Flash è il modello provato per primo.
- Gemini 3.8 Flash resta come alternativa se il primo modello restituisce HTTP 404 (modello non trovato).
- Se Gemini risponde con un errore di quota o altro errore diverso da 404, l’app mostra l’errore e non invia una seconda richiesta a un altro modello.
- Navigazione, dati salvati, chiavi API e contenuti dell’itinerario sono invariati.
- Aggiornati il numero di versione e la cache del service worker a 40.
