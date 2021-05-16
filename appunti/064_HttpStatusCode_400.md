# HTTP Status Code 4xx

* **400** – Bad Request – Richiesta non valida. L’errore esatto dovrebbe essere spiegato nel payload dell’ errore (di cui ne parleremo a breve). Per esempio. “Il JSON non è valido”
* **401** – Unauthorized – La richiesta richiede una autenticazione dell’utente
* **403** – Forbidden – Il server ha capito la richiesta, ma in base ai diritti del richiedente l’accesso non è consentito.
* **404** – Not Found – Non vi è alcuna risorsa dietro l’URI richiesto.
* **422** – Unprocessable Entity – deve essere usato se il server non può elaborare il enitity, ad esempio se un’immagine non può essere formattata o campi obbligatori sono mancanti nel payload.

## Classi di messaggi legati allo status-code

Risposte di errore del client

* **400** Bad Request
    Il server non è riuscito a comprendere la richiesta a causa di una sintassi non valida.
* **401** Non autorizzato
    Sebbene lo standard HTTP specifichi "non autorizzato", semanticamente questa risposta significa "non autenticato". Cioè, il client deve autenticarsi per ottenere la risposta richiesta.
* **402** Pagamento richiesto

    Questo codice di risposta è riservato per uso futuro. L'obiettivo iniziale per creare questo codice era utilizzarlo per i sistemi di pagamento digitale, tuttavia questo codice di stato viene utilizzato molto raramente e non esiste alcuna convenzione standard.
* **403** Proibito
    Il cliente non dispone dei diritti di accesso al contenuto; cioè, non è autorizzato, quindi il server si rifiuta di fornire la risorsa richiesta. A differenza di 401, l'identità del client è nota al server.
* **404** non trovato
    Il server non riesce a trovare la risorsa richiesta. Nel browser, questo significa che l'URL non viene riconosciuto. In un'API, questo può anche significare che l'endpoint è valido ma la risorsa stessa non esiste. I server possono anche inviare questa risposta invece di 403 per nascondere l'esistenza di una risorsa a un client non autorizzato. Questo codice di risposta è probabilmente il più famoso a causa della sua frequente presenza sul web.
* **405** Metodo non consentito
    Il metodo di richiesta è noto al server ma è stato disabilitato e non può essere utilizzato. Ad esempio, un'API potrebbe vietare l'eliminazione di una risorsa. I due metodi obbligatori, GET e HEAD, non devono mai essere disabilitati e non devono restituire questo codice di errore.
* **406** Non accettabile
    Questa risposta viene inviata quando il server Web, dopo aver eseguito la negoziazione del contenuto guidata dal server, non trova alcun contenuto conforme ai criteri forniti dall'agente utente.
* **407** Autenticazione proxy richiesta
    È simile a 401 ma l'autenticazione deve essere eseguita da un proxy.
* **408** Timeout richiesta
    Questa risposta viene inviata su una connessione inattiva da alcuni server, anche senza alcuna precedente richiesta da parte del client. Significa che il server vorrebbe chiudere questa connessione inutilizzata. Questa risposta viene utilizzata molto di più poiché alcuni browser, come Chrome, Firefox 27+ o IE9, utilizzano meccanismi di pre-connessione HTTP per velocizzare la navigazione. Notare inoltre che alcuni server interrompono semplicemente la connessione senza inviare questo messaggio.
* **409** Conflitto
    Questa risposta viene inviata quando una richiesta è in conflitto con lo stato corrente del server.
* **410** Gone
    Questa risposta viene inviata quando il contenuto richiesto è stato eliminato definitivamente dal server, senza indirizzo di inoltro. Ci si aspetta che i client rimuovano le proprie cache e i collegamenti alla risorsa. La specifica HTTP prevede che questo codice di stato venga utilizzato per "servizi promozionali a tempo limitato". Le API non dovrebbero sentirsi obbligate a indicare le risorse che sono state eliminate con questo codice di stato.
* **411** Lunghezza richiesta
    Il server ha rifiutato la richiesta perché il campo dell'intestazione Content-Length non è definito e il server lo richiede.
* **412** Precondizione non riuscita
    Il client ha indicato le precondizioni nelle sue intestazioni che il server non soddisfa.
* **413** Carico utile troppo grande
    L'entità richiesta è maggiore dei limiti definiti dal server; il server potrebbe chiudere la connessione o restituire un campo di intestazione Retry-After.
* **414** URI troppo lungo
    L'URI richiesto dal client è più lungo di quanto il server sia disposto a interpretare.
* **415** Tipo di supporto non supportato
    Il formato multimediale dei dati richiesti non è supportato dal server, quindi il server rifiuta la richiesta.
* **416** Gamma non soddisfacente
    L'intervallo specificato dal campo di intestazione Intervallo nella richiesta non può essere soddisfatto; è possibile che l'intervallo sia al di fuori della dimensione dei dati dell'URI di destinazione.
* **417** Aspettativa fallita
    Questo codice di risposta indica che l'aspettativa indicata dal campo di intestazione della richiesta Expect non può essere soddisfatta dal server.
* **418** Sono una teiera
    Il cameriere rifiuta il tentativo di preparare il caffè con una teiera.
* **421** Richiesta errata
    La richiesta è stata indirizzata a un server che non è in grado di produrre una risposta. Questo può essere inviato da un server che non è configurato per produrre risposte per la combinazione di schema e autorità inclusa nell'URI della richiesta.
* **422** Entità non elaborabile (WebDAV)
    La richiesta era ben formata ma non è stato possibile seguirla a causa di errori semantici.
* **423** bloccato (WebDAV)
    La risorsa a cui si accede è bloccata.
* **424** Dipendenza non riuscita (WebDAV)
    La richiesta non è riuscita a causa del fallimento di una richiesta precedente.
* **425** Troppo presto
    Indica che il server non è disposto a rischiare di elaborare una richiesta che potrebbe essere riprodotta.
* **426** Aggiornamento richiesto
    Il server rifiuta di eseguire la richiesta utilizzando il protocollo corrente, ma potrebbe essere disposto a farlo dopo che il client è stato aggiornato a un protocollo diverso. Il server invia un'intestazione di aggiornamento in una risposta 426 per indicare i protocolli richiesti.
* **428** Presupposto richiesto
    Il server di origine richiede che la richiesta sia condizionale. Questa risposta ha lo scopo di prevenire il problema di "aggiornamento perso", in cui un client OTTIENE lo stato di una risorsa, la modifica e la RIMETTE al server, quando nel frattempo una terza parte ha modificato lo stato sul server, portando a un conflitto.
* **429** Troppe richieste
     L'utente ha inviato troppe richieste in un determinato periodo di tempo ("limitazione della velocità").
* **431** Campi intestazione richiesta troppo grandi
     Il server non è disposto a elaborare la richiesta perché i suoi campi di intestazione sono troppo grandi. La richiesta può essere inviata nuovamente dopo aver ridotto le dimensioni dei campi di intestazione della richiesta.
* **451** Non disponibile per motivi legali
     Lo user-agent ha richiesto una risorsa che non può essere fornita legalmente, come una pagina web censurata da un governo.

[< back](061_HttpStatusCode_0.md)

