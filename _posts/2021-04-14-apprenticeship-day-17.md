---
layout: post
---

## Advent of Code. Day 3
1. Contar cual es el ancho y alto de la input
2. Calcular cuántas veces tienes que multiplicar el ancho para poder llegar hasta el final por abajo:
	número de líneas * número de movimientos hacia la derecha / ancho de tu línea
3. Crear matrix,
```
	for (i)
		line = input[i]
		matrix[i] = line.repeat()
```
