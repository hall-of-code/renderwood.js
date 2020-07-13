# Renderwood.js
Renderwood.js is a small rendering Module for nodeJS, to render HTML in (for example:) Express.js linke .blade.php in Laravel.

**webapp.js**
```
const renderwood = require('renderwood');
const express = require('express');
var app = express();

app.get('/', function (req, res) {
  var test = "Hello World!";
  res.send(renderwood("index.html", {"test": test}));
});

app.listen(3000, function () {
  console.log('Example app listening on port 3000!');
});
```

**index.html**
```
<!DOCTYPE: html>
<html>
<head>
  <title>Lalalala</title>
</head>
<body>
  <p>{{ test }}</p>
</body>
</html>
```


