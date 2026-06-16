# Objeto: **sync**
- sirve para sincronizar una sección del documento con otra fuente de datos (por ejemplo una tabla de SQL).
- así podemos usar las capturas de documentos para actualizar algunas de las tablas de SQL.

## Parámetros
#### id
- identificador del sincronizador

#### type
- `sql` base de datos tipo SQL.

#### table
- nombre de la tabla de SQL a sincronizar.

## Sub objetos

#### [select](sync-select.md)
- comando para obtener los datos nuevos desde SQL.
- se puede usar con `query` o con `call`.

#### [update](sync-update.md)
- comando para actualizar los datos en la base SQL.

## Ejemplos:
````
{{#sync id="normalizar" type="sql" table="norm"}}
  {{#select call="sp_refresh_norm($tenant)"}}
    {{param tenant="_id"}}
    {{where tenant="_id"}}
    {{set campo="campo"}}
    {{set llave="llave"}}
    {{set valor="valor"}}
  {{/select}}
  {{#update}}
    {{where tenant="_id"}}
    {{where campo="campo"}}
    {{where llave="llave"}}
    {{set valor="valor"}}
  {{/update}}
{{/sync}}
````

