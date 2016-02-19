# Objeto: **section**
- define una sección del documento
- los documentos editables forzosamente se tienen que estructurar en secciones/campos.
- las secciones no son recursivas.

## Parámetros
##### id
- identificador de la sección

##### type (object, array)
- `object` son la secciones que contienen campos directos (por omisión).
- `array` es una sección múltiple, para detalles.

##### temp (true, false)
- define si es una sección temporal
- si se activa, la sección no se guarda en la base de datos.
- es muy útil cuando queremos guardar temporalmente los datos de un widget en la forma.

## Sub objetos

##### [field](field.md)
- campos de la sección

##### [object](section-object.md)
- se pueden generar sub objetos, como resultado de transformaciones o campos calculados, que se pueden guardar directamente sobre el documento.
- unicamente de lectura.