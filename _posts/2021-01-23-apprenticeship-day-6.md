---
layout: post
---

## Blog
Durante el día de hoy hemos eliminado el theme mínima e incorporado su estructura de fichero y directorios en el repositorio. De esa forma, ahora somos capaces de modificar los estilos a nuestro gusto.
<https://jekyllrb.com/docs/themes/#overriding-theme-defaults/>

El CSS que finalmente se utiliza está comprimido de esa forma el peso de la página es menor. <https://jekyllrb.com/docs/assets/#sassscss/>

Utilizar la versión minified es algo muy común, por ejemplo JQuery nos da la versión uncompressed y minified que ocupan mucho menos. <https://code.jquery.com/>

## Línea de comandos
Con los conocimientos anteriores de línea de comando, ahora sabemos cómo renombrar varios ficheros de forma automatizada:
`for i in 1 2 3 4; do git mv images/hackerRank$i.png images/hackerrank$i.png; done`

Si tenemos un alias definido pero queremos ejecutar el comando original, tenemos que anteponer `\` al comando, ejemplo: `\jekyll help`

## Git
- `git log` – Muestra el commits log
- `git blame` file – Muestra los commits y autor que modificó una línea
- `git diff file` – Muestra cambios de un fichero
- `git add file` – Añade un fichero al index
- `git diff --staged` – Muestra cambios del index que se van a comitear
- `git checkout file` – Recupera la versión original de un fichero del repositorio, eliminando nuestros cambios
- `git show commit-sha` – Muestra los cambios de un commit
