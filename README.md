# Renderwood.js
Renderwood.js is a small rendering Module for nodeJS, to render HTML in (for example:) Express.js like .blade.php in PHP's Laravel.

**webapp.js**
```
const renderwood = require('renderwood');
const express = require('express');
var app = express();

app.get('/', function (req, res) {
  var test = "Hello World!";
  res.send(renderwood("index.rw.html", {"test": test}));
});

app.listen(3000, function () {
  console.log('Example app listening on port 3000!');
});
```

**index.rw.html**
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

**Basic Usage:**

``renderwood(<html>, <data>);`` in NodeJS.

``@usehere: header.html;;`` = Include HTML from other File here.

``@useCSS: style.css ;;`` = Include CSS-File.

``{{ variable }}`` = Get passed Variable in HTML.

```
@foreach: item of object ;;
<p>{{ item[0] }} </p>
<button>{{ item[1] }} </button>
@endforeach;;
``` 

```
@for: item in array ;;
<p> {{ item }} </p>
@endfor ;;
```



