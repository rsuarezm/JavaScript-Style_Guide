#  Convenciones de nomenclatura
- Evita usar nombres simples. Se descriptivo con los nombres de tus variables.

```javascript
// mal
function sb() {
  // ...
}

// bien
function sidebar() {
  // ...
}
```
 
 
 - Usa camelCase cuando nombres objetos, funciones e instancias.
```javascript
// mal
const OBJEcttsssss = {};
const this_is_my_object = {};
function c() {}

// bien
const thisIsMyObject = {};
function thisIsMyFunction() {}
```

 - Usa PascalCase solo cuando nombres constructores o clases.

```javascript
// mal
function user(options) {
  this.name = options.name;
}

const bad = new user({
  name: 'nope',
});

// bien
class User {
  constructor(options) {
    this.name = options.name;
  }
}

const good = new User({
  name: 'yup',
});
```

- Usa un guión bajo _ adelante de la variable cuando nombres propiedades privadas.

```javascript
// mal
this.__firstName__ = 'Panda';
this.firstName_ = 'Panda';

// bien
this._firstName = 'Panda';
```

- Cuando guardes una referencia a this usa _this.
```javascript
// mal
function() {
  var self = this;
  return function() {
    console.log(self);
  };
}

// mal
function() {
  var that = this;
  return function() {
    console.log(that);
  };
}

// bien
function() {
  var _this = this;
  return function() {
    console.log(_this);
  };
}
```

- Constantes y abreviaciones deberan ser llamadas en UPPERCASE
```javascript
// bad
import SmsContainer from './containers/SmsContainer';

// bad
const HttpRequests = [
  // ...
];

// good
import SMSContainer from './containers/SMSContainer';

// good
const HTTPRequests = [
  // ...
];
```

## jQuery
- Nombre las variables de objetos jQuery con un prefijo $.
```javascript
// mal
var sidebar = $('.sidebar');

// bien
var $sidebar = $('.sidebar'); 
```


# Comentarios
- Usa ```/** ... */``` para comentarios de múltiples líneas. Incluye una descripción, especificación de tipos y valores para todos los parámetros y valores de retorno.

```javascript
// mal
// make() returns a new element
// based on the passed in tag name
//
// @param <String> tag
// @return <Element> element
function make(tag) {

  // ...stuff...

  return element;
}

// bien
/**
 * make() returns a new element
 * based on the passed in tag name
 *
 * @param <String> tag
 * @return <Element> element
 */
function make(tag) {

  // ...stuff...

  return element;
}
```

- Usa ```// ``` para comentarios de una sola línea. Ubica los comentarios de una sola línea encima del sujeto comentado. Deja una línea en blanco antes del comentario. 

```javascript
// mal
var active = true;  // is current tab

// bien
// is current tab
var active = true;

// mal
function getType() {
  console.log('fetching type...');
  // set the default type to 'no type'
  var type = this._type || 'no type';

  return type;
}

// bien
function getType() {
  console.log('fetching type...');

  // set the default type to 'no type'
  var type = this._type || 'no type';

  return type;
}
```


Recursos
- [airbnb style guide](https://www.google.com)
- [snowdream style guide](http://snowdream.github.io/javascript-style-guide/javascript-style-guide/es/)
- [voorhoede jquery style guide](https://github.com/voorhoede/jquery-style-guide)
