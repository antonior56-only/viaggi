# Versione 27 - 09/10/2026

Modifica autorizzata a Strumenti itinerario > Approfondisci descrizioni:
- Nuova richiesta di schede concrete senza segnaposto, con fonti distinte.
- Anteprima con confronto prima/proposta per ogni tappa; possibilità di escludere schede e scartare tutto.
- Nessuna scrittura delle informazioni prima della conferma.
- Descrizioni vuote, brevi/generiche e risposte non confermate non sostituiscono i dati precedenti. Il motivo viene segnalato nell'anteprima.
- Fonti HTTP/HTTPS separate, con hostname visibile, senza chiamarle automaticamente siti ufficiali. Testi segnaposto e collegamenti non validi vengono esclusi. Funziona anche nella stampa e nell'importazione JSON.
- Se il viaggio cambia dopo la richiesta, la conferma viene bloccata per proteggere le modifiche recenti.
- Solo descrizione, apertura, prenotazione, costi e fonti vengono applicati. Tappe, ordine, orari del programma, posizioni e note personali restano invariati.

Versione visibile e cache offline aggiornate a 27. Il manuale PDF resta quello della versione 26; le indicazioni sui limiti di Approfondisci descrizioni sono superate dalle correzioni qui descritte.

Test reali in Chromium con risposte Gemini simulate: segnaposto, campi non confermati, anteprima/scarto/selezione/conferma, fonti multiple e non valide, stampa, riapertura/importazione, risposta duplicata/indici non validi, protezione da modifiche recenti, vista mobile. Verificata invariabilità dei dati estranei alle informazioni aggiornate. Test di regressione su date, interessi, Maps, aggiunta/correzione tappe e backup/cestino superati.

Non è stata effettuata una richiesta Gemini con credenziali reali. I controlli sulla risposta non certificano la correttezza geografica o l'attualità di orari/prezzi: le fonti richiedono sempre verifica.
