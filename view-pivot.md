# Objeto: **pivot** (view)
- pivotea los resultados de la vista.
- para usarse en reportes con matrices (es como una vista de un cubo estática)

## Parámetros
#### cols
- lista de columnas

#### cols
- lista de columnas separadas por comas.

#### rows
- lista de renglones separadas por comas.

#### measures
- lista de medidas separadas por comas.

#### totals (true, false)
- incluye información para generar totales y subtotales en la matriz.

#### totalsLabel
- nombre a mostrar para los totales.

## Ejemplo:
````
{{#view id="pivot"}}
  {{#all}}
  {{calc field="amount" value="quantity*price"}}
  {{pivot cols="category" rows="country" measures="quantity" totals="true" totalsLabel="Total"}}
{{/view}}
````