# REST vs. SOAP

**REST** e Simple Object Access Protocol (**SOAP**) offrono diversi metodi per invocare un servizio web. 

**REST** è uno stile architettonico, mentre **SOAP** definisce una specifica standard del protocollo di comunicazione per lo scambio di messaggi basato su XML. Le applicazioni **REST** possono usare **SOAP**.

I servizi Web **RESTful** sono stateless. Un'implementazione basata su **REST** è semplice rispetto a **SOAP**, ma gli utenti devono comprendere il contesto e il contenuto trasmessi, in quanto non esiste un insieme standard di regole per descrivere l'interfaccia dei servizi Web **REST**. I servizi **REST** sono sono facili da integrare con i siti Web esistenti e sono utili per i dispositivi mobili per l'uso ridotto della banda.

---

**SOAP** richiede un codice infrastrutturale di basso livello che collega i moduli di codice principali insieme rispetto alla progettazione dei servizi **REST**. 

Il linguaggio di descrizione dei servizi Web descrive un insieme comune di regole per definire i messaggi, i collegamenti, le operazioni e la posizione del servizio. I servizi Web **SOAP** sono utili per l'elaborazione e l'invocazione asincroni.


Prima di **REST**, gli sviluppatori utilizzavano **SOAP** per integrare le API. Per effettuare una chiamata, gli sviluppatori hanno scritto a mano un documento XML con una chiamata RPC (Remote Procedure Call) nel corpo. Hanno quindi specificato l'endpoint e POST la loro busta **SOAP** sull'endpoint.
