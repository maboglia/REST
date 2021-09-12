# **REST**

**REST** (**REpresentational State Transfer**) è una tipologia di archittettura software per sistemi client-server, il cui principio fondamentale è la separazione dei compiti fra le componenti distribuite del sistema, in modo da semplificarne l’implementazione eliminando ogni interdipendenza tra le stesse.

---


L’approccio proposto prevede che il sistema venga progettato seguendo i seguenti principi:

* I dati e le funzionalità dell’applicazione devono essere rappresentate come **risorse**;
* Ogni **risorsa** deve essere **univocamente identificabile e indirizzabile**, solitamente tramite l’uso di **URL**;
* Le **risorse** devono essere accessibili attraverso un’interfaccia comune tra le varie componenti distribuite, che permetta di definire delle operazioni eseguibili.

*L’approccio **REST** è **puramente concettuale** e implementabile con qualsiasi tecnologia e protocollo ne permetta di soddisfare i requisiti.*

---



**REST** è la tecnologia di servizio web più utilizzata! 

**REST** è un modo per due sistemi di computer di comunicare su HTTP in modo simile a **browser** Web e **server**.

La **condivisione di dati** tra due o più sistemi è sempre stata un requisito fondamentale per lo sviluppo del software. 

---
# Cos'è REST

REST è l'acronimo di **REpresentational State Transfer**. È uno stile architettonico per sistemi ipermediali distribuiti ed è stato presentato per la prima volta da Roy Fielding nel 2000 nella sua tesi di dottorato.

Come ogni altro stile architettonico, anche REST ha i suoi vincoli che devono essere soddisfatti se un'interfaccia deve essere definita RESTful. Questi principi sono elencati di seguito.

---


## Principi guida (vincoli di REST)

* **[Client-server](050_Principi_ClientServer.md)**
* **[Stateless](051_Principi_Stateless.md)**
* **[Memorizzabile nella cache](052_Principi_Cacheable.md)**
* **[Interfaccia uniforme](053_Principi_InterfacciaUniforma.md)**
* **[Sistema a livelli](054_Principi_LayerSystem.md)**
* **[Codice su richiesta](055_Principi_CodeOnDemand.md)** (opzionale)

---


### Esempio di REST

Apri il seguente link nel tuo browser per richiedere un commento casuale su argomento programmazione:

`curl "https://official-joke-api.appspot.com/jokes/programming/random"`

Questa è un'**API** pubblica implementata come servizio web RESTful (segue le convenzioni REST). Il tuo browser mostrerà una terribile battuta di programmazione in formato **JSON**, come:

---


```JSON
[
  {
    "id": 29,
    "type": "programming",
    "setup": "There are 10 types of people in this world...",
    "punchline": "Those who understand binary and those who don't"
  }
]
```

---


Le librerie client **HTTP** sono disponibili in tutte le lingue e runtime più diffusi, tra cui **Fetch** in **JavaScript** e **file_get_contents()**  in **PHP**. Una risposta **JSON** è leggibile da una macchina in modo che possa essere analizzata e prodotta in **HTML** o in qualsiasi altro formato.

---

## altre API pubbliche per lo sviluppo

