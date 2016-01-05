# Objeto: **vista**
- define una vista del documento
- podemos establecer filtros y selección de campos específicos, para no estar movimiento datos de mas por la red.

## Parámetros
##### id
- identificador de la vista

## Sub objetos

##### [all](view-all.md)
- lee todo la colección

##### [find](view-find.md)
- ejecuta una búsqueda en la colección

##### [pipeline](view-pipeline.md)
- podemos hacer una consulta compleja con múltiples faces y agrupaciones.
- cada fase debe ser un objeto independiente.

##### [sql](view-sql.md)
- ejecuta una consulta en la base de datos SQL.

##### [cypher](view-cypher.md)
- ejecuta una consulta en la base de datos GraphDB

##### [calc](view-calc.md)
- se pueden agregar campos calculados adicionales, que se calculan sobre el resultado de la consulta.

##### [editor](view-editor.md)
- establece los valores por omisión, para cuando se use esta vista.

##### [define](view-define.md)
- podemos definir parámetros de la vista.

