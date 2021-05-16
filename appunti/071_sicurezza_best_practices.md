## Security

Un'API RESTful fornisce un altro percorso per accedere e manipolare l'applicazione. Anche se non è un target di hacking interessante, un client mal comportato potrebbe inviare migliaia di richieste ogni secondo e arrestare in modo anomalo il tuo server.

le migliori pratiche comuni includono:

* usare HTTPS
* utilizzare un metodo di autenticazione affidabile
* utilizzare CORS per limitare le chiamate lato client a domini specifici
* fornire funzionalità minime, ovvero non creare opzioni DELETE non necessarie
* convalidare tutti gli URL degli endpoint e i dati del corpo
* evitare di esporre token API in JavaScript lato client
* bloccare l'accesso da domini o indirizzi IP sconosciuti
* bloccare carichi utili inaspettatamente grandi
* considerare la limitazione della velocità, ovvero le richieste che utilizzano lo stesso token API o indirizzo IP sono limitate a N al minuto
* rispondere con un codice di stato HTTP e un'intestazione di cache appropriati
* registrare le richieste e analizzare gli errori.