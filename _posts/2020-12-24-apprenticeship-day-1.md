---
layout: post
title:  "First Post"
date: "2020-12-24"
categories: jekyll update
---
Merry Xmas!

El principal objetivo del proyecto es la creación de un blog personal sobre consejos y utilidades de programación.

Cada semana doy clase con mi hermano para mejorar y aprender cosas nuevas que pueda aplicar en mi trabajo y a nivel profesional. Cada nuevo post tendrá la información de la clase anterior.


## Homebrew
brew es un gestor de paquetes para instalar utilidades de linea de comandos y brew cask sirve para instalar aplicaciones de escritorio. Es igual que apt para Linux.

```
brew help
brew search ruby
brew install node
brew cask install visual-studio-code
brew list
```

## ssh
ssh sirve para comunicarse de forma segura entre máquinas. Utiliza una clave pública que se corresponde con una clave privada.

En el caso de la comunicación con GitHub necesitamos crear nuestro par de claves pública–privada <https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent>

La clave pública se puede compartir pero la clave privada NO. Están guardadas en el directorio ~/.ssh

## Ruby
Los archivos Gemfile + Gemfile.lock son a Ruby lo mismo que package.json y yarn.lock a JavaScript.
bundle install – Instala las dependencias del archivo Gemfile. El archivo Gemfile.lock no se edita a mano.

## Otras utilidades de linea de comando
- `cat file` – Muestra el contenido del archivo
- `touch file` – Crear un archivo vacío
- `echo Hi world` – Imprime el texto
- `echo Hi >> test.txt` – Redirige la salida a un fichero y lo añade al final
- `echo Hi > test.txt` – Redirige la salida a un fichero  y lo sobreescribe
- `git clone git@...` – Clona el repositorio
- `man command` – Muestra el manual de un comando
- `mv name new-name` – Mueve el archivo con un nuevo nombre o lo cambia de directorio
- `mv myblog/* .` – Mueve todos los archivos que están dentro de myblog al directorio actual (.)
- `rmdir directory` – Elimina un directorio vacío
- `rm -r directory` – Elimina un directorio aunque no esté vacío

## Zsh vs Bash
Zsh es la shell (el intérprete de comandos) que corre dentro de la terminal (iTerm).
Hay algunos archivos que se ejecutan automáticamente cuando arrancas la terminal. En zsh el ~/.zprofile, en Bash ~/.bash_profie.

