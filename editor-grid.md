# Objeto: **grid** (editor)
- en el caso de captura tipo `grid` es posible tener una ayuda de captura con otro `grid`.
- por el momento únicamente funciona con preset's.


## Sub objetos
##### column
- define una columna de la ayuda
- únicamente se pueden usar los parámetros: `field`, `label` y `width`.


## Ejemplo
````
{{#field id="moneda" type="text" label="Moneda"}}
  {{#editor type="select" preset="app.moneda"}}
    {{#grid}}
      {{column field="nombre" label="Nombre" width="200"}}
      {{column field="id" label="Identificador" width="100"}}
    {{/grid}}
  {{/editor}}
{{/field}}
````