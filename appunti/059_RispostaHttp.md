## HTTP Response – la risposta del server

Campo dell’header|Funzione|Esempio
---|---|---             
Accept-Ranges|Quali unità del server sono accettate per il range indicato (vedi sopra)|Accept-Ranges: bytes
Age|Il tempo in secondi dalla creazione dell’oggetto nella cache|Age:2300             
Allow|I tipi di richieste ammessi per una determinata risorsa|Allow: GET, POST, HEAD
Cache-Control|Se e per quanto tempo l’oggetto può essere mantenuto nella cache|Cache-Control: max-age=4800|
Connection|Il tipo di connessione preferito|Connection: close|
Content-Encoding|Tipo di compressione|Content-Encoding: deflate|
Content-Language|Lingua della risorsa|Content-Language: it-IT|
Content-Length|Dimensione del body in bytes|Content-Length: 135674|
Content-Location|Luogo di archiviazione del file, nel caso in cui provenga da un luogo d’archiviazione diverso da quello richiesto (ad esempio CDN).|Content-Location: /esempio.it|
Content-Security-Policy|La politica di sicurezza del server|Content-Security-Policy: frame-src 'none’; object-src 'none‘|
Content-Type|Il tipo di MIME del file richiesto|Content-Type: text/tml; charset=utf-8|
Date|L’orario della risposta|Date: Mon 2 Mar 2020 1:00:00 GMT|
ETag|Indica una versione specifica del file|ETag: “vt6789oi8uztgfvbn“|
Expires|Da quando il file deve essere considerato superato|Expires: Tue 3 Mar 2020 1:00:00 GMT|
Last-Modified|Orario dell’ultima modifica del file|Last-Modified: Mon 2 Mar 2020 1:00:00 GMT|
Location|Contraddistingue il luogo d’archiviazione nel quale viene inoltrata la richiesta|Location: https://www.esempio.it|
Proxy-Authenticate|Indica se e come il client si deve autenticare con il server proxy|Proxy-Authenticate: Basic|
Retry-After|A partire da quando il client deve avanzare un’altra richiesta, nel caso in cui la risorsa sia temporaneamente indisponibile (data o secondi)|Retry-After: 300|
Server|Identificazione del server.|Server: Apache|
Set-Cookie|Posiziona un cookie nel client|Set-Cookie: UserID=XY; Max-Age=3800; Version=1|
Transfer-Encoding|Il metodo di compressione|Transfer-Encoding: gpzip|
Vary|Informa quale campo dell’header vada considerato come variabile nel caso in cui un file viene richiesto dalla cache|Vary: User-Agent (= il server ha a disposizione diverse versioni del file in base allo User Agent)|
Via|Il proxy tramite il quale viene inviata la risposta|Via: 1.1www.esempio.it

---

## Servizio Web RESTful: il payload della risposta

Il payload della risposta può essere **qualsiasi cosa sia utilizzabile**: dati, HTML, un'immagine, un file audio e così via. Le risposte ai dati sono **in genere codificate** in JSON, ma è possibile utilizzare **XML**, **CSV**, **stringhe** semplici o qualsiasi altro formato. È possibile specificare nella richiesta il formato da ritornare, se disponibile, ad esempio / user / 123? Format = json o / user / 123? Format = xml.

---

## i codici di stato

È inoltre necessario impostare un codice di stato HTTP appropriato nell'intestazione della risposta. Per esempio:

* **200** OK viene spesso utilizzato per richieste riuscite, anche se 
* **201** Creato può essere restituito anche quando viene creato un record. 

Gli errori devono restituire un codice appropriato come 
* **400** Richiesta errata, 
* **404** non trovato, 
* **401** non autorizzato 
* e così via.

---

Altre intestazioni HTTP possono essere impostate tra cui le direttive **Cache-Control** o **Expires** per specificare per quanto tempo una risposta può essere memorizzata nella cache prima che venga considerata obsoleta.

**Tuttavia, non esistono regole rigide.**

URL endpoint, metodi HTTP, dati del corpo e tipi di risposta possono essere implementati a piacere. Ad esempio, POST, PUT e PATCH sono spesso usati in modo intercambiabile, quindi chiunque creerà o aggiornerà un record.

[codici di stato](061_HttpStatusCode_0.md)