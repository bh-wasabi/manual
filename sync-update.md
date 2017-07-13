# Objeto: **update** (sync)
- aquí se configura la actualización de datos en SQL desde la sección del documento que se sincroniza.

## Parámetros
- no tiene parámetros

## Sub objetos

#### where
- campos llaves de la tabla.
- tipo campo="valor", puede ser multiple y el valor puede tener [expresiones](expr.md).
- Nota: hay que tener mucho cuidado para no actualizar cosas que no corresponde.

#### set
- aquí vamos a actualizar los campos de la tabla parados en la sección del documento, las llaves que vamos a indicar son los nombres de los campos de la tabla SQL y los valores salen de la sección del documento.
- tipo campo="valor", puede ser multiple y el valor puede tener [expresiones](expr.md).

## Ejemplo:
Este ejemplo genera la siguiente sentencia de SQL: `UPDATE art SET descripcion=$descripcion, tipo=$tipo, grupo=$grupo, familia=$familia WHERE articulo=$articulo`, para cada uno de los detalles de la sección.
````
{{#sync id="articulos" type="sql" table="art"}}
  {{#update}}
    {{where articulo="articulo"}}
    {{set descripcion="descripcion"}}
    {{set tipo="tipo"}}
    {{set grupo="grupo"}}
    {{set familia="familia"}}
  {{/update}}
{{/sync}}
````