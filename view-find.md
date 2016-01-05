# Objeto: **find**
- define una consulta sobre la colección de documentos

## Parámetros
##### source
- cambiar la fuente de la consulta a que sea de otra colección, por omisión es de la misma colección del tipo de documento.

##### flatten (true, false)
- con esta opción podemos usar `as` en `include` y así poder devolver un arreglo de documentos sin secciones.

##### limit (#)
- podemos limitar la cantidad de documentos a obtener por página.

##### skip (#)
- podemos saltar algunos documentos.

## Sub objetos

##### [include](view-include.md)
- se define el campo a incluir en la vista

##### [exclude](view-exclude.md)
- se define el campo a excluir en la vista

##### [sort](sort.md)
- se puede definir el orden del resultado de la consulta

##### [filter](filter.md)
- se puede definir filtros sobre la consulta

