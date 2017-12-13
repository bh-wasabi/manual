# Objeto: **update**
- actualiza una sección en el documento.

## Parámetros
#### section
- sección a modificar 

#### sourcePath
- ruta base del documento, por omisión `"/"`
- las expresiones toman en cuenta esta ruta.

#### value
- es posible establecer el valor de toda la sección directamente.

#### condition
- con esta opción es posible condicionar la acción.

#### updateItem (true, false)
- si es un arreglo recorre los elementos y hace el `update` a cada uno de los elementos del arreglo.

## Sub objetos

#### [push](push.md)
- inserta manualmente un objeto al arreglo.

#### [set](set.md)
- asigna valor a uno o varios campos.
