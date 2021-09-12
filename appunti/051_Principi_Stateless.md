# Stateless

**Stateless**: ogni richiesta dal client al server deve contenere tutte le informazioni necessarie per comprendere la richiesta e non può sfruttare alcun contesto memorizzato sul server. Lo stato della sessione viene quindi mantenuto interamente sul client.

* Operazioni **stateless**. Tutte le operazioni client-server dovrebbero essere stateless e qualsiasi gestione dello stato richiesta dovrebbe avvenire sul client, non sul server.


---


Roy Fielding si è ispirato al protocollo HTTP, che di fatto è senza stato: stateless.

Uno dei principi dell'architettura REST è che tutte le interazioni client-server siano senza stato: il server non memorizzerà nulla sull'ultima richiesta HTTP effettuata dal client.
Tratterà ogni richiesta come nuova. Nessuna sessione, nessuna cronologia.

---

Se l'applicazione client deve mantenere stato memorizzato per l'utente finale, per esempio nei casi in cui l'utente accede una volta e fa successivamente altre operazioni autorizzate, ogni richiesta del client deve contenere tutte le informazioni necessarie per soddisfare la richiesta, tra cui autenticazione e autorizzazione.

Nessun contesto client deve essere memorizzato sul server tra le richieste.

Il client è responsabile della gestione dello stato dell'applicazione.

---

La comunicazione tra utente del servizio (client) e servizio (server) deve essere senza stato tra le richieste. Ciò significa che ogni richiesta da parte di un client dovrebbe contenere tutte le informazioni necessarie per il servizio per comprendere il significato della richiesta. Tutti i dati sullo stato della sessione dovrebbero quindi essere restituiti al consumatore del servizio alla fine di ciascuna richiesta. In breve ogni richiesta è come se fosse la prima richiesta e non è correlata ad una precedente richiesta.


---


Se il server è senza stato, può scalare molto più facilmente e sicuramente sarà molto più semplice perché elimina alla radice il problema della gestione e sincronizzazione delle sessioni utente in ambienti clusterizzati. Facciamo un esempio: il tuo servizio REST è utilizzato da milioni di persone e non regge il carico? Essendo stateless potrà essere scalato orizzontalmente in maniera semplicissima: basterà tirare su più istanze del tuo servizio  bilanciando il carico. Come? Utilizzando un Load Balancer che si ponga davanti alle istanze dei nostri server e passi le richieste seguendo delle regole ben precise (ad esempio, con l’algoritmo round robin a turno ogni server riceverà una richiesta, giunti all’ultimo server si riprende l’assegnazione partendo dal primo).

