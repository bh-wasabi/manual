# Objeto: **get**
- obtiene un documento

## Parámetros
#### id
- identificador del documento

#### source
- tipo de documento
- por omisión es en el mismo tipo de documento que se encuentra.

#### rate
- es posible leer el tipo de cambio de una moneda.

#### as
- con esta opción es posible cambiar el nombre del objeto para el contexto.

## Sub objetos

#### [set](set.md)
- para modificar un campo del la sección.

## Ejemplos:
`````
{{#onChange}}
  {{#get rate="=moneda" as="_rate"}}
    {{set tipoCambio="=_rate.value"}}
  {{/get}}
{{/onChange}}
`````