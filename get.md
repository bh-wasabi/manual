# Objeto: **get**
- obtiene un documento

## Parámetros

#### id
- identificador del documento

#### source
- tipo de documento
- por omisión es en el mismo tipo de documento que se encuentra.

#### view
- nombre de la vista opcional.

#### rate
- es posible leer el tipo de cambio de una moneda.
- puede ser una expresión.

#### dmn
- es posible ejecutar una tabla de decisión (DMN). 
- puede ser una expresión.

#### input o body
- en las vistas en posible enviar un body.

#### body1, body2, body3
- en las vistas en posible enviar un body como arreglo.

#### as
- con esta opción es posible cambiar el nombre del objeto para el contexto.

## Sub objetos

#### [set](set.md)
- para modificar un campo del la sección.

#### [param](param.md)
- en algunos casos se requieren parámetros.

## Ejemplos:
`````
{{#get rate="'usd'" as="_usd"}}
  {{set tipoCambio="=_usd.value"}}
{{/get}}
`````