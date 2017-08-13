# Objeto: **param**
- asigna uno o múltiples parámetros

## Parámetros
#### parametro="valor"
- nombre del parámetro y su valor a pasar
- el valor puede ser una [expresión](expr.md)
- se pueden pasar múltiples parámetros juntos sobre el mismo objeto, separados por un espacio.
- es posible usar el prefijo `#` cuando se quiere leer el valor de un `widget` directamente.

#### condition
- es posible establecer una condición para mandar el parámetro

#### format
- es posible aplicar un formato antes de generar el parámetro

## Ejemplos

- parámetros unitarios

````
{{param id="factura"}}
{{param name="Factura"}}
{{param pagesStart="1"}}
{{param pagesJustified="true"}}
{{param allowDirectOperations="true"}}
{{param allowEdit="true"}}
{{param allowAdd="true"}}
````

- mútiples parámetros juntos

````
{{param id="factura" name="Factura" pagesStart="1" pagesJustified="true" allowDirectOperations="true" allowEdit="true" allowAdd="true"}}
````

- widgets usando combos.

````
{{#widget type="cube" source="facturas" cube="resumen"}}
  {{param ejercicio="#ejercicio"}}
{{/widget}}
````