# REST e http

Un sistema che segue i principi dettati da **REST** viene comunemente definito **REST**ful.

![REST](https://raw.githubusercontent.com/maboglia/Fondamenti/master/img/REST.png)

* Solitamente REST viene associato al **protocollo HTTP**: preferibile poiché estremamente diffuso e già utilizzato per trasferire “ipertesti” collocati a determinati indirizzi,

---

* inoltre ogni sua richiesta può essere completamente indipendente dalle altre e può specificare una determinata operazione (o metodo) da eseguire, rispettando così i principi REST.


## REST != HTTP

Capita spesso di considerare REST come sinonimo di HTTP:
**REST e HTTP non sono la stessa cosa!**

---

La confusione nasce dal fatto che REST intende anche rendere il web più snello e standardizzato, sostiene l'utilizzo più rigoroso dei principi REST anche per internet.

Roy Fielding, nella sua tesi di dottorato, **non ha mai menzionato alcuna direttiva di implementazione**, comprese le preferenze di protocollo e HTTP. 

---

Se si seguono i 6 principi guida di REST, si può definire l'interfaccia come **RESTful**.

In parole più semplici, nello stile architettonico REST, **i dati e le funzionalità sono considerati risorse** e sono accessibili tramite gli [Uniform Resource Identifier](046_URI_URL.md) (**URI**). Le risorse vengono gestite utilizzando una serie di operazioni semplici e ben definite. I client e i server si scambiano rappresentazioni di risorse utilizzando un'interfaccia e un protocollo standardizzati, in genere HTTP.

---

**Le risorse sono disaccoppiate dalla loro rappresentazione** in modo che sia possibile accedere al loro contenuto in una varietà di formati, come HTML, XML, testo normale, PDF, JPEG, JSON e altri. I metadati sulla risorsa sono disponibili e utilizzati, ad esempio, per controllare la memorizzazione nella cache, rilevare errori di trasmissione, negoziare il formato di rappresentazione appropriato ed eseguire l'autenticazione o il controllo dell'accesso. E, soprattutto, ogni interazione con una risorsa è stateless.

Tutti questi principi aiutano le applicazioni RESTful ad essere semplici, leggere e veloci.

---

Riferimenti:

http://roy.gbiv.com/untangled/2008/rest-apis-must-be-hypertext-driven
http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm