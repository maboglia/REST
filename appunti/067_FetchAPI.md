# Fetch API

L'API Fetch fornisce un'interfaccia per il recupero delle risorse (anche attraverso la rete). Sembrerà familiare a chiunque abbia utilizzato XMLHttpRequest, ma la nuova API fornisce un set di funzionalità più potente e flessibile.

Nota: questa funzione è disponibile in Web Workers.

---

Concetti e utilizzo

Fetch fornisce una definizione generica degli oggetti Request e Response (e altre cose coinvolte nelle richieste di rete). Ciò consentirà loro di essere utilizzati ovunque siano necessari in futuro, che si tratti di lavoratori del servizio, API della cache e altre cose simili che gestiscono o modificano richieste e risposte o qualsiasi tipo di caso d'uso che potrebbe richiedere la generazione delle risposte programmaticamente (ovvero, l'uso di programmi per computer o istruzioni di programmazione personali).

Definisce anche concetti correlati come CORS e la semantica dell'intestazione HTTP Origin, soppiantando le loro definizioni separate altrove.

Per effettuare una richiesta e recuperare una risorsa, utilizzare il metodo WindowOrWorkerGlobalScope.fetch (). È implementato in più interfacce, in particolare Window e WorkerGlobalScope. Questo lo rende disponibile praticamente in qualsiasi contesto in cui potresti voler recuperare le risorse.

---

Il metodo fetch () accetta un argomento obbligatorio, il percorso della risorsa che si desidera recuperare. Restituisce una promessa che si risolve nella risposta a quella richiesta, non appena il server risponde con le intestazioni, anche se la risposta del server è uno stato di errore HTTP. Puoi anche opzionalmente passare un oggetto opzioni di inizializzazione come secondo argomento (vedi Richiesta).

Una volta recuperata una risposta, sono disponibili numerosi metodi per definire qual è il contenuto del corpo e come deve essere gestito (vedere Corpo).

È possibile creare una richiesta e una risposta direttamente utilizzando i costruttori Request () e Response (), ma è raro farlo direttamente. È invece più probabile che vengano creati come risultato di altre azioni API (ad esempio, FetchEvent.respondWith () da service worker).

---

## Differenze da jQuery

La specifica fetch differisce da jQuery.ajax () in tre modi principali:

* La promessa restituita da fetch () non rifiuterà sullo stato di errore HTTP anche se la risposta è HTTP 404 o 500. Invece, si risolverà normalmente (con lo stato ok impostato su false) e rifiuterà solo in caso di errore di rete o se qualcosa ha impedito il completamento della richiesta.
* fetch () non invierà cookie cross-origin a meno che non imposti l'opzione di inizializzazione delle credenziali (da includere).
  *  Nell'aprile 2018, la specifica ha modificato la politica delle credenziali predefinite in "stessa origine". I seguenti browser hanno fornito un recupero nativo obsoleto e sono stati aggiornati in queste versioni: Firefox 61.0b13, Safari 12, Chrome 68.
  * Se scegli come target versioni precedenti di questi browser, assicurati di includere le credenziali: opzione di inizializzazione "stessa origine" su tutte le richieste API che potrebbero essere influenzate dai cookie / dallo stato di accesso dell'utente.

