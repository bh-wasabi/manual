# Markup: **each**
- hace un bucle para cada elemento del arreglo
- si se quiere hacer una tabla con un diseño diferente esta función puede ser útil.

## Contexto
- el arreglo a recorrer
- automáticamente hace un [with](helper-with.md), del detalle del arreglo.

## Parámetros

##### limit (#)
- con esta opción es posible limitar la cantidad de registros a desplegar.

## Ejemplo:
````
{{#each articulos}}
	{{value precio}} {{value cantidad}} {{value importe}}
{{/each}}
````