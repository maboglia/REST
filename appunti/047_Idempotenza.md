# Idempotenza

Un metodo HTTP è idempotente se una richiesta identica può essere effettuata una o più volte di seguito con lo stesso effetto lasciando il server nello stesso stato. In altre parole, un metodo idempotente non dovrebbe avere effetti collaterali (ad eccezione del mantenimento delle statistiche). Implementati correttamente, i metodi GET, HEAD, PUT e DELETE sono idempotenti, ma non il metodo POST. Tutti i metodi sicuri sono anche idempotenti.

---

Per essere idempotenti, viene considerato solo lo stato back-end effettivo del server, il codice di stato restituito da ciascuna richiesta può essere diverso: la prima chiamata di DELETE probabilmente restituirà un 200, mentre quelle successive probabilmente restituiranno un 404. Un'altra implicazione se DELETE è idempotente, gli sviluppatori non dovrebbero implementare API RESTful con una funzionalità di eliminazione dell'ultima voce utilizzando il metodo DELETE.

---

Si noti che l'idempotenza di un metodo non è garantita dal server e alcune applicazioni potrebbero infrangere erroneamente il vincolo di idempotenza.

GET / pageX HTTP / 1.1 è idempotente. Chiamato più volte di seguito, il client ottiene gli stessi risultati:

GET / pageX HTTP / 1.1
GET / pageX HTTP / 1.1
GET / pageX HTTP / 1.1
GET / pageX HTTP / 1.1

---

POST / add_row HTTP / 1.1 non è idempotente; se viene chiamato più volte, aggiunge più righe:

POST / add_row HTTP / 1.1
POST / add_row HTTP / 1.1 -> Aggiunge una seconda riga
POST / add_row HTTP / 1.1 -> Aggiunge una terza riga

---

DELETE / idX / delete HTTP / 1.1 è idempotente, anche se il codice di stato restituito può cambiare tra le richieste:

DELETE / idX / delete HTTP / 1.1 -> Restituisce 200 se idX esiste
DELETE / idX / delete HTTP / 1.1 -> Restituisce 404 poiché è stato appena eliminato
DELETE / idX / delete HTTP / 1.1 -> Restituisce 404