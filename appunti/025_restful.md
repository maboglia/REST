# Cos'è REST

REST è l'acronimo di REpresentational State Transfer. È uno stile architettonico per sistemi ipermediali distribuiti ed è stato presentato per la prima volta da Roy Fielding nel 2000 nella sua tesi di dottorato.

Come ogni altro stile architettonico, anche REST ha i suoi vincoli che devono essere soddisfatti se un'interfaccia deve essere definita RESTful. Questi principi sono elencati di seguito.

## Principi guida di REST

* **Client-server** - Separando le preoccupazioni dell'interfaccia utente dalle preoccupazioni relative alla memorizzazione dei dati, miglioriamo la portabilità dell'interfaccia utente su più piattaforme e miglioriamo la scalabilità semplificando i componenti del server.

* **Stateless**: ogni richiesta dal client al server deve contenere tutte le informazioni necessarie per comprendere la richiesta e non può sfruttare alcun contesto memorizzato sul server. Lo stato della sessione viene quindi mantenuto interamente sul client.
    
* **Memorizzabile nella cache**: i vincoli della cache richiedono che i dati all'interno di una risposta a una richiesta siano etichettati in modo implicito o esplicito come memorizzabili nella cache o non memorizzabili nella cache. Se una risposta è memorizzabile nella cache, una cache client ha il diritto di riutilizzare i dati di risposta per richieste successive ed equivalenti.
    
* **Interfaccia uniforme**: applicando il principio di ingegneria del software di generalità all'interfaccia del componente, l'architettura generale del sistema è semplificata e la visibilità delle interazioni è migliorata. Per ottenere un'interfaccia uniforme, sono necessari più vincoli architetturali per guidare il comportamento dei componenti. Il REST è definito da quattro vincoli di interfaccia: identificazione delle risorse; manipolazione delle risorse attraverso rappresentazioni; messaggi auto-descrittivi; e, hypermedia come motore dello stato dell'applicazione.
    
* **Sistema a livelli**: lo stile di sistema a livelli consente a un'architettura di essere composta da livelli gerarchici vincolando il comportamento dei componenti in modo tale che ciascun componente non possa "vedere" oltre il livello immediato con cui interagiscono.
    
* **Codice su richiesta** (opzionale) - REST consente di estendere le funzionalità del client scaricando ed eseguendo il codice sotto forma di applet o script. Ciò semplifica i client riducendo il numero di funzionalità necessarie per essere pre-implementate.

## Risorsa

L'astrazione chiave delle informazioni in REST è una **risorsa**. Qualsiasi informazione che può essere nominata può essere una **risorsa**: un documento o un'immagine, un servizio temporale, una raccolta di altre risorse, un oggetto non virtuale (ad esempio una persona) e così via. REST utilizza un identificatore di **risorsa** per identificare la particolare **risorsa** coinvolta in un'interazione tra componenti.

Lo stato della **risorsa** in qualsiasi data e ora è noto come rappresentazione delle risorse. Una rappresentazione è costituita da dati, metadati che descrivono i dati e collegamenti ipertestuali che possono aiutare i client a passare al successivo stato desiderato.

Il formato dei dati di una rappresentazione è noto come tipo di supporto. Il tipo di supporto identifica una specifica che definisce come deve essere elaborata una rappresentazione. Un'API veramente RESTful sembra ipertesto. Ogni unità di informazioni indirizzabile reca un indirizzo, esplicitamente (ad esempio, attributi link e id) o implicitamente (ad esempio, derivato dalla definizione del tipo di supporto e dalla struttura di rappresentazione).

## Secondo Roy Fielding:

* R. Fielding: contributor del protocollo HTTP nonché cofondatore del progetto Apache HTTP Server

Ipertesto (o **hypermedia**) significa la **presentazione simultanea di informazioni e controlli** in modo tale che l'informazione diventi lo strumento attraverso il quale l'utente (o automa) ottiene le scelte e seleziona le azioni. Ricorda che l'ipertesto non deve essere HTML (o XML o JSON) su un browser. Le macchine possono seguire i collegamenti quando comprendono il formato dei dati e i tipi di relazione.

Inoltre, **le rappresentazioni delle risorse devono essere auto-descrittive**: il client non ha bisogno di sapere se una **risorsa** è dipendente o dispositivo. Dovrebbe agire sulla base del tipo di supporto associato alla **risorsa**. Quindi, in pratica, finirai per creare molti tipi di media personalizzati, normalmente un tipo di media associato a una **risorsa**.

