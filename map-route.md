# Objeto: **route** (map)
- define la ruta en el mapa.

## Parámetros
#### section
- sección del documento que contiene las rutas.
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

#### mode
- `driving` por omisión.
- `walking`

#### color
- es posbile cambiar el color de la ruta.
- por omisión es `blue`.

#### weight
- especifica el grueso (en pixeles) de la línea que marca la ruta.
- por omisión es `6`

#### opacity
- define el nivel de opacidad de la línea que marca la ruta.
- por omisión es `0.5`
