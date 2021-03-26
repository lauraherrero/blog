---
layout: post
---

## Advent of Code
Seguimos con el primer problema de Advent of Code.

La entrada que tenemos es un array de strings y tenemos que convertir los valores a números para poder operar correctamente con ellos.
```
> 1 + 1
2
> '1' + '1'
'11'
```

La function + existe en JavaScript pero los distintos [**tipos primitivos**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#primitive_values){:target="_blank"} la implementan de forma distinta.

Type conversion, type casting o type coercion <https://en.wikipedia.org/wiki/Type_conversion/>
se utiliza para cambiar un tipo de dato en otro, por ejemplo string to number, en JavaScript se puede hacer con parseInt('100') o con Number('100').

## ESLint
Se pueden configurar distintas reglas de estilo y excepciones.

Si queremos añadir una regla de forma permanente tenemos que modificar el archivo `.eslintrc`:, por ejemplo deshabilitar reglas desde la configuración base.
```
"rules": {
  "no-console": "off"
}
```

También podemos deshabilitar una línea en concreto, en lugar de hacerlo de forma global:

`console.log(1) // eslint-disable-line no-alert`

## Git
Hemos renombrado el repositorio que teníamos de FizzBuzz a puzzles y añadido el código de Advent of Code.

Al renombrar el repositorio en GitHub la referencia remota (URL) cambia, podemos ver cuál es el repositorio remoto con 
`git remote -v`

## Sistema binario
El sistema binario es un sistema donde los números son representados por dos cifras (0, 1) <https://es.wikipedia.org/wiki/Sistema_binario/>

| Decimal | Binario |
| -- | -- |
| 0 | 0 | 
| 1 | 1 | 
| 2 | 10 | 
| 3 | 11 | 
| 4 | 100 | 
| 5 | 101 | 
| 6 | 110 | 
| 7 | 111 | 
| 8 | 1000 | 


Un ejemplo de uso es el sistema de permisos de Linux, en los que con chmod se pueden cambiar los permisos. Por ejemplo al estar agrupados los permisos en 3 grupos y cada valor puede estar encendido o apagado.

Por ejemplo, por cada grupo tenemos que establecer los permisos de cada elemento en binario:

| read | write | execution |  |
| -- | -- | -- | -- |
| r | - | x |  |
| 1 | 0 | 1 |  |
| 4 | 0 | 1 | = 5 (decimal) |


```
$ ls -l package.json
-rw-rw-r-x  1 laura  group   107552  1 Jan  2020 package.json
```

| read | write | execution | read | write | execution | read | write | execution |
| -- | -- | -- | -- | -- | -- | -- | -- | -- |
| 4 | 2 | 0 | 4 | 2 | 0 | 4 | 0 | 1 |

```
$ chmod 644
$ ls -l package.json
-rw-r--r--  1 laura  group   107552  1 Jan  2020 package.json
$ chmod 664
$ ls -l package.json
-rw-rw-r--  1 laura  group   107552  1 Jan  2020 package.json
````

Otra uso muy común de otros sistema numéricos es el hexadecimal, por ejemplo se utiliza para definir colores: #FA21B2.
