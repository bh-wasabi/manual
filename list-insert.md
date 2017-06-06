# Objeto: **insert**
- con esta opción es posible definir mas posibles documentos a insertar.

## Sub objetos
##### [item](item.md)
- documento a insertar, es necesario definir `id`y `label`.


## Ejemplo
````
{{#browser id="lista" view="lista2" showDoc="true" docOrientation="vertical" docPosition="75%" zoom="70%" mobile="detalle"}}
  {{#list itemTemplate="lista" allowSearch="true" allowRefresh="true" allowEdit="true" allowInsert="true"}}
    {{#insert}}
      {{item id="asegurado" label="Asegurado"}}
      {{item id="aviso-accidente" label="Aviso Accidente"}}
    {{/insert}}
  {{/list}}
{{/browser}}
````