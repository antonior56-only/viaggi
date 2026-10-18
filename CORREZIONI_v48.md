# Correzione del controllo aggiornamenti

Il controllo aggiornamenti confrontava il numero servito da app-version.json con una costante interna rimasta al valore precedente. Di conseguenza, dopo il caricamento del pacchetto, la Home poteva continuare a proporre lo stesso aggiornamento.

Allineati il numero interno, app-version.json e la cache del service worker. Il manuale non cambia.
