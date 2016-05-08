# Objeto: **create**
- crea una nueva sección en el documento.
- en el caso de `upsert` reemplaza la sección completa.

## Parámetros
##### section
- sección a modificar 

##### sourcePath
- ruta base del documento, por omisión `"/"`
- las expresiones toman en cuenta esta ruta.

##### value
- es posible establecer el valor de toda la sección directamente.

##### condition
- con esta opción es posible condicionar la acción.

## Sub objetos

##### [push](push.md)
- inserta manualmente un objeto al arreglo.

##### [set](set.md)
- asigna valor a uno o varios campos.
