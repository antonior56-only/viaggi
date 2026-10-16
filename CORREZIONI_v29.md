# Versione 29 - 09/10/2026

Modifica autorizzata alla sola presentazione delle partenze nella scheda Viaggio:
- Se tutte le giornate del periodo hanno la stessa partenza, con indirizzo e coordinate coincidenti, un unico blocco «Partenza comune a tutte le giornate» sostituisce i controlli ripetuti.
- Il controllo considera anche l'indirizzo localizzato e l'eventuale utilizzo diretto di coordinate manuali; eventuali differenze mantengono la gestione separata.
- Conferma, ricerca e scelta di un risultato, modifica dell'indirizzo, coordinate manuali e posizione attuale applicate dal blocco comune aggiornano tutte le giornate del periodo. Non modificano le tappe.
- «Usa partenze diverse» espande i controlli individuali senza cambiare i dati. Se ancora identiche, «Mostra partenza comune» li ricompatta. La scelta della vista separata vale per la sessione corrente del viaggio; riaprendolo il raggruppamento viene valutato nuovamente.
- La conferma comune indica «Posizione confermata da te» solo se tutte le giornate sono confermate.
- Nell'Itinerario restano i controlli della singola giornata.

Versione visibile e cache offline a 29. Manuale PDF invariato, edizione 26: vedere anche le note delle versioni 27 e 28 per le funzioni successive.

Test Chromium: blocco unico, conferme con stato iniziale diverso fra giornate, espansione/ricompattazione, indirizzo comune, scelta risultato di ricerca simulato, coordinate manuali comuni, salvataggio/riapertura, espansione con coordinate differenti, conservazione tappe e controlli itinerario, visualizzazione su schermo mobile, nessun errore JavaScript.
