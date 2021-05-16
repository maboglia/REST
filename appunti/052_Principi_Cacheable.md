# cacheable

**Memorizzabile nella cache**: i vincoli della cache richiedono che i dati all'interno di una risposta a una richiesta siano etichettati in modo implicito o esplicito come memorizzabili nella cache o non memorizzabili nella cache. Se una risposta è memorizzabile nella cache, una cache client ha il diritto di riutilizzare i dati di risposta per richieste successive ed equivalenti.

* Memorizzazione nella **cache delle risorse**. Tutte le risorse dovrebbero consentire la memorizzazione nella cache se non indicato esplicitamente che la memorizzazione nella cache non è possibile.


Nel mondo di oggi, la memorizzazione nella cache di dati e risposte è della massima importanza ovunque siano applicabili / possibili. La pagina Web che stai leggendo qui è anche una versione cache della pagina HTML. La memorizzazione nella cache comporta un miglioramento delle prestazioni per il lato client e un migliore ambito di scalabilità per un server perché il carico è stato ridotto.

In REST, la memorizzazione nella cache deve essere applicata alle risorse quando applicabile, e quindi queste risorse DEVONO dichiararsi memorizzabili nella cache. La memorizzazione nella cache può essere implementata sul server o sul lato client.
La memorizzazione nella cache ben gestita elimina parzialmente o completamente alcune interazioni client-server, migliorando ulteriormente la scalabilità e le prestazioni.

---

La richiesta di rete più efficiente è quella che non utilizza la rete.
in un Architettura REST i messaggi di risposta dal servizio ai suoi consumatori sono esplicitamente etichettati come cacheabili o non. In questo modo, il servizio, il consumatore o uno dei componenti middleware intermediari possono memorizzare nella cache la risposta per il riutilizzo nelle richieste successive.
Il vincolo Cache si basa su Client-Server e Stateless con il requisito che le risposte siano etichettate implicitamente o esplicitamente come memorizzabili nella cache o non memorizzabili nella cache. Le richieste vengono passate attraverso un componente cache, che può riutilizzare le risposte precedenti per eliminare parzialmente o completamente alcune interazioni sulla rete