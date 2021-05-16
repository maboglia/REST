# Come funzionano le **API RESTful**

Un'**API RESTful** suddivide una transazione per creare una serie di piccoli moduli.
Ogni modulo affronta una parte sottostante particolare della transazione. 
Questa modularità offre agli sviluppatori molta flessibilità, ma può essere difficile per gli sviluppatori progettare la loro API REST da zero.
Attualmente, diverse aziende forniscono modelli che gli sviluppatori possono usare.

Un'**API RESTful** utilizza le metodologie **HTTP** esistenti definite dal protocollo _RFC 2616_. Usano **GET** per recuperare una risorsa; **PUT** per cambiare lo stato o aggiornare una risorsa, che può essere un oggetto, un file o un'altra qualsiasi risorsa; **POST** per creare quella risorsa; e **DELETE** per rimuoverlo.

Con **REST**, i componenti in rete sono una risorsa a cui l'utente richiede l'accesso - una scatola nera i cui dettagli di implementazione non sono noti. Tutte le chiamate sono stateless; nulla può essere trattenuto dal servizio **RESTful** tra le esecuzioni.

Poiché le chiamate sono **senza stato**, **REST** è utile nelle applicazioni **cloud**. I componenti senza stato possono essere ridistribuiti liberamente in caso di errore e possono adattarsi alle modifiche del carico. Questo perché qualsiasi richiesta può essere indirizzata a qualsiasi istanza di un componente; non può esserci nulla di salvato che deve essere ricordato dalla transazione successiva. 

Ciò rende **REST** preferibile per l'uso sul Web, ma il modello **RESTful** è utile anche nei servizi **cloud** perché il collegamento a un servizio tramite un'API è una questione di controllo del modo in cui l'URL viene decodificato. 

Il **cloud** computing e i microservizi sono quasi certi di rendere la progettazione di **API RESTful** la regola in futuro.

## Vincoli di progettazione e architettura **API RESTful**

Il design dell'**API RESTful** è stato definito dal **Dr. Roy Fielding** nella sua tesi di dottorato del 2000. Per essere una vera **API RESTful**, un servizio Web deve rispettare i seguenti **sei vincoli architetturali** REST:

* **[Client-server](050_Principi_ClientServer.md)**
* **[Stateless](051_Principi_Stateless.md)**
* **[Memorizzabile nella cache](052_Principi_Cacheable.md)**
* **[Interfaccia uniforme](053_Principi_InterfacciaUniforma.md)**
* **[Sistema a livelli](054_Principi_LayerSystem.md)**
* **[Codice su richiesta](055_Principi_CodeOnDemand.md)** (opzionale)

