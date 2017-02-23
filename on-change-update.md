# Objeto: **update** (onChange)
- actualiza una sección completa del documento
- se pueden usar como contexto la sección actual, el documento remoto (cuando se usa ayudas en captura tipo `lookup`, `select` o `autocomplete`), y el documento local.

## Parámetros
##### section
- sección del documento a actualizar.

##### value
- valor a asignar.
- puede ser una [expresión](expr.md).

##### pushValue
- es posible agregar mas elementos en lugar de reemplazarlos completamente.
- puede ser una [expresión](expr.md).

##### condition
- es posible establecer una condición para que se ejecute
- puede ser una [expresión](expr.md).

## Sub objetos

##### [set](set.md)
- actualiza el valor de uno o varios campos.

## Ejemplos:
`````
{{#onChange}}
  {{update section="articulos" value="=articulos"}}
{{/onChange}}
`````