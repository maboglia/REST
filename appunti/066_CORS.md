# CORS

**CORS** (**Cross-Origin Resource Sharing**) è un sistema, costituito dalla trasmissione di intestazioni HTTP, che determina se i browser bloccano il codice JavaScript frontend dall'accesso alle risposte per le richieste cross-origin.

La politica di sicurezza della stessa origine impedisce l'accesso alle risorse tra le origini. Ma **CORS** offre ai server Web la possibilità di dichiarare di voler consentire l'accesso cross-origin alle proprie risorse.

[riferimenti]
* Cross-Origin Resource Sharing (**CORS**) su MDN
* Condivisione di risorse cross-origin su Wikipedia


## Intestazioni CORS

* **Access-Control-Allow-Origin**
    Indica se la risposta può essere condivisa.
* **Access-Control-Allow-Credentials**
    Indica se la risposta alla richiesta può essere esposta o meno quando il flag delle credenziali è true.
* **Access-Control-Allow-Headers**
    Utilizzato in risposta a una richiesta di verifica preliminare per indicare quali intestazioni HTTP possono essere utilizzate quando si effettua la richiesta effettiva.
* **Access-Control-Allow-Methods**
    Specifica il metodo oi metodi consentiti quando si accede alla risorsa in risposta a una richiesta di verifica preliminare.
* **Access-Control-Expose-Headers**
    Indica quali intestazioni possono essere esposte come parte della risposta elencandone i nomi.
* **Access-Control-Max-Age**
    Indica per quanto tempo i risultati di una richiesta di verifica preliminare possono essere memorizzati nella cache.
* **Access-Control-Request-Headers**
    Utilizzato quando si invia una richiesta di verifica preliminare per far sapere al server quali intestazioni HTTP verranno utilizzate quando viene effettuata la richiesta effettiva.
* **Access-Control-Request-Method**
    Utilizzato quando si invia una richiesta di verifica preliminare per far sapere al server quale metodo HTTP verrà utilizzato quando viene effettuata la richiesta effettiva.
* **Origin**
    Indica da dove ha origine un recupero.


---



## Client-side REST Requests and CORS

Ad esempio considera la seguente risorsa HTML `http://localhost:8888/`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>REST test</title>
</head>
<body>
<script>
fetch('http://localhost:8888/hello/')
  .then((response) => {
    return response.json();
  })
  .then((json) => {
    console.log(json);
  });
</script>
</body>
</html>
```

La chiamata di recupero fa la stessa richiesta API e la console del browser mostra Oggetto {messaggio: "Ciao mondo!" } come ti aspetteresti.

Tuttavia, supponiamo che il tuo servizio Web RESTful sia stato messo online sul Web nel dominio `http://mydomain.com/hello/`. L'URL JavaScript `fetch()` della pagina viene modificato di conseguenza, ma l'apertura di `http://localhost:8888/` nel browser ora restituisce l'errore della console **Cross-Origin Request Blocked**.

Per motivi di sicurezza, i browser consentono solo chiamate **XMLHttpRequest** e **Fetch API** lato client **ALLO STESSO DOMINIO** in cui è ospitata la pagina.

Fortunatamente, la **condivisione delle risorse tra le origini** (CORS) ci consente di aggirare questa limitazione della sicurezza. 

L'impostazione di un'intestazione di risposta HTTP **Access-Control-Allow-Origin** indica ai browser di consentire la richiesta. Può essere impostato su un dominio specifico o * per tutti i domini (fatto dall'API Joke sopra).

Il codice API del servizio Web può quindi essere modificato per consentire l'accesso da qualsiasi script lato client in esecuzione su qualsiasi dominio:

```javascript
// /hello/ GET request
app.get('/hello/:name?', (req, res) =>
  res
    .append('Access-Control-Allow-Origin', '*')
    .json(
      { message: `Hello ${req.params.name || 'world'}!` }
    )
);
```

In alternativa, una funzione middleware Express.js potrebbe aggiungere l'intestazione a ogni richiesta di endpoint:


```javascript
// enable CORS
app.use((req, res, next) => {
  res.append('Access-Control-Allow-Origin', '*');
  next();
});

// /hello/ GET request
// ...
```
