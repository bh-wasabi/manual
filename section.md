# Objeto: **section**
- define una sección del documento
- los documentos editables forzosamente se tienen que estructurar en secciones/campos.
- las secciones no son recursivas.

## Parámetros
#### id
- identificador de la sección

#### label
- etiqueta de la sección

#### type (object, array)
- `object` son la secciones que contienen campos directos (por omisión).
- `array` es una sección múltiple, para detalles.

#### temp o temporal (true, false)
- define si es una sección temporal
- si se activa, la sección no se guarda en la base de datos.
- es muy útil cuando queremos guardar temporalmente los datos de un widget en la forma.

#### validateSignature (true, false)
- es posible validar la firma electrónica de la sección antes de guardar el documento.
- esto se recomienda en secciones calculadas por el servidor que regresan al cliente a modo de consulta o para usarse como pasos intermedios.

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

#### view
- vista a usar

#### source
- documento a usar en la vista
- por omisión toma el tipo de documento actual.

#### dmn 
- identificador de la tabla DMN, se tiene que subir previamente con un `make`.

#### fusionOnce
- con esta opción es posible usar multiples tablas DMN para generar el resultado.
- lista de tablas DMN separadas por comas.
- esta opción lo hace una sola vez con el primer registro que se enviar al DMN.

#### fusionAll
- con esta opción es posible usar multiples tablas DMN para generar el resultado.
- lista de tablas DMN separadas por comas.
- esta opción lo hace para cada registro que se enviar al DMN.

#### input o body
- es una forma de pasar los parámetros usando una sección completa, incluso puede ser un arreglo
- en el caso de dmn, se pueden mandar arreglos de arreglos y se van a considerar todo como un solo arreglo.

#### output
- se puede especificar un campo de salida unitario

#### map
- es posible concertar los resultados
- lista de campos separada por comas

#### reduce
- es posible reducir los resultados
- lista de campos separada por comas

#### compact (true, false)
- si se ejecuta map/reduce elimina los registros que no tienen valor.

#### pluck
- es posible extraer un campo del resultado, cuando es tipo arreglo

#### orderBy
- al final es posible ordenar el resultado por algún campo.

#### forceCalcOrder (true, false)
- los campos calculados van con un orden específico (calcOrder).

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

#### [valueFrom](valueFrom.md)
- obtiene el valor de otra forma mas compleja
- pueden ser vistas o tablas `DMN`.

