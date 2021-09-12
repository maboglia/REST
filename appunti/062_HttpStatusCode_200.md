# HTTP Status Code 2xx 

* **200** – OK – Tutto bene
* **201** – OK – E’ stata creata una nuova risorsa
* **204** – OK – La risorsa è stata cancellata con successo

---

## Classi di messaggi legati allo status-code 2xx

Risposte di successo

* **200** OK
    La richiesta è andata a buon fine. Il significato del successo dipende dal metodo HTTP:

    * **GET**: la risorsa è stata recuperata e viene trasmessa nel corpo del messaggio.
    * **HEAD**: le intestazioni dell'entità si trovano nel corpo del messaggio.
    * **PUT** o POST: la risorsa che descrive il risultato dell'azione viene trasmessa nel corpo del messaggio.
    * **TRACE**: il corpo del messaggio contiene il messaggio di richiesta ricevuto dal server.

---

* **201** Creato
    La richiesta è riuscita e di conseguenza è stata creata una nuova risorsa. Questa è in genere la risposta inviata dopo le richieste POST o alcune richieste PUT.
* **202** Accettato
    La richiesta è stata ricevuta ma non ha ancora dato seguito. Non è vincolante, poiché non è possibile in HTTP inviare in un secondo momento una risposta asincrona che indichi l'esito della richiesta. È inteso per i casi in cui un altro processo o server gestisce la richiesta o per l'elaborazione in batch.
* **203** Informazioni non autorevoli
    Questo codice di risposta indica che le meta-informazioni restituite non sono esattamente le stesse disponibili dal server di origine, ma vengono raccolte da una copia locale o di terze parti. Viene utilizzato principalmente per mirror o backup di un'altra risorsa. Ad eccezione di quel caso specifico, la risposta "200 OK" è preferibile a questo stato.
* **204** Nessun contenuto
    Non ci sono contenuti da inviare per questa richiesta, ma le intestazioni possono essere utili. Lo user-agent può aggiornare le sue intestazioni memorizzate nella cache per questa risorsa con quelle nuove.


---


* **205** Reimposta contenuto
    Dice allo user-agent di reimpostare il documento che ha inviato questa richiesta.
* **206** Contenuto parziale
    Questo codice di risposta viene utilizzato quando l'intestazione Range viene inviata dal client per richiedere solo una parte di una risorsa.
* **207** Multi-Stato (WebDAV)
    Trasmette informazioni su più risorse, per situazioni in cui potrebbero essere appropriati più codici di stato.
* **208** già segnalato (WebDAV)
    Utilizzato all'interno di un elemento di risposta `<dav: propstat>` per evitare di enumerare ripetutamente i membri interni di più associazioni alla stessa raccolta.
* **226** IM utilizzato (codifica HTTP Delta)
    Il server ha soddisfatto una richiesta GET per la risorsa e la risposta è una rappresentazione del risultato di una o più manipolazioni dell'istanza applicate all'istanza corrente.
[< back](061_HttpStatusCode_0.md)