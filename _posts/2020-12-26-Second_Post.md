---
layout: post
title:  "Second Post"
date: "2020-12-26"
categories: jekyll update
---

## Variables de entorno
Al igual que el archivo ~/.zprofile, existe el archivo ~/.zshrc que se ejecuta cada vez que se abre una nueva consola.

La variables de entorno definen la forma en que funcionan distintos componentes del sistema. Por ejemplo, para customizar el prompt de la terminal, tenemos que modificar la variable de entorno PS1:
`export PS1='%n@%m:%F{magenta}%/%F{white}$ '`

Para ver el contenido de una variable de entorno, utilizamos el prefijo $, ejemplo `echo $PS1`, sin embargo para modificarlo no utilizamos el prefijo.

## Path
La diferencia entre el path relativo y el absoluto, es que el relativo funciona desde el directorio en el que nos encontremos, mientras que el path absoluto funciona desde cualquier localización.

A veces podemos utilizar el path absoluto de distintas formas, esta 3 líneas son equivalentes:
{% highlight ruby %}
ls /Users/lauraherrero/Desktop/Laura/Blog/
ls $HOME/Desktop/Laura/Blog/
ls ~/Desktop/Laura/Blog/
{% endhighlight %}
