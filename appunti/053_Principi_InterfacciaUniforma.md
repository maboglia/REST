# Interfaccia uniforme

**Interfaccia uniforme**: applicando il principio di ingegneria del software di generalità all'interfaccia del componente, l'architettura generale del sistema è semplificata e la visibilità delle interazioni è migliorata. Per ottenere un'interfaccia uniforme, sono necessari più vincoli architetturali per guidare il comportamento dei componenti. Il REST è definito da quattro vincoli di interfaccia: identificazione delle risorse; manipolazione delle risorse attraverso rappresentazioni; messaggi auto-descrittivi; e, hypermedia come motore dello stato dell'applicazione.

* Utilizzo di un'**interfaccia uniforme** (UI). Le risorse dovrebbero essere identificabili in modo univoco tramite un singolo URL e solo utilizzando i metodi sottostanti del protocollo di rete, come DELETE, PUT e GET con HTTP, dovrebbe essere possibile manipolare una risorsa.



Poiché si applica il nome stesso del vincolo, DEVI decidere l'interfaccia API per le risorse all'interno del sistema che sono esposte ai consumatori API e seguono religiosamente. Una risorsa nel sistema dovrebbe avere un solo URI logico e ciò dovrebbe fornire un modo per recuperare dati correlati o aggiuntivi. È sempre meglio sinonimizzare una risorsa con una pagina web.

Ogni singola risorsa non dovrebbe essere troppo grande e contenere ogni cosa nella sua rappresentazione. Se pertinente, una risorsa deve contenere collegamenti (HATEOAS) che puntano a URI relativi per recuperare informazioni correlate.

Inoltre, le rappresentazioni delle risorse nel sistema dovrebbero seguire linee guida specifiche come convenzioni di denominazione, formati di collegamento o formato dei dati (XML o / e JSON).

Tutte le risorse dovrebbero essere accessibili attraverso un approccio comune come HTTP GET e analogamente modificate utilizzando un approccio coerente.
Una volta che uno sviluppatore acquisisce familiarità con una delle API, dovrebbe essere in grado di seguire un approccio simile per altre API.

4. interfaccia uniforme
Per avere un caching efficiente in una rete, i componenti devono essere in grado di comunicare tramite un’interfaccia uniforme. Con un’interfaccia uniforme, il carico utile può essere trasferito in un formato standard.
4.1. Identificazione delle risorse
Una risorsa è un oggetto o la rappresentazione di qualcosa di significativo nel dominio applicativo. È possibile interagire con le risorse attraverso le API. Esempi di entità? Un Libro, un Ordine, un Post e qualsiasi altra entità che si può astrarre da un determinato contesto. Il concetto di risorsa è quindi molto simile a quello di oggetto nel mondo della programmazione ad oggetti.
4.2. Manipolazione delle risorse attraverso rappresentazioni
Una risorsa può essere rappresentata in molti modi diversi.
Ad esempio come HTML, XML, JSON o anche come file JPEG.
Questa regola significa che i clienti interagiscono con le risorse tramite le loro rappresentazioni, il che è un modo potente per mantenere i concetti di risorse astratti dalle loro interazioni. La rappresentazione più famosa utilizzata nelle implementazioni REST è il JSON . 
4.3  Hypermedia deve essere il motore dello stato dell’applicazione
Ciò significa solo che l’applicazione deve essere guidata da collegamenti, consentendo ai clienti di scoprire risorse tramite collegamenti ipertestuali. Come si può notare, molte di queste regole possono essere implementate nel protocollo HTTP. Pertanto, quando un’API utilizza correttamente HTTP, è un enorme passo avanti verso RESTful.