# Versione 26 — 09/10/2026

Modifiche autorizzate:
- Controllo della partenza giornaliera nelle schede Viaggio, Programma e Oggi: indirizzo inserito, indirizzo localizzato, coordinate salvate, link separati a Google Maps e conferma esplicita.
- Ricerca/correzione con elenco dei risultati: nessuna posizione viene applicata automaticamente. «Usa questa posizione» salva il risultato scelto mantenendo l’indirizzo inserito e tutte le tappe.
- Versione visibile nelle Impostazioni e aggiornamento della cache offline a 26.

Le partenze esistenti vengono indicate come da verificare, senza cambiarne le coordinate. Confermare la posizione salvata solo dopo averla controllata in Maps; se errata, cercare e scegliere una posizione alternativa. Una conferma dell’utente non equivale a una certificazione geografica automatica.

Verifiche: JavaScript valido; test Chromium dei tre punti di accesso, selezione/conferma e salvataggio, ricerca vuota/non disponibile e risultati obsoleti; regressione su date, interessi, quattro partenze Napoli nei link e nella stampa, correzione/aggiunta tappe, backup/cestino e importazione. Le risposte cartografiche dei nuovi test sono simulate, senza verifica geografica dal vivo.

Il manuale PDF e gli altri file preesistenti, eccetto index.html e service-worker.js, sono identici alla versione precedente.
