---
layout: post
---

## Referencia de línea de comandos
Repasando el día anterior,  The Linux Commands Handbook 

<https://www.freecodecamp.org/news/the-linux-commands-handbook/>

## Línea de comandos
Repaso de comandos `ls, touch, cat, mkdir, mv, cd, ..`
¿Cómo se colorea la salida del comando ls? `man ls`
ls -G –> ls con color

**Variables de entorno:**
La variable CLICOLOR=1 controla la salida coloreada de ls, si queremos que se lea cada vez que abrimos la terminal lo añadimos a ~/.zshrc
Tenemos que volver a leer el contenido de source ~/.zshrc para que los cambios sean efectivos en la terminal en la que estamos.

Directorios de Linux <https://es.wikipedia.org/wiki/Filesystem_Hierarchy_Standard/>

El comando tree, lo hemos instalado en Mac `brew install tree` sirve para visualizar el sistema de archivos como un árbol.
`tree -L 2` –> Lista los ficheros del directorio, limitando a dos niveles.

## Vim
Vi o Vim (Vi IMproved) es un editor que está presente en muchos sistemas operativos. Hay principalmente dos modos: 
  - Inserción
  - Comando

Para escribir hay que entrar en modo inserción con, entre otros: i, A
Para volver al modo comando: ESC
Para guardar y salir: :wq

Una de las preguntas más populares de Stack Overflow es cómo salir de Vim
<https://stackoverflow.blog/2017/05/23/stack-overflow-helping-one-million-developers-exit-vim/>
