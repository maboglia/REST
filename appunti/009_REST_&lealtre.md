# REST e le altre tecnologie analoghe

Vari standard di comunicazione dei dati si sono evoluti nel corso degli anni. Per esempio: CORBA, [SOAP](010_rest_vs_soap.md) o XML-RPC, che di solito stabilivano rigide regole di messaggistica.

---

**REST** è stato definito nel 2000 da **Roy Fielding** ed è notevolmente più semplice. Non è uno standard ma una serie di raccomandazioni e vincoli per i servizi web RESTful.

---

## Questi includono:

* **Client-Server**. SystemA invia una richiesta HTTP a un URL ospitato da SystemB, che restituisce una risposta.

* **Request-response**. Il funzionamento è molto simile a quello di un normale browser. L'applicazione effettua una richiesta per un URL specifico. La richiesta viene instradata a un server Web che restituisce una pagina HTML. Quella pagina può contenere riferimenti a immagini, fogli di stile e JavaScript, che comportano ulteriori **richieste e risposte**.

---

* **Stateless**. REST è senza stato: la richiesta del client deve contenere tutte le informazioni necessarie per rispondere a una richiesta. In altre parole, dovrebbe essere possibile effettuare due o più richieste HTTP in qualsiasi ordine e verranno ricevute le stesse risposte.

* **Cacheable**. Una risposta dovrebbe essere definita come memorizzabile nella cache o meno.

* **A strati**. Il client richiedente non deve sapere se sta comunicando con il server effettivo, un proxy o qualsiasi altro intermediario.

* [SOAP](010_rest_vs_soap.md)
* [HTTP](011_rest_vs_http.md)

