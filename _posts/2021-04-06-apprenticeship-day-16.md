---
layout: post
---
## Línea de comandos
En la línea de comandos o Git podemos movernos al directorio o rama en la que estábamos previamente con el guión (-) en lugar de teclear la ruta.
```
cd -
git -
```

## JavaScript Prototypes
JavaScript es un lenguaje basado en prototipos <https://en.wikipedia.org/wiki/Prototype-based_programming/>

La API de JavaScript nos facilita dos tipos de métodos:
Métodos del objeto, se llaman sobre el objeto. Ej. String.fromCharCode()
```
> String.fromCharCode(97)
'a'
````

Métodos del prototipo, se llaman sobre una instancia del objeto. Ej. String.prototype.charCodeAt()
```
> "a".charCodeAt()
97
```

## Metaprogramación
La metaprogramación es un programa que escribe o modifica otros programas.
<https://en.wikipedia.org/wiki/Metaprogramming/>

Una forma de (meta)programación es un monkey patch, donde extendemos o modificamos una funcionalidad ya existente <https://en.wikipedia.org/wiki/Monkey_patch/>

Por ejemplo podemos hacer que los números respondan a una nueva función fizzBuzz:
```
Number.prototype.fizzBuzz = 'Fizz'
(3).fizzBuzz
```

O podemos modificar funciones definidas en la API de JavaScript
```
String.prototype.split = () => {
  return ['Hola', 'Laura']
}
```

Esta técnica de programación es muy potente pero también muy peligrosa. Casi nunca debemos modificar prototipos de objetos.

## Puertas lógicas
Una puerta lógica nos permite realizar una función booleana basada en una operación lógica. <https://es.wikipedia.org/wiki/Puerta_l%C3%B3gica/>

| AND | `&&` | Esto y lo otro |
| OR | `||` | O esto o lo otro |
| XOR | `^` | O esto o lo otro, pero no las dos |
| NOT | `!` | Contrario de esto |
