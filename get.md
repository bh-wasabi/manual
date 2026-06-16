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
- `usd` / `dolar-fix`
- `eur` / `euro`
- `cad` / `dolar-canadiense`
- `yen`
- `udis`
- `tiie` / `tiie-28d`
- `tiie-91d`
- `cetes-28d`
- `reservas-internacionales`
- `dolar-liquidacion`
- `libra-esterlina`
- `tasa-objetivo`

#### dmn
- es posible ejecutar una tabla de decisión (DMN). 
- puede ser una expresión.

#### input o body
- en las vistas en posible enviar un body.
- por omisión se manda el documento actual.

#### body1, body2, body3
- en las vistas en posible enviar un body como arreglo.
- por omisión se manda el documento actual en body1.

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
