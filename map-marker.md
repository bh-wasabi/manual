# Objeto: **marker** (map)
- define las marcas en el mapa.

## Parámetros
#### section
- sección del documento que contiene los marcadores.
- si no se indica va usar los datos de la vista del `widget`.

#### location
- campo o [expresión](expr.md) que contiene la localidad.
- puede ser una dirección o una coordenada.

#### latitude
- es posible definir la latitud directamente.

#### longitude
- es posible definir la longitud directamente.

#### tooltip
- campo o [expresión](expr.md) que contiene el nombre a mostrar al pararse sobre el marcador.

#### pin
- es posible asignar una url diferente para pintar las marcas.
- por omisión es: `https://s3.amazonaws.com/mx-imagenes/pin-red/default.png`.


