# Codice Rest

Esempio di "Hello World" REST

Il codice seguente crea un servizio Web RESTful utilizzando il framework Node.js Express. Un singolo / ciao / endpoint risponde alle richieste GET.

Assicurati di aver installato Node.js, quindi crea una nuova cartella chiamata restapi. Crea un nuovo file package.json all'interno di quella cartella con il seguente contenuto:
```javascript
{
  "name": "restapi",
  "version": "1.0.0",
  "description": "REST test",
  "scripts": {
    "start": "node ./index.js"
  },
  "dependencies": {
    "express": "4.17.1"
  }
}
```

Run npm install from the command line to fetch the dependencies, then create an index.js file with the following code:

```javascript

// simple Express.js RESTful API
'use strict';

// initialize
const
  port = 8888,
  express = require('express'),
  app = express();

// /hello/ GET request
app.get('/hello/:name?', (req, res) =>
  res.json(
    { message: `Hello ${req.params.name || 'world'}!` }
  )
);

// start server
app.listen(port, () =>
  console.log(`Server started on port ${port}`);
);
```

Launch the application from the command line using npm start and open http://localhost:8888/hello/ in a browser. The following JSON is displayed in response to the GET request:

```javascript
{
  "message": "Hello world!"
}
```

The API also allows a custom name, so http://localhost:8888/hello/everyone/ returns:

```javascript
{
  "message": "Hello everyone!"
}
```

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

## CORS


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

### Alternatively (Express.js)

```javascript
// enable CORS
app.use((req, res, next) => {
  res.append('Access-Control-Allow-Origin', '*');
  next();
});

// /hello/ GET request
// ...
```
