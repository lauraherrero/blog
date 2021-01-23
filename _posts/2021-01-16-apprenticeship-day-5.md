---
layout: post
---

## Línea de comandos
Unix philosophy 

<https://es.wikipedia.org/wiki/Filosof%C3%ADa_de_Unix/>

- `ls | grep D` – Listar los ficheros que empiezan por D
- `mkdir -p src/test` – La opción -p, crea el directorio incluyendo los directorios intermedios
- `git init` – Iniciar repositorio Git

## Git
Se puede crear un fichero global .gitignore en el que ignorar ficheros independientemente del directorio en el que estemos. Git lee automáticamente este fichero global  __~/.gitignore__

También existe un fichero global con la configuración de Git: __~/.gitconfig__

Semantic Versioning
<https://semver.org/>

Given a version number MAJOR.MINOR.PATCH, increment the:
- MAJOR version when you make incompatible API changes,
- MINOR version when you add functionality in a backwards compatible manner, and
- PATCH version when you make backwards compatible bug fixes.

En las releases, se comunican los cambios de tu software <https://github.com/facebook/jest/releases/>

**CHANGELOG.md**, se suele utilizar también para comunicar los cambios <https://github.com/facebook/jest/blob/master/CHANGELOG.md/>

## Kata FizzBuzz
Introduction Jest <https://github.com/osoco/introducing-jest/>
Jest <https://jestjs.io/>

- `npm init` – Iniciar package.json
- `npm install` --save-dev jest – Instalar jest como dev dependency
- `npx jest` --watchAll – Correr los test automáticamente

Hemos realizado **Test-Driven-Development (TDD)** donde vamos escribiendo la especificación (test), hacemos que pase y después refactorizamos el código en pequeños pasos.

<https://github.com/lauraherrero/FizzBuzz/>


## Algunas ideas interesantes:
Los test también se refactorizan, por ejemplo hemos agrupado test bajo un mismo bloque it cuando hemos pasado de test individuales (3 -> Fizz, 6 -> Fizz) a la idea de múltiplo.
Hemos extraído funciones para que la lectura del código fuera más fluida: __isMultipleofThree(num)__ y __isMultipleofFive(num)__.
Hemos extraído un colaborador externo Number.js que tenía la responsabilidad de las funciones numéricas.


Development Documentation
Programming languages documentation <https://devdocs.io/>

## Visual Studio Code
- `⌘ + j` – Abre y cierra la terminal
- `⌥ + ↑` – Mover la línea hacia arriba
- `⌘ + ⇧ + k` – Eliminar la línea

## Testing
Piramide de testing <https://www.browserstack.com/guide/testing-pyramid-for-test-automation/>


