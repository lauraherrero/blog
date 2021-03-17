---
layout: post
---

## Advent of Code
Hemos trabajado en el primer problema de [**Advent of Code**](https://adventofcode.com/){:target="_blank"}

Algunas ideas para avanzar programando: pensar el problema antes de escribir el código, utilizar lápiz y papel o pizarra para esbozar el funcionamiento, escribir código y ejecutarlo a menudo para comprobar que cada paso funciona, utilizar console.log para hacer debugging y entender lo que ocurre, utilizar ejemplos muy pequeños para avanzar antes de pasar a datos más grandes, etc. A veces la solución llega después de descansar o dejarlo hasta el día siguiente.

## Repaso ecosistema JavaScript
Para crear un proyecto JavaScript creamos un nuevo paquete con npm

`npm init`

Para ejecutar un fichero de JavaScript necesitamos un intérprete que transforme el código escrito con las sintaxis adecuada y lo ejecute:

`node file.js`

## Crear un archivo ejecutable
Como alternativa para ejecutar un archivo se puede crear un archivo ejecutable. Para ello el archivo tiene que tener permisos de ejecución, ls -l nos muestra los permisos:

```
-r-xr-xr-x  1 root  wheel  1296640  1 Jan  2020 bash*
-rwxr-xr-x  1 root  wheel   121968  1 Jan  2020 cat*
-rwxr-xr-x  1 root  wheel   107552  1 Jan  2020 chmod*
```

La primer columna nos muestra los permisos que están agrupados en 3 partes: usuario, grupo y otros. Y los valores que son r (read), w (write) y x (execution).

Hemos creado un archivo y le hemos cambiado los permisos para que sea ejecutable: chmod +x file.js

Ahora podemos ejecutar el archivo ./myfile o si añadimos su ubicación al PATH, estará disponible desde cualquier localización del sistema como myfile,

Un aspecto importante al crear un ejecutable es la shebang, la primera línea de nuestro archivo indica cómo tiene que interpretar el contenido el sistema operativo, por ejemplo en el caso de este ejemplo será node el encargado de interpretar nuestro fichero.
#!/usr/bin/env node

console.log('Hi');

## JavaScript usando require
```
module.exports = input;
const input = require("./api");
```

## JavaScript usando import
Tenemos que modificar el fichero package.json para que el proyecto se configure como ES6 
`"type": "module"`

```
export default input;
import input from "./api.js";
```
