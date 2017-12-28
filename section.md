# Objeto: **section**
- define una sección del documento
- los documentos editables forzosamente se tienen que estructurar en secciones/campos.
- las secciones no son recursivas.

## Parámetros
#### id
- identificador de la sección

#### type (object, array)
- `object` son la secciones que contienen campos directos (por omisión).
- `array` es una sección múltiple, para detalles.

#### temp o temporal (true, false)
- define si es una sección temporal
- si se activa, la sección no se guarda en la base de datos.
- es muy útil cuando queremos guardar temporalmente los datos de un widget en la forma.

#### beforeStart (true, false)
- se recalcula la sección al abrir el documento, siempre.
- es mejor que sean temp="true" este tipo de secciones.

#### afterAffect (true, false)
- se actualiza esta sección leyendo de una vista, después de correr spAffect.

#### afterAffectView
- nombre de la vista a leer.
- si la vista tiene parámetros hay que usar `param`.

#### isOpenPayCard (true, false)
- para definir si la sección es para capturar una tarjeta de crédito con OpenPay
- requiere mapear los campos (`card_number, holder_name, expiration_month, expiration_year, cvv2 y token`).

#### defaultValue
- es posible establecer una valor por omisión a una sección completa.
- puede ser un preset.
- puede ser una expresión.

#### transform
- es posible generar la sección usando una transformación.

#### updateFromArray
- actualiza la sección (tipo arreglo) basada en un arreglo.

#### updateFromArrayId
- llave del arreglo

#### updateFromArrayKey
- llave local

#### confirmBeforeSave
- es posible confirmar antes de guardar la sección
- puede ser una [expresión](expr.md).

#### confirmBeforeSaveTitle
- título de la ventana de confirmación
- puede ser una [expresión](expr.md).

#### confirmBeforeSaveMessage
- mensaje de la ventana de confirmación.
- puede ser una [expresión](expr.md).

#### confirmBeforeSaveHeight (#)
- alto de la ventana de confirmación
- opcional

#### confirmBeforeSaveWidth (#)
- ancho de la ventana de confirmación
- opcional

## Sub objetos

#### [field](field.md)
- campos de la sección

#### [object](section-object.md)
- se pueden generar sub objetos, como resultado de transformaciones o campos calculados, que se pueden guardar directamente sobre el documento.
- unicamente de lectura.

#### [validator](validator.md)
- se pueden agregar una o varias validaciones de captura a nivel sección.
- unicamente tipo `expr`. 

#### [param](param.md)
- parámetros 
- se usa cuando en `afterAffect="true"`

#### [onChange](on-change.md)
- es posible generar eventos cuando se modifica la sección.

