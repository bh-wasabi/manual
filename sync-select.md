# Objeto: **select** (sync)
- aquí se configura la obtención de datos para actualizar la sección del documento que se sincroniza.

## Parámetros
#### call
- para ejecutar un stored procedure, ya sea que de ahi salga los datos, o también puede servir para preparar los datos antes de leer la tabla o hacer un `query` más sofisticado.
- opcional

#### query
- para mandar un consulta más sofisticada de multiples tablas.
- opcional

## Sub objetos

#### param
- asigna valor a los parámetros, ya sean para hacer un `call` o un `query`.
- tipo campo="valor", puede ser multiple y el valor puede tener [expresiones](expr.md).

#### where
- llaves para filtrar al obtener los datos de la tabla.
- tipo campo="valor", puede ser multiple y el valor puede tener [expresiones](expr.md).

#### set
- aquí vamos a generar la sección del documento, las llaves que vamos a indicar son los nombres de los campos de la sección y los valores son los campos de la tabla SQL.
- tipo campo="valor", puede ser multiple y el valor puede tener [expresiones](expr.md).

## Ejemplo:
En este ejemplo, primero se ejecuta `sp_refresh_articulos($tenant, $empresa)` usando los parámetros indicados, después el sistema hace una consulta a la tabla `SELECT articulo, descripcion, tipo, grupo, familia FROM art` y con esto sustituye la sección del documento.
````
{{#sync id="articulos" type="sql" table="art"}}
  {{#select}}
    {{set articulo="articulo"}}
    {{set descripcion="descripcion"}}
    {{set tipo="tipo"}}
    {{set grupo="grupo"}}
    {{set familia="familia"}}
  {{/select}}
{{/sync}}
````