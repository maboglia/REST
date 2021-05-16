# Risorsa

Nello stile architettonico **REST**, **i dati e le funzionalità sono considerati risorse** e sono accessibili tramite gli Uniform Resource Identifier (**URI**). Le risorse vengono gestite utilizzando una serie di operazioni semplici e ben definite. 

I client e i server si scambiano **rappresentazioni di risorse** utilizzando un'interfaccia e un protocollo standardizzati, in genere **HTTP**.

L'astrazione chiave delle informazioni in REST è una **risorsa**. 
Qualsiasi **informazione** che può essere **nominata** può essere una **risorsa**: 
* un documento, 
* un'immagine, 
* un servizio, 
* una raccolta di altre risorse, 
* un oggetto non virtuale 
* e così via... 
 
**REST** utilizza un [identificatore](046_URI_URL.md) di **risorsa** per identificare la particolare **risorsa** coinvolta in un'interazione tra componenti.

---

## rappresentazione delle risorse

Lo stato della **risorsa** in qualsiasi data e ora è noto come **rappresentazione delle risorse**. Una rappresentazione è costituita da dati, metadati che descrivono i dati e collegamenti ipertestuali che possono aiutare i client a passare al successivo stato desiderato.

**Le risorse sono disaccoppiate dalla loro rappresentazione** in modo che sia possibile accedere al loro contenuto in una varietà di **formati**, come **HTML**, **XML**, testo normale, **PDF**, **JPEG**, **JSON** e altri. 

I **metadati** sulla risorsa sono disponibili e utilizzati, ad esempio, per controllare la memorizzazione nella cache, rilevare errori di trasmissione, negoziare il formato di rappresentazione appropriato ed eseguire l'autenticazione o il controllo dell'accesso. E, soprattutto, ogni interazione con una risorsa è **[stateless](051_Principi_Stateless.md)**.

---

## formato

Il **formato** dei dati di una rappresentazione è noto come **tipo di supporto**. Il tipo di supporto identifica una specifica che definisce come deve essere elaborata una rappresentazione. 

Un'**API** veramente **RESTful** sembra **ipertesto**. Ogni unità di informazione indirizzabile reca un **indirizzo**, esplicitamente (ad esempio, attributi link e id) o implicitamente (ad esempio, derivato dalla definizione del tipo di supporto e dalla struttura di rappresentazione).

* [JSON](048_JSON.md)
* [XML](048_XML.md)