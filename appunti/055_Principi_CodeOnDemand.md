# Codice su richiesta (opzionale)

**Codice su richiesta** (opzionale) - REST consente di estendere le funzionalità del client scaricando ed eseguendo il codice sotto forma di applet o script. Ciò semplifica i client riducendo il numero di funzionalità necessarie per essere pre-implementate.

* **Codice su richiesta**. Il più delle volte, un server invierà **rappresentazioni statiche** di risorse sotto forma di XML o JSON. Tuttavia, quando necessario, i server possono inviare codice eseguibile al client.

---


Bene, questo vincolo è facoltativo. Il più delle volte, invierai le rappresentazioni statiche delle risorse sotto forma di XML o JSON. Ma quando è necessario, sei libero di restituire il codice eseguibile per supportare una parte della tua applicazione, ad esempio i clienti possono chiamare la tua API per ottenere un codice di rendering del widget dell'interfaccia utente. È permesso.
Tutti i vincoli di cui sopra ti aiutano a costruire un'API veramente RESTful e dovresti seguirli. Tuttavia, a volte, potresti trovarti a violare uno o due vincoli. Non preoccuparti; stai ancora creando un'API RESTful, ma non "veramente RESTful".

---

Si noti che tutti i vincoli di cui sopra sono strettamente correlati al WWW (il Web). Utilizzo di RESTful API, puoi fare la stessa cosa con i tuoi servizi web come fai con le pagine web.

---

## Code On Demand
Questo vincolo facoltativo è inteso principalmente a consentire alla logica all’interno dei client (come i browser Web) di essere aggiornata indipendentemente dalla logica lato server. Al momento della tesi di Roy Fielding, il web era per lo più solo documenti statici e l’unico “client web” era il browser stesso. Oggi è normale che le app web basate su JavaScript stiano consumando API REST: le single page application rispettano in pieno questo punto.