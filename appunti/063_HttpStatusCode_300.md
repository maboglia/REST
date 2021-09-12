# **HTTP** Status Code 3xx

* **304** – Not modified – I dati non sono cambiati. Il cliente può utilizzare i dati nella **cache**

---

## Classi di messaggi legati allo status-code 3xx

Messaggi di reindirizzamento

* **300** Scelta multipla
    La richiesta ha più di una possibile risposta. Lo user-agent o l'utente dovrebbe sceglierne uno. (Non esiste un modo standardizzato per scegliere una delle risposte, ma si consigliano collegamenti HTML alle possibilità in modo che l'utente possa scegliere.)
* **301** Spostato in modo permanente
    L'URL della risorsa richiesta è stato modificato in modo permanente. Il nuovo URL viene fornito nella risposta.
* **302** Found
    Questo codice di risposta indica che l'**URI** della risorsa richiesta è stato modificato temporaneamente. In futuro potrebbero essere apportate ulteriori modifiche all'**URI**. Pertanto, questo stesso **URI** dovrebbe essere utilizzato dal client nelle richieste future.
* **303** Vedi altro
    Il server ha inviato questa risposta per indicare al client di ottenere la risorsa richiesta in un altro **URI** con una richiesta **GET**.

---

* **304** Non modificato
    Viene utilizzato per scopi di memorizzazione nella **cache**. Indica al client che la risposta non è stata modificata, quindi il client può continuare a utilizzare la stessa versione memorizzata nella **cache** della risposta.
* **305** Usa proxy (deprecato!)

    Definito in una versione precedente della specifica **HTTP** per indicare che una risposta richiesta deve essere accessibile da un proxy. È stato deprecato a causa di problemi di sicurezza relativi alla configurazione in banda di un proxy.
* **306** inutilizzato
    Questo codice di risposta non è più utilizzato; è solo riservato. È stato utilizzato in una versione precedente della specifica **HTTP** / 1.1.
* **307** Reindirizzamento temporaneo
    Il server invia questa risposta per indicare al client di ottenere la risorsa richiesta su un altro **URI** con lo stesso metodo utilizzato nella richiesta precedente. Questo ha la stessa semantica del codice di risposta **HTTP** 302 Found, con l'eccezione che l'agente utente non deve modificare il metodo **HTTP** utilizzato: se un **POST** è stato utilizzato nella prima richiesta, un **POST** deve essere utilizzato nella seconda richiesta.
* **308** Reindirizzamento permanente
    Ciò significa che la risorsa si trova ora permanentemente in un altro **URI**, specificato dall'intestazione `Location: HTTP Response`. Questo ha la stessa semantica del codice di risposta **HTTP** 301 spostato permanentemente, con l'eccezione che il programma utente non deve cambiare il metodo **HTTP** utilizzato: se un **POST** è stato utilizzato nella prima richiesta, un **POST** deve essere utilizzato nella seconda richiesta.

[< back](061_HttpStatusCode_0.md)