# Sistema a strati

**Sistema a livelli**: lo stile di sistema a livelli consente a un'architettura di essere composta da livelli gerarchici vincolando il comportamento dei componenti in modo tale che ciascun componente non possa "vedere" oltre il livello immediato con cui interagiscono.


* **Sistema a strati**. REST consente un'architettura composta da più livelli di server.


---


REST consente di utilizzare un'architettura di sistema a più livelli in cui distribuire le API sul server A, archiviare i dati sul server B e autenticare le richieste nel server C, ad esempio. Un client non può normalmente dire se è collegato direttamente al server finale o a un intermediario lungo la strada.

---


Sistema stratificato (LAYERED SYSTEM)
In un sistema a livelli, componenti intermedi come i proxy possono essere collocati tra client e server utilizzando l’interfaccia uniforme del web.
Uno dei vantaggi di un sistema a più livelli è che gli intermediari possono intercettare il traffico client-server per scopi specifici; ad esempio il caching o sicurezza.
Una soluzione basata su REST può essere composta da più livelli architettonici e quest’ultimi sono indipendenti l’uno dall’altro. I livelli possono essere aggiunti, rimossi, modificati o riordinati in risposta a come la soluzione deve evolversi.