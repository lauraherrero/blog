---
layout: post
---

## Modern JavaScript

Un buena guía de referencia para Modern JavaScript Cheatsheet <https://github.com/mbeaudru/modern-js-cheatsheet/>

En cuanto a modern JS hemos usado las arrow function. ES6 ofrece la posibilidad de usar funciones tipo flecha, de ahí su nombre, con una sintaxis más reducida, donde en algunos casos se puede escribir en una sola línea sin que sea obligatorio escribir **return**.

Arrow function <https://github.com/mbeaudru/modern-js-cheatsheet#-arrow-function/>

`function fizzbuzz(num) {} vs. var fizzbuzz = (num) => {}`

## require vs. import

Por otro lado, primeramente utilizamos en la kata Fizzbuzz el método **require** para realizar las importaciones de otros ficheros. Posteriormente decidimos cambiar al método de **import** tras comprobar las ventajas: permite seleccionar solo aquello que necesitas permitiendo ahorrar memoria y su carga es asíncrona, lo que produce mayor rendimiento.
Sin embargo, cuando empezamos a trabajar con Jest nos dimos cuenta de que los test lanzaban un error con esos import que habíamos puesto. Tras analizar qué pasaba, llegamos a la conclusión de que **teníamos que volver nuevamente a require**.

Import / Export <https://github.com/mbeaudru/modern-js-cheatsheet#imports--exports/>

Jest parece que no soporta import
<https://stackoverflow.com/questions/35756479/does-jest-support-es6-import-export/>

## GitHub Gist

GitHub Gist <https://gist.github.com/> permite guardar snippets de código.

## Paradigmas de programación

Los lenguajes de programación se pueden clasificar dependiendo de sus funcionalidades
<https://en.wikipedia.org/wiki/Programming_paradigm/>

Además, dependiendo del estilo de programación, el código puede acercarse más a un paradigma u otro. En este ejemplo la funcionalidad es la misma, pero uno es imperativo y la otra implementación es más funcional.

```
Imperativo
var result = []
[1,2,3].forEach((x) => result.push(x + 1));

Funcional
var result = [1,2,3].map((x) => x + 1);
```

La ventajas de una aproximación funcional es que cada function realiza una única cosa, evitando estados mutables o con side-effects que no esperamos que puede mejorar la calidad del código.

## Currying

Currying es un técnica de programación que permite transformar una función que utiliza múltiples argumentos en una secuencia de funciones que utilizan un único argumento, un ejemplo muy básico podría ser:

```
const isMultipleOf = (base, number) => number % base === 0;
const isMultipleOfThree = (number) => isMultipleOf(3, number);
const isMultipleOfFive  = (number) => isMultipleOf(5, number);
```

## REPL

Read - Eval - Print - Loop <https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop/>
Para testear cosas, es muy útil utilizar el REPL de Node.js, simplemente escribiendo node.

Otra forma es crear un fichero y ejecutar node file.js, de esa forma ejecutamos el contenido del fichero en lugar de copiar y pegar en el REPL.

## Crear Testing Framework à la Jest

Actualmente estamos utilizando elementos muy básicos de Jest, la idea es construir un framework básico de testing para sustituir a Jest.

Hemos empezado tratando de entender la construcción más básica del framework, expect - toBe y qué está haciendo.

```
expect(1).toBe(1);
expect(actual).toBe(expected);
```

Parece que tenemos una función expect que recibe un parámetro (actual) y devuelve un objeto. Ese objeto responde a toBe que es una función que recibe otro parámetro (expected). Por lo que podríamos escribir algo así, aunque todavía nos queda implementar la comparación que realiza el framework

```
function expect(actual) {
  return {
    toBe: function (expected) { return "foo" },
    toEqual: function (expected) { return "bar" }
  }
};
```

Hemos utilizado foo, bar, un estándar en programación <https://en.wikipedia.org/wiki/Foobar/>
