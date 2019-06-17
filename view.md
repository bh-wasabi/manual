# Objeto: **vista**
- define una vista del documento
- podemos establecer filtros y selección de campos específicos, para no estar movimiento datos de mas por la red.

## Parámetros
#### id
- identificador de la vista

#### name
- nombre visible de la vista
- principalmente se usa cuando hay opción de cambiar la vista en el `browser`.

#### forceCache (true, false)
- es posible indicar que haga un `cache` de esta vista.
- por seguridad esta opción únicamente funciona cuando el `editor` es `type="select"`.

#### minSearchLength (#)
- cantidad mínima de caracteres para buscar en la vista
- si no esta establecido devuelve sin búsqueda lo primero que encuentre (por omisión).

#### template
- identificador del template a usar.
- por omisión toma el template que esta en `defaultDisplayTemplate`.

#### source
- con esta opción es posible invocar a otra vista de otro documento.
- Nota: si se usa esta opción es indispensable especificar la propiedad de `editor.display`.

#### view
- con esta opción es posible invocar a otra vista de otro documento.
- Nota: si se usa esta opción es indispensable especificar la propiedad de `editor.display`.

#### removeNulls (true, false)
- elimina los valores vacios

#### onlyMapped (true, false)
- unicamente regresa los valores mapeados

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

#### [search](view-search.md)
- ejecuta una consulta en la base de datos ElasticSearch.

#### [slots](view-slots.md)
- ejecuta una consulta para obtener los `slots` disponibles.

#### [unwind](view-unwind.md)
- se pueden explosionar algunos campos tipo arreglo para que lleguen como un solo resultado.

#### [calc](view-calc.md)
- se pueden agregar campos calculados adicionales, que se calculan sobre el resultado de la consulta.

#### [acum](view-acum.md)
- se pueden agregar campos calculados acumulados.

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

#### [display](view-display.md)
- en el caso de ayudas en captura tipo `lookup` o `select` es posible configurar las columnas a desplegar.

#### [syncUser](view-syncUser.md)
- permite hacer una sincronización previa a obtener la vista.
- es necesario hacer un filtro a `_user` con el ID del usuario actual.

#### [map](view-map.md)
- es posible generar re-mapear el resultado de la vista a nuevos campos y valores
- esto se corre al final, después de todo buscar, cálculos, mapReduce, etc.

#### [transform](transform.md)
- en casos muy especificos
- es posible transformar el resultado arreglo (items) a un documento con secciones usando `tranform`.
