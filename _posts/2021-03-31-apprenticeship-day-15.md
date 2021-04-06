---
layout: post
---
## Advent of Code
Finalizamos la primera parte del segundo día de Advent of Code. Algunos métodos de la API de JavaScript que hemos utilizado:

Teníamos que eliminar de un array el último elemento, hay dos formas de hacer eso
- **slice** devuelve un número array con el subconjunto que especifiquemos.
- **pop** modifica el array original y devuelve el elemento eliminado.

Otras alternativas interesantes a la solución es utilizar un **forEach** en lugar de un **for**. También utilizar **reduce** para que sea una solución funcional eliminando las variables externas para llevar el contador.
- map:
```
 [1, 2, 3, 4, 5].map(x => x * x)
```
- reduce: 
```
[1, 2, 3, 4, 5].reduce(function (acc, current) {
    acc.push(current*current);
    return acc;
 }, [])
```
## Clean code
Un par de temas interesantes que han salido relativos a clean code.

#### Magic number 
<https://en.wikipedia.org/wiki/Magic_number_(programming)/>

Normalmente no se utiliza ningún número mágico, es decir, un número del cual no sabemos a que hace referencia en el código. Se suelen utilizar constantes que capturan la idea de lo que queremos hacer, ej. MIN_AGE = 18 mejor que encontrar simplemente 18.

#### Code smell 
<https://en.wikipedia.org/wiki/Code_smell/>

A veces en el código encontramos cosas que nos indican que las cosas no van bien. Por ejemplo una función con el nombre ReadFileAndRemoveLast, nos indica en realidad que tenemos una función con dos responsabilidades1 y seguramente se deba dividir en dos funciones independientes (más fáciles de entender, testear, etc.)

1: Single Responsibility Principle: <https://en.wikipedia.org/wiki/Single-responsibility_principle/>
