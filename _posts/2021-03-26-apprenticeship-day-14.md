---
layout: post
---
## Advent of Code
Continuamos resolviendo el segundo problema de Advent of Code. Hemos desgranado las distintas partes que necesitamos para resolver el problema y hemos contado el número de ocurrencias de una letra en un string.

How to count string occurrence in string <https://stackoverflow.com/q/4009756/462015/>

Algunos métodos de la API de JavaScript que nos han sido útiles. 
- **split**

```
var theString = "This is a string.";
console.log(theString.split("is").length - 1);
```
- **match**

```
var temp = "This is a string.";
var count = (temp.match(/is/g) || []).length;
console.log(count);
```
- **RegExp**

```
var temp = "This is a string.";

function countOcurrences(str, value) {
  var regExp = new RegExp(value, "gi");
  return (str.match(regExp) || []).length;
}

console.log(countOcurrences(temp, 'is'));
```
