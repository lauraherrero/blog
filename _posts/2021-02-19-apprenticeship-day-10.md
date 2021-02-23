---
layout: post
---
## Cómo hacer export y require de varias functions en JavaScript

```
module.exports = { expect, it }
const {expect, it} = require('./fakest);

Cómo listar los archivos de un directorio con Node.js
const fs = require('fs');

fs.readdir('src/test', (err, files) => {
  files.forEach(file => {
    console.log(file);
  });
});
```

## Testing Framework à la Jest: Fakest
Hemos completado nuestro pequeño framework básico para sustituir a Jest, ¡y funciona! Obviamente Jest tiene mucha mayor funcionalidad, pero esto me ha servido para entender con claridad la magia que hay detrás del framework.

```
function expect(actual) {
  return {
    toBe(expected) {
      if (actual !== expected) {
        throw new Error(`${actual} is different from ${expected}`);
      }
    },
  };
}

function it(_description, callback) {
  return callback();
}
const describe = it;
const test = it;
```

## Jest Mocks
Durante la implementación de Fakest, ha surgido una oportunidad para utilizar un mock y verificar que estamos llamando a la callback.

```
function fakestIt(_description, callback) {
  return callback();
}

test('the callback is invoked', () => {
  const callback = jest.fn();

  fakestIt('description', callback);
  expect(callback.mock.calls.length).toBe(1);
});
```
