# Autenticazione

Alcune API sono disponibili sul web in maniera aperta: qualsiasi sistema può recuperare i dati senza autorizzazione. Questo non è praticabile per le API che accedono a dati privati ​​o che consentono richieste di aggiornamento ed eliminazione.

Le applicazioni lato client **sullo stesso dominio dell'API RESTful** invieranno e riceveranno cookie proprio come qualsiasi altra richiesta HTTP. (Si noti che fetch() nei browser meno recenti richiede l'impostazione dell'opzione init credenziali.) È quindi **possibile convalidare una richiesta API** per garantire che un utente abbia effettuato l'accesso e disponga dei diritti appropriati.

Le **applicazioni di terze parti** devono utilizzare metodi di autorizzazione alternativi. Le opzioni di autenticazione comuni includono:

* **Autenticazione di base HTTP**. Un'intestazione di autorizzazione HTTP contenente un nome utente con codifica base64: la stringa della password viene passata nell'intestazione della richiesta.
* **Chiavi API**. A un'applicazione di terze parti viene concessa l'autorizzazione per utilizzare un'API emettendo una chiave che può avere diritti specifici o essere limitata a un determinato dominio. La chiave viene passata in ogni richiesta nell'intestazione HTTP o nella stringa di query.
* **OAuth**. Un token viene ottenuto prima di poter effettuare qualsiasi richiesta inviando un ID client e possibilmente un client segreto a un server OAuth. Il token OAuth viene quindi inviato con ogni richiesta API fino alla scadenza.
* **Token Web JSON** (JWT). I token di autenticazione con firma digitale vengono trasmessi in modo sicuro nell'intestazione sia della richiesta che della risposta.

L'autenticazione API varia in base al contesto d'uso. In alcuni casi, l'applicazione di terze parti viene considerata come un altro utente connesso con diritti e autorizzazioni specifici, ad esempio quando si generano indicazioni stradali da un'API di mappe. In altri casi, l'applicazione di terze parti viene utilizzata da un utente registrato e può accedere solo ai suoi dati, ad esempio quando si recuperano contenuti e documenti e-mail.

