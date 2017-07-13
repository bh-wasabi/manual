# Objeto: **mapReduce** (view)
- agrupa y concentra los resultados de una vista

## Parámetros
#### keys
- lista de columnas (separadas por comas) a agrupar.

#### values
- lista de valores (separadas por comas) a concentrar (sumar).

## Ejemplo:
````
{{mapReduce keys="color, category" values="amount"}}
````