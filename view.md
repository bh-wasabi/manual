# Objeto: **vista**
- define una vista del documento
- podemos establecer filtros y selección de campos específicos, para no estar movimiento datos de mas por la red.

## Parámetros
#### id
- identificador de la vista

#### name
- nombre visible de la vista
- principalmente se usa cuando hay opción de cambiar la vista en el `browser`.

#### minSearchLength (#)
- cantidad mínima de caracteres para buscar en la vista
- si no esta establecido devuelve sin búsqueda lo primero que encuentre (por omisión).

## Sub objetos

#### [all](view-all.md)
- lee todo la colección

#### [find](view-find.md)
- ejecuta una búsqueda en la colección

#### [request](view-request.md)
- ejecuta una llamada a un web service externo y de ahí obtiene los datos.

#### [pipeline](view-pipeline.md)
- podemos hacer una consulta compleja con múltiples faces y agrupaciones.
- cada fase debe ser un objeto independiente.

#### [sql](view-sql.md)
- ejecuta una consulta en la base de datos SQL.

#### [s3](view-s3.md)
- buscar un archivo especifico en s3.

#### [redis](view-redis.md)
- hace una consulta en redis.

#### [cypher](view-cypher.md)
- ejecuta una consulta en la base de datos GraphDB

#### [calc](view-calc.md)
- se pueden agregar campos calculados adicionales, que se calculan sobre el resultado de la consulta.

#### [pivot](view-pivot.md)
- es posible pivotear los resultados de la vista para generar un reporte matricial.

#### [mapReduce](view-mapReduce.md)
- en algunos casos se puede necesitar agrupar y concentrar los resultados de la vista.
- es una alternativa al pipeline.

#### [serialize](view-serialize.md)
- es posible serializar los resultados.
- esto es muy útil en el caso de gráficas que se necesitan así los datos.

#### [editor](view-editor.md)
- establece los valores por omisión, para cuando se use esta vista.

#### [define](view-define.md)
- podemos definir parámetros de la vista.

#### [join](view-join.md)
- es posible unir los resultados con otros documentos y crear un resultado de múltiples fuentes.
- esto es sobre el mismo documento, agrega un campo o sección nuevo en base al ´join´.

#### [union](view-union.md)
- es posible unir los resultados con otros documentos y crear un resultado de múltiples fuentes.
- esto une los resultados.