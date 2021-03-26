---
layout: post
---

## Advent of Code
Revisamos el primer problema de Advent of Code y continuamos con el segundo problema de Advent of Code.

## Encoding
Parece que en todos los ejercicios vamos a necesitar leer un input que podemos guardar en un fichero de texto, así que lo primero que tenemos que hacer es leer el fichero.

`fs.readFileSync`

<https://nodejs.org/docs/latest/api/fs.html#fs_fs_readfilesync_path_options/>

La función readFileSync tiene una opción para especificar el encoding, lo cual nos ha permitido investigar sobre distintos formatos de encoding. Al final es tratar de representar un carácter como un número, algunos de los más famosos son el código morse, ASCII o Unicode (UTF-8).

Al final todo se reduce a 1 y 0 en el ordenador. Bits que se agrupan como bytes, kilobytes, megabytes, gigabytes, etc. siguiendo los prefijos del Sistema Internacional.

<https://en.wikipedia.org/wiki/Byte/>

Otro punto importante es que al realizar esa transformación de para codificar datos en unos y ceros, se puede utilizar un algoritmo de compresión con pérdidas donde no es posible recuperar los datos originales, pero tampoco es necesario ya que no son útiles, por ejemplo MP3. Es un compromiso entre información y espacio de almacenamiento de los datos.

Otro aspecto a tener en cuenta al leer o escribir en un archivo, es que algunos lenguajes necesitas especificar si el archivo se abre para lectura (read), escritura (write) o para añadir texto (append).

Recordatorio de línea de comandos relacionado con write o append, la redirección se puede hacer para que escriba o para que añada:
```
echo hola > file.txt
echo hola >> file.txt 
```

## Caracteres especiales
Para leer un fichero de texto y separarlo por líneas, necesitamos utilizar el carácter que designa la nueva línea, en Unix/Mac es `\n`, en Windows es `\r\n`.

<https://en.wikipedia.org/wiki/Newline/>

<https://stackoverflow.com/questions/15433188/r-n-r-and-n-what-is-the-difference-between-them/>
```
> console.log(“Laura\nHerrero”)
Laura
Herrero
```

El carácter `\` es un escape character que designa que el siguiente carácter tiene un significado especial. Por ejemplo, nueva línea `(\n)` o tabulación `(\t)` <https://en.wikipedia.org/wiki/Escape_character/>
 
También se utiliza con las expresiones regulares, cuando utilizamos . quiere decir cualquier carácter, pero si escribimos **\.** Queremos hacer match de un punto, no de cualquier carácter.

Un sitio para hacer pruebas rápidas de regex es **Rubular**, aunque es para Ruby tiene una cheat sheet y podemos ver rápidamente qué funciona en el editor online.
