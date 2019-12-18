# Objeto: **search**
- define los campos por los que se va efectuar la búsqueda.

## Parámetros
#### index
- indice

#### type
- tipo de documento

#### limit (#)
- limite de registros

#### sort
- orden

#### filterParamsOnlySearch (true, false)
- con esta opción se puede controlar que se aplique los filtros de los parámetros únicamente cuando esta buscando y cuando lee algo unitario lo hace sin los filtros.
- esta opción sirve para cuando se quiere tener un estatus de algunos registros pero que siga funcionando con lo capturado anteriormente.

## Sub objetos

#### [param](param.md)
- parametros a enviar