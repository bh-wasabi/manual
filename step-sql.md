# Objeto: **sql** (step)
- obtiene un arreglo como resultado de una consulta a la base de datos SQL.
- los parametros se usan con el prefijo `$`, es posible usar `$tenant`, `$tenantHash` y `$user` sin tener que definirlos.
- el resultado de la consulta queda en el contexto para ser usado por un comando [each](step-each.md).

## Parámetros
#### query
- puede ser a multiples líneas para tener mayor claridad, hay que incluir los parámetros en la misma sentencia.

#### call
- nombre del stored procedure con sus parametros.

## Sub objetos
- puede ser cualquiera de los objetos del [step](step.md) del flujo de trabajo.
