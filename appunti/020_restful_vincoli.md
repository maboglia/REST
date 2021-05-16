# REST: Vincoli architettonici

**REST** è l'acronimo di **Representational State Transfer**, un termine coniato da Roy Fielding nel 2000. È uno **stile di architettura** per la progettazione di applicazioni, che viene spesso utilizzato nello sviluppo di servizi Web.

**REST** non applica alcuna regola in merito a come dovrebbe essere implementato a un livello inferiore, ma stabilisce solo linee guida di progettazione di alto livello e lascia che tu pensi alla tua implementazione.

Cominciamo con **elementi specifici del design standard** per chiarire cosa "Roy Fielding" vuole che costruiamo.

## Vincoli architettonici

REST definisce **6 vincoli architetturali** che rendono qualsiasi servizio web - una vera API RESTful.

* **[Client-server](050_Principi_ClientServer.md)**
* **[Stateless](051_Principi_Stateless.md)**
* **[Memorizzabile nella cache](052_Principi_Cacheable.md)**
* **[Interfaccia uniforme](053_Principi_InterfacciaUniforma.md)**
* **[Sistema a livelli](054_Principi_LayerSystem.md)**
* **[Codice su richiesta](055_Principi_CodeOnDemand.md)** (opzionale)

## Interfaccia uniforme

Poiché si applica il nome stesso del vincolo, DEVI decidere l'interfaccia API per le risorse all'interno del sistema che sono esposte ai consumatori API e seguono religiosamente. Una risorsa nel sistema dovrebbe avere un solo URI logico e ciò dovrebbe fornire un modo per recuperare dati correlati o aggiuntivi. È sempre meglio sinonimizzare una risorsa con una pagina web.

Ogni singola risorsa non dovrebbe essere troppo grande e contenere ogni cosa nella sua rappresentazione. Se pertinente, una risorsa deve contenere collegamenti (HATEOAS) che puntano a URI relativi per recuperare informazioni correlate.

Inoltre, le rappresentazioni delle risorse nel sistema dovrebbero seguire linee guida specifiche come convenzioni di denominazione, formati di collegamento o formato dei dati (XML o / e JSON).

Tutte le risorse dovrebbero essere accessibili attraverso un approccio comune come HTTP GET e analogamente modificate utilizzando un approccio coerente.
Una volta che uno sviluppatore acquisisce familiarità con una delle API, dovrebbe essere in grado di seguire un approccio simile per altre API.

## Client-server

Ciò significa essenzialmente che l'applicazione client e l'applicazione server DEVONO essere in grado di evolversi separatamente senza alcuna dipendenza l'una dall'altra. Un client dovrebbe conoscere solo gli URI delle risorse, e questo è tutto. Oggi, questa è una pratica normale nello sviluppo web, quindi non è richiesta alcuna fantasia da parte tua. Mantienilo semplice.
Server e client possono anche essere sostituiti e sviluppati in modo indipendente, a condizione che l'interfaccia tra loro non venga modificata.

## Stateless

Roy Fielding si è ispirato al protocollo HTTP, che di fatto è senza stato: stateless.

Uno dei principi dell'architettura REST è che tutte le interazioni client-server siano senza stato: il server non memorizzerà nulla sull'ultima richiesta HTTP effettuata dal client.
Tratterà ogni richiesta come nuova. Nessuna sessione, nessuna cronologia.

Se l'applicazione client deve mantenere stato memorizzato per l'utente finale, per esempio nei casi in cui l'utente accede una volta e fa successivamente altre operazioni autorizzate, ogni richiesta del client deve contenere tutte le informazioni necessarie per soddisfare la richiesta, tra cui autenticazione e autorizzazione.

Nessun contesto client deve essere memorizzato sul server tra le richieste.

Il client è responsabile della gestione dello stato dell'applicazione.

## cacheable

Nel mondo di oggi, la memorizzazione nella cache di dati e risposte è della massima importanza ovunque siano applicabili / possibili. La pagina Web che stai leggendo qui è anche una versione cache della pagina HTML. La memorizzazione nella cache comporta un miglioramento delle prestazioni per il lato client e un migliore ambito di scalabilità per un server perché il carico è stato ridotto.

In REST, la memorizzazione nella cache deve essere applicata alle risorse quando applicabile, e quindi queste risorse DEVONO dichiararsi memorizzabili nella cache. La memorizzazione nella cache può essere implementata sul server o sul lato client.
La memorizzazione nella cache ben gestita elimina parzialmente o completamente alcune interazioni client-server, migliorando ulteriormente la scalabilità e le prestazioni.

## Sistema a strati

REST consente di utilizzare un'architettura di sistema a più livelli in cui distribuire le API sul server A, archiviare i dati sul server B e autenticare le richieste nel server C, ad esempio. Un client non può normalmente dire se è collegato direttamente al server finale o a un intermediario lungo la strada.

## Codice su richiesta (opzionale)

Bene, questo vincolo è facoltativo. Il più delle volte, invierai le rappresentazioni statiche delle risorse sotto forma di XML o JSON. Ma quando è necessario, sei libero di restituire il codice eseguibile per supportare una parte della tua applicazione, ad esempio i clienti possono chiamare la tua API per ottenere un codice di rendering del widget dell'interfaccia utente. È permesso.
Tutti i vincoli di cui sopra ti aiutano a costruire un'API veramente RESTful e dovresti seguirli. Tuttavia, a volte, potresti trovarti a violare uno o due vincoli. Non preoccuparti; stai ancora creando un'API RESTful, ma non "veramente RESTful".

Si noti che tutti i vincoli di cui sopra sono strettamente correlati al WWW (il Web). Utilizzo di RESTful API, puoi fare la stessa cosa con i tuoi servizi web come fai con le pagine web.