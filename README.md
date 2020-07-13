# Renderwood.js
Renderwood.js is a small rendering Module for nodeJS, to render HTML in (for example:) Express.js linke .blade.php in Laravel.

```
const renderwood = require('renderwood');
var passing-variable = "Hello World";
return renderwood("index.html", {"passing-variable": passing-variable});
