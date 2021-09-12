# Client-server

Separando le preoccupazioni dell'interfaccia utente dalle preoccupazioni relative alla memorizzazione dei dati, miglioriamo la portabilità dell'interfaccia utente su più piattaforme e miglioriamo la scalabilità semplificando i componenti del server.

---

* Dovrebbe esserci una chiara delimitazione tra client e server. 
* Le preoccupazioni relative all'interfaccia utente e alla raccolta delle richieste sono di dominio del client. 
* L'accesso ai dati, la gestione del carico di lavoro e la sicurezza sono il dominio del server. 
* Questo accoppiamento libero tra client e server consente a ciascuno di essere sviluppato e migliorato indipendentemente dall'altro.

---

## Client-server

Ciò significa essenzialmente che l'applicazione client e l'applicazione server DEVONO essere in grado di evolversi separatamente **senza alcuna dipendenza l'una dall'altra.** Un client dovrebbe conoscere solo gli [URI](046_URI_URL.md) delle risorse, e questo è tutto. Oggi, questa è una pratica normale nello sviluppo web, quindi non è richiesta alcuna fantasia da parte tua. Mantienilo semplice.
Server e client possono anche essere sostituiti e sviluppati in modo indipendente, a condizione che l'interfaccia tra loro non venga modificata.

---

Una architettura REST sposa il noto paradigma dell’informatica conosciuto con il termine di separation of concerns (SoC) : tradotto in italiano come “separazione delle preoccupazioni o compiti“. SoC è un principio di progettazione per separare un sistema in moduli distinti, in modo tale che ogni modulo si preoccupi di un certo compito.
REST applica il paradigma SoC con un architettura Client-Server . Ciò aiuta a stabilire un’architettura distribuita, supportando in tal modo l’evoluzione indipendente della logica lato client e della logica lato server.

---

Il vincolo Client-Server richiede che il server offra una o più funzionalità e ascolti le richieste di possibili client. Un client invoca il servizio messo a disposizione dal server inviando il corrispondente messaggio di richiesta e il servizio lato server respinge la richiesta o esegue l’attività richiesta prima di inviare un messaggio di risposta al client. La gestione delle eccezioni è delegata al client.