Ogni tipo di supporto definisce un modello di elaborazione predefinito. Ad esempio, HTML definisce un processo di rendering per l'ipertesto e il comportamento del browser attorno a ciascun elemento. Non ha alcuna relazione con i metodi di **risorsa** **GET** / **PUT** / **POST** / **DELETE** ... a parte il fatto che alcuni elementi del tipo di supporto definiranno un modello di processo che va come "gli elementi di ancoraggio con un attributo href creano un collegamento ipertestuale che, quando selezionato, invoca una richiesta di recupero (GET) sull'URI corrispondente all'attributo href con codifica CDATA. "

## Metodi di risorsa

Un'altra cosa importante associata al REST sono i metodi delle risorse da utilizzare per eseguire la transizione desiderata. Un gran numero di persone riferisce erroneamente i metodi delle risorse ai metodi HTTP **GET** / **PUT** / **POST** / **DELETE**.

Roy Fielding non ha mai menzionato alcuna raccomandazione su quale metodo utilizzare in quale condizione. Tutto ciò che sottolinea è che dovrebbe essere un'interfaccia uniforme. Se decidi che HTTP POST verrà utilizzato per l'aggiornamento di una risorsa - piuttosto che la maggior parte delle persone consiglia HTTP PUT - va bene e l'interfaccia dell'applicazione sarà RESTful.

Tutto ciò che è necessario per modificare lo stato delle risorse deve far parte della risposta API per quella risorsa, inclusi i metodi e in quale stato lasceranno la rappresentazione.

Un'API REST deve essere immessa senza alcuna conoscenza precedente oltre l'URI iniziale (segnalibro) e un set di tipi di media standardizzati appropriati per il pubblico previsto (ovvero, che dovrebbe essere compreso da qualsiasi client che potrebbe utilizzare l'API). Da quel momento in poi, tutte le transizioni dello stato dell'applicazione devono essere guidate dalla selezione del client delle scelte fornite dal server che sono presenti nelle rappresentazioni ricevute o implicite dalla manipolazione dell'utente di tali rappresentazioni. Le transizioni possono essere determinate (o limitate da) la conoscenza del client dei tipi di media e dei meccanismi di comunicazione delle risorse, entrambi i quali possono essere migliorati al volo (ad esempio, il codice su richiesta).
    
[Il fallimento qui implica che le informazioni fuori banda stanno guidando l'interazione anziché l'ipertesto.]

Un'altra cosa che ti aiuterà durante la creazione di API RESTful è che i risultati API basati su query dovrebbero essere rappresentati da un elenco di collegamenti con informazioni di riepilogo, non da array di rappresentazioni di risorse originali perché la query non sostituisce l'identificazione delle risorse.


## REST != HTTP

Molte persone preferiscono assimilare HTTP con REST:
REST e HTTP non sono la stessa cosa!

La confusione nasce dal fatto che REST intende anche rendere il web più snello e standardizzato, sostiene l'utilizzo più rigoroso dei principi REST anche per internet.

Roy Fielding, nella sua tesi di dottorato, non ha mai menzionato alcuna direttiva di implementazione, comprese le preferenze di protocollo e HTTP. Se si seguono i 6 principi guida di REST, si può definire l'interfaccia come **RESTful**.

In parole più semplici, nello stile architettonico REST, **i dati e le funzionalità sono considerati risorse** e sono accessibili tramite gli Uniform Resource Identifier (**URI**). Le risorse vengono gestite utilizzando una serie di operazioni semplici e ben definite. I client e i server si scambiano rappresentazioni di risorse utilizzando un'interfaccia e un protocollo standardizzati, in genere HTTP.

**Le risorse sono disaccoppiate dalla loro rappresentazione** in modo che sia possibile accedere al loro contenuto in una varietà di formati, come HTML, XML, testo normale, PDF, JPEG, JSON e altri. I metadati sulla risorsa sono disponibili e utilizzati, ad esempio, per controllare la memorizzazione nella cache, rilevare errori di trasmissione, negoziare il formato di rappresentazione appropriato ed eseguire l'autenticazione o il controllo dell'accesso. E, soprattutto, ogni interazione con una risorsa è stateless.

Tutti questi principi aiutano le applicazioni RESTful ad essere semplici, leggere e veloci.

Riferimenti:

http://roy.gbiv.com/untangled/2008/rest-apis-must-be-hypertext-driven
http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm