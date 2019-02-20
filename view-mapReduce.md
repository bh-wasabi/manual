# Objeto: **mapReduce** (view)
- agrupa y concentra los resultados de una vista

## Parámetros
#### keys
- lista de columnas (separadas por comas) a agrupar.

#### values
- lista de valores (separadas por comas) a concentrar (sumar).

#### compact (true, false)
- comprime los resultados finales

## Ejemplo:
````
{{mapReduce keys="color, category" values="amount"}}
````