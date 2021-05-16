# HTTP Status Code 5xx


* **500** – Internal **Server** Error – gli sviluppatori di API dovrebbero evitare questo errore. Se si verifica un errore globale dell’applicazione, lo stacktrace deve esere loggato e non inviato nella risposta all’utente.

## Classi di messaggi legati allo status-code 5xx


* **5xx** - Errore del **server**
Il **server** non è in grado di completare la richiesta a causa di un errore.

  * **500** - Errore interno del **server**. Questo messaggio di errore vene visualizzato per molti errori lato **server**. Nei registri del Visualizzatore eventi possono essere presenti ulteriori informazioni sulle cause di questo errore. È inoltre possibile disattivare i messaggi di errore HTTP brevi per visualizzare una descrizione più dettagliata dell'errore.
    * **500**.12 - Riavvio dell'applicazione in corso sul **server** Web.
    * **500**.13 - **Server** Web troppo impegnato.
    * **500**.15 - Richieste dirette per Global.asa non consentite.
    * **500**.16 - Credenziali di autorizzazione UNC non corrette. Questo codice di errore è specifico di IIS 6.0.
    * **500**.18 - Impossibile aprire l'archivio autorizzazioni URL. Questo codice di errore è specifico di IIS 6.0.
    * **500**.19 - I dati per il file sono configurati in modo non corretto nella metabase.
    * **500**.100 - Errore ASP interno.
  * **501** - La configurazione specificata dai valori intestazione non è implementata.
  * **502** - Il **server** Web con funzioni di gateway o di proxy ha ricevuto una risposta non valida.
      **502**.1 - Timeout dell'applicazione CGI.
    50  0-100.ASP - Errore ASP. Questo messaggio di errore viene visualizzato quando si tenta di caricare una pagina ASP nel cui codice sono presenti errori. Per informazioni più dettagliate sull'errore, disattivare i messaggi di errore HTTP brevi. Per impostazione predefinita, questo errore è attivato solo per il sito Web predefinito.
    * **500**.12 - Riavvio dell'applicazione in corso. Indica che si è tentato di caricare una pagina ASP durante il riavvio dell'applicazione da parte di IIS. Il messaggio non dovrebbe essere più visualizzato quando si aggiorna la pagina. Se si aggiorna la pagina e il messaggio continua a essere visualizzato, la causa potrebbe essere l'esecuzione della scansione del file Global.asa da parte del software antivirus.
    * **500**.19 - Questo errore viene visualizzato quando la metabase XML contiene informazioni di configurazione non valide per il tipo di contenuto al quale si tenta di accedere. Per risolvere il problema, rimuovere o correggere la configurazione non valida. Questo problema indica in genere un problema nella chiave della metabase ScriptMap.
  * **502** - Gateway non valido. Questo messaggio di errore viene visualizzato quando si tenta di eseguire uno script CGI che non restituisce un set valido di intestazioni HTTP. Per risolvere il problema, è necessario eseguire il debug dell'applicazione CGI per stabilire il motivo per il quale sono state passate informazioni HTTP non valide a IIS.
      **502**.2 - Errore nell'applicazione CGI.
  * **503** - Servizio non disponibile. A partire da IIS 6, il componente HTTP.sys in modalità kernel produce uno stato HTTP 503.
  * **504** - Timeout del gateway.
  * **505** - Versione HTTP non supportata.


[< back](061_HttpStatusCode_0.md)