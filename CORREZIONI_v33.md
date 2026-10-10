# Versione 33 - 10/10/2026

Nella scheda Viaggio, per viaggi di più giornate, è disponibile la scelta esplicita:
- Stessa partenza per tutti i giorni: unico campo e controlli comuni, anche quando tutti gli indirizzi sono inizialmente vuoti. Le modifiche dal blocco comune valgono per tutti i giorni del periodo.
- Partenze diverse per giornata: un campo e controlli individuali per ogni giorno. La scelta è salvata nel viaggio e mantenuta nella normalizzazione dell'importazione JSON.

Passare a partenza comune con indirizzi o coordinate differenti richiede conferma: viene utilizzata la partenza del Giorno 1. Annullare conserva i dati. Passare a partenze diverse non modifica gli indirizzi. I giorni aggiunti ampliando le date ereditano la partenza comune quando questa è attiva. Le tappe restano invariate.

Per viaggi precedenti senza scelta salvata, partenze uguali (anche inizialmente vuote) mostrano il campo comune; partenze differenti mostrano i campi separati. Se una modifica in Itinerario produce partenze diverse, la scheda Viaggio le mostra separate per evitare di nascondere differenze.

Versione visibile e cache offline a 33. Manuale PDF invariato.

Test Chromium: nuovo viaggio di tre giorni con campo comune vuoto, indirizzo applicato a tutti, modalità separata conservata alla riapertura, conferma/annullamento prima di uniformare indirizzi diversi, tappe preservate, modalità in importazione JSON, nuovi giorni con partenza ereditata, riapertura e differenze mostrate individualmente, nessun errore JavaScript. Ricerca cartografica simulata.
