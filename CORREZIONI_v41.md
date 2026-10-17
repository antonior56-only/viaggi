# Correzioni versione 41

- Corretto il trattamento di `null` e stringhe vuote nei campi di minuti e distanza dei segmenti: non diventano più `0`, quindi i riepiloghi non mostrano trasferimenti di durata/distanza zero quando Gemini non ha fornito quel dato.
- Aggiunta una scadenza alle richieste verso Gemini (60 secondi), OpenStreetMap e ricerca località (20 secondi), OpenRouteService geocoder (25 secondi), matrice ORS (30 secondi), meteo (20 secondi) e verifica aggiornamenti (12 secondi). Le richieste scadute restituiscono un errore leggibile, che viene gestito dai flussi di errore già presenti.
- Ridotti i salvataggi ripetuti durante la digitazione di destinazione, città di partenza, interessi, programma del giorno, tema, note e riferimenti di prenotazione: il salvataggio parte dopo 450 ms di inattività.
- Il salvataggio differito viene anticipato prima di cambiare scheda, usare Indietro, salvare esplicitamente o chiudere la pagina; il controllo dei dati condivisi fra finestre non sovrascrive modifiche in attesa.
- Aggiornato il numero versione e la cache PWA a 41.

Il manuale utente non è stato modificato: questa versione non cambia le procedure visibili all’utente. Nessuna pubblicazione è stata eseguita.