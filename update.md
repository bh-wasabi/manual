# Objeto: **update**
- actualiza una sección del documento

## Parámetros
##### section
- sección a modificar 

##### sourcePath
- ruta base del documento, por omisión `"/"`
- las expresiones toman en cuenta esta ruta.

##### type
- `object` 
- `array`

##### value
- es posible establecer el valor de toda la sección directamente.

##### sortBy
- podemos ordenar el resultado, lista de campos separados por comas.

##### groupBy
- agrupa el resultado por la lista de campos (separados por comas) indicados.
- por ejemplo: `groupBy="alias, descripción, unidad, precio"`

##### sum
- cuando se usan los agrupadores podemos indicar que campos hay que concentrar.
- por ejemplo: `sum="cantidad,importe"`

##### where
- podemos tener filtros adicionales, separados por comas y en forma de llave=valor.
- por ejemplo: `where="unidad=KG"`

##### indexBy
- podemos indexar el resultado por alguno de los campos, esto genera nuevos sub objetos con la llave por el campo indicado.

##### render
- podemos usar un [template](template.md) especial.

## Sub objetos

##### [set](set.md)
- actualiza el valor de uno o varios campos.
