# Versione 37 — 16 ottobre 2026

L'app sceglie automaticamente Gemini 3.8 Flash per le cinque funzioni AI e prova 2.5 Flash soltanto se la prima richiesta riceve HTTP 404. La stessa richiesta viene ripetuta una sola volta; errori di chiave, quota o rete non provocano retry. La selezione manuale è rimossa da Impostazioni. Service worker e controllo aggiornamenti restano come nella versione 36, con nuova cache 37. README e manuale PDF aggiornati.

Verifica con risposte HTTP simulate: 200, 404+200, doppio 404, 400, 401, 429 e 500; corpo e intestazioni della richiesta invariati nel retry. PDF di 16 pagine renderizzato e controllato. Nessuna chiamata reale a Gemini né pubblicazione sul sito.
