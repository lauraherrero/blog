---
layout: post
---

## Advent of Code
Hemos arreglado algunos test.

Un concepto interesante que ha salido durante la conversación es la [**inyección de dependencias**](https://es.wikipedia.org/wiki/Inyecci%C3%B3n_de_dependencias){:target="_blank"}. En este caso, simplemente hemos aislado nuestras funciones de los valores de entrada del sistema de ficheros, de esa forma podemos escribir tests donde la entrada cubre los distintos escenarios que queremos testear.

## Bases de datos
Una base de datos muy simple es un CSV (comma-separated values), es decir, un fichero de texto donde estructuramos la información de una determinada forma. Nos basta con ciertas herramientas Unix para hacer queries.

Por ejemplo, podemos “consultar” todos los valores de la primera columna

`cat db.txt | cut -d',' -f 1`

Las [**bases de datos relacionales**](https://es.wikipedia.org/wiki/Base_de_datos_relacional){:target="_blank"} organizan la información en tablas.

| Usuario |
| -- |
| Arturo |
| Laura |


| Ciudad |
| -- |
| Londres |
| Madrid |
