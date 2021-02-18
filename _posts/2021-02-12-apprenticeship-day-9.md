---
layout: post
---

## GitHub Actions
Ya tenemos el repositorio con integratición continua. De esta forma todo el código cumple con los estándares definidos en el linter y también se ejecutan todos los tests.

Para ellos hemos utilizado GitHub Actions CI 

<https://docs.github.com/en/actions/>

Nos hemos basado en el template de GitHub Actions for Node.js 

<https://docs.github.com/en/actions/guides/building-and-testing-nodejs/>

```
name: CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [15.x]

    steps:
      - uses: actions/checkout@v2

      - name: Use Node.js ${{ matrix.node-version }}
        uses: actions/setup-node@v1
        with:
          node-version: ${{ matrix.node-version }}

      - name: Install dependencies
        run: npm install

      - name: Run linter and test
        run: npm run ci
```

## Git
Cuando integramos una rama de código en otra se pueden utilizar distintas estrategias, principalmente rebase o merge 

<https://www.atlassian.com/git/tutorials/merging-vs-rebasing/>

Merge crea un commit de integración pero es más sencillo a la hora de resolver conflictos y es una operación no destructiva. Rebase permite incorporar cambios de una manera más limpia, pero puede ser una opción má complicada y destructiva.

Algunos comandos para visualizar los logs

`git log --graph --oneline`
`git log --graph --pretty=format:'%C(yellow)%h%C(reset) -%C(auto)%d %s %C(green)(%cr) %C(bold blue)<%an>'`

Mostrar el último commit o un commit determinado

`git show`
`git show 2e6f317`

Eliminar el último commit (operación destructiva, ¡cuidado!)

`git reset --hard HEAD^`
`git reset --hard HEAD~1`

Modificar el mensaje del último commit

`git commit --amend`

Cuando hemos modificado la historia (ya sea eliminando commits o modificándolos) y queremos hacer push de los cambios, tenemos que pasar la opción --force (operación destructiva, ¡cuidado!)
git push -f

Añadir cambios al stash incluyendo untracked files (archivos de los que Git no tiene conocimiento)

`git stash -u`
`git stash pop`

Podemos eliminar nuestros cambios locales si volvemos a hacer checkout de un fichero o directorio

`git checkout src`

Otra utilizadad que nos permite modificar la historia es rebase interactive, pasádole un commit podemos modificar la historia con distintas opciones

`git rebase -i 04099a6`

## Mocks
Un mock es un objeto que simula el comportamiento del objeto real de forma controlada. Puede ser muy útil para simular llamadas costosas, lentas o no deterministicas. Algunos ejemplos de uso pueden ser llamadas a bases de datos, llamadas a una API, etc. Al mockear objetos podemos aislar mejor su comportamiento y mejorar nuestros test unitarios.

Jest como framework de testing nos permite crear mocks. 
<https://jestjs.io/docs/en/mock-functions/>

## Testing Framework à la Jest: Fakest
```
function expect(actual) {
  return {
    toBe: function (expect) {
      try {
        if (actual != expect) {
          throw 'Error'
        }
      } catch (error) {
        console.log('My Error');
      }
    }
  }
};

// expect(actual).toBe(expect);
expect(1).toBe(1); // Pass
expect(1).toBe(2); // Fail
expect('hi').toBe('hi'); // Pass
expect('hi').toBe('bye'); // Fail
```

## Línea de comandos
Con los conocimientos de línea de comandos hemos mostrado la historia de una mejor forma, para ellos hemos mostrado la historia desde el comienzo, mostrando solo los comandos y por último eliminado las entradas duplicadas:

`history 0 | cut -d' ' -f 4- | uniq`
