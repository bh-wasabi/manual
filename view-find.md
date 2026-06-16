# Objeto: **find**
- define una consulta sobre la colección de documentos

## Parámetros
#### source
- cambiar la fuente de la consulta a que sea de otra colección, por omisión es de la misma colección del tipo de documento.

#### flatten (true, false)
- con esta opción podemos usar `as` en `include` y así poder devolver un arreglo de documentos sin secciones.

#### limit (#)
- podemos limitar la cantidad de documentos a obtener por página.
- si se indica `limit="-1"` devuelve todo sin limite.

#### skip (#)
- podemos saltar algunos documentos.

## Sub objetos

#### [include](view-include.md)
- se define el campo a incluir en la vista

#### [exclude](view-exclude.md)
- se define el campo a excluir en la vista

#### [sort](sort.md)
- se puede definir el orden del resultado de la consulta

#### [filter](filter.md)
- se puede definir filtros sobre la consulta

#### [search](view-find-search.md)
- se puede definir los campos por lo que se desea buscar.
- si no se define busca por todos los campos incluidos en la vista.

#### [hint](view-hint.md)
- se puede especificar un indice en la búsqueda.
- si existen múltiples `hint` toma el primero.
