---
layout: post
---

## Seguridad informática (Gestores de contraseñas)
Debemos utilizar un gestor de contraseñas, de esa forma incrementamos la seguridad al utilizar una contraseña diferente para cada plataforma que utilicemos. 2FA: Two Factor Authentication es un mecanismo para utilizar no solo una contraseña sino otro método adicional de seguridad, ejemplo un código de verificación por SMS o aplicación de 2FA (Authy o Google Authenticator).

**Algunos ejemplos de gestores de contraseñas:**
- `Google` – <https://passwords.google.com/>
- `LastPass` - <https://www.lastpass.com/>
- `¿Has sido hackeadX?`- <https://haveibeenpwned.com/>

Seguridad informática (Bases de datos con contraseñas)
Las contraseñas se tienen que guardar en una base de datos de forma cifrada. Hay distintos algoritmos de cifrado, MD5 (inseguro), SHA256, etc. que aplican una función hash para transformar texto plano en texto cifrado, esa función hash funciona en un único sentido y de un texto cifrado no se puede conocer el texto plano. Ejemplo:
$ md5 -s laura
MD5 ("laura") = 680e89809965ec41e64dc7e447f175ab

Una <a href="https://en.wikipedia.org/wiki/Rainbow_table">rainbow table</a> es una base de datos que tiene precomputadas la salida de funciones hash para muchos valores diferentes. De esta forma, si tenemos texto cifrado, podríamos ser capaces de conocer el texto plano original mirando la tabla con los valores precomputados.

Adicionalmente se utiliza un <a href="https://en.wikipedia.org/wiki/Salt_(cryptography)">salt</a> (datos aleatorios) para cifrar el texto.

## Línea de comandos
El pipe operator (|) permite concatenar la salida de un comando con la entrada del siguiente.
cat laura.txt | head -n 2 – Imprime la dos primeras líneas del fichero.

Una buena página web para poder practicar ejercicios con bash es: <https://www.hackerrank.com/domains/shell/>

<br>Instrucciones del problema.

![Alt text](/assets/images/hackerrank2.png)


<br> Consola para poder escribir la solución.

![Alt text](/assets/images/hackerrank3.png)


<br> Comprobación mediante test del código que hemos escrito.

![Alt text](/assets/images/hackerrank4.png)

## Blog
Un blog de referencia, Julia Evans <https://jvns.ca/>
