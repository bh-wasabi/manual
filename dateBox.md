# Objeto: **dateBox**
- sirve para capturar parámetros a usar en otros `widgets`.

## Parámetros
#### type
- `date` (por omisión).
- `time`
- `datetime`

#### placeholder
- etiqueta a mostrar cuando el combo esta vacío.

#### width
- con esta opción es posible controlar el ancho del combo.
- es mejor usar `{{row}}` y `{{col}}` para controlar las posiciones y los anchos.

#### forceLastSecond (true, false)
- le agrega 59 segundos si es `type="datetime"`