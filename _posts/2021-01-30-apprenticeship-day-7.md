---
layout: post
---
## Cheat Sheet
La cheatsheet son referencias de información sobre lenguajes o tecnología que vienen bien para recordar cosas, ejemplo de Markdown <https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet/>

## Frontend
El uso de la etiqueta `<br />` está desaconsejada porque utilizamos una etiqueta HTML para modificar el estilo visual. En su lugar debemos utilizar CSS <https://stackoverflow.com/questions/1726073/is-it-sometimes-bad-to-use-br/>

## Visual Studio Code
En Visual Studio Code se pueden sincronizar las settings usando GitHub, de esa forma aunque trabajemos en distintas máquina tenemos la misma configuración.

Las settings se pueden configurar en opciones o desde el archivo settings.js, algunas de las que hemos modificado para añadir una línea al final de cada archivo, eliminar las líneas extra del final, poner una marca visual a los 80 y 120 caracteres, mostrar en rojo los espacios al final de la línea **(trailing spaces)**.

![](/assets/images/vs-settings.png)

## Git
git restore file – Para descartar los cambios de un fichero del working tree
git add -A – Añadir todos los ficheros del working tree al index

Referencia visual sobre el funcionamiento de Git <https://marklodato.github.io/visual-git-guide/index-en.html/>

![](/assets/images/git-cicle.png)

## Npm & ESLint
Hemos instalado una herramienta de análisis estático de código **(ESLint)** para detectar errores en el código y para verificar que cumplimos las reglas de estilo, una de las guías de estilo más populares es la de Airbnb <https://github.com/airbnb/javascript/>

```
npm install eslint --save-dev
npx eslint --init
npx eslint yourfile.js
```

También hemos creado algunos scripts para facilitar el análisis del código, ejecutar los test y ambas cosas juntas:
```
npm run eslint
npm run test
npm run ci
```

## Línea de comandos
En Zsh, el comando history nos devuelve los 15 comando más recientes para ver desde el principio hay que pasar el parámetro con el número history 0. Podemos filtrar la salida con grep: history 0 | grep npm install
