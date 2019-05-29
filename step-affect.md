# Objeto: **affect** (step)
- afecta un documento en SQL.

## Parámetros
#### action
- `afectar` 
- `cancelar`

#### condition
- es posible determinar una condición

#### stopNotify
- si no pudo continuar por la condición, emite una notificación al usuario.

#### url
- en el caso del `engine="post"`

#### engine
- `mysql` por omision
- `mssql`
- `node`
- `post`

#### sp
- nombre del `stored procedure` que se ejecuta
- por omisión es `spAffect` y tiene 2 parámetros (`params` y `doc`) en el caso se `mysql` son `JSON` y en el caso de `mssql` son `XML`.
- el sp debe regresar una consulta con los siguientes datos: `ok`, `okRef`, `message`, `type` y `reference`.

## Sub objetos
#### update
- es posible efectuar un `update` al documento afectado.
- se tiene en el `scope` las siguientes variables (`ok, okRef, message, type, reference`).

#### split
- siempre y cuando la afectación no mande errores previos.
- permite dividir un documento en múltiples documentos.
- puede tener un `condition`.