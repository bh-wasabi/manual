# Objeto: **editor**
- define el editor de un campo

## Parámetros
##### type
- `text` texto simple sin ayuda.
- `text-area` area de texto multi-renglón.
- `select` seleccionar de una lista de opciones.
- `lookup` búsqueda avanzada sobre el campo.
- `autocomplete` sugiere el texto en base a la lista de opciones.
- `tags` multiples etiquetas.
- `number`
- `date`
- `calendar`
- `checkbox`
- `color`
- `progress-bar`
- `range-slider`
- `slider`
- `switch`
- `file-uploader` cargar archivos.

##### preset
predefinidos:
- `status`, Alta, Bloqueado, Baja.
- `boolean`, Si, No.
- `priority`, Urgente, Alta, Normal, Baja, Muy baja.
- `months` Enero, Febrero, Marzo, Abril, etc.
- `countries` lista de países del mundo.
- `collections` lista de colecciones de la base de datos.
- `sources` lista de tipos de documentos.

basados en las configuraciones `_user`, `_company`, `_tenant` y `_config`:
- `section` en este caso el sistema va a buscar en ese mismo orden (usuario, empresa, tenant y por ultimo config) que exista la sección (tipo arreglo y los campos `id` y `name`).
- `_user/section` va a buscar específicamente en el usuario que exista esa sección (tipo arreglo y los campos `id` y `name`).
- `_company/section` va a buscar específicamente en el usuario que exista esa sección (tipo arreglo y los campos `id` y `name`).
- `_tenant/section` va a buscar específicamente en el usuario que exista esa sección (tipo arreglo y los campos `id` y `name`).
- `_config/section` va a buscar específicamente en el usuario que exista esa sección (tipo arreglo y los campos `id` y `name`).

##### visible (true, false)
- podemos ocultar un campo con esta opción.

##### readOnly (true, false)
- bloquea la edición

##### spellcheck (true, false)
- activa el corrector ortográfico sobre el campo.

##### placeholder
- etiqueta a desplegar sobre el campo cuando esta vacío.

##### showClearButton (true, false)
- muestra un botón que permite borrar el contenido del campo.

##### maxLength (#)
- con esta opción se puede limitar el tamaño de un texto.

##### mask
- [mascara de edición](mask.md)
- por ejemplo: `mask="+52 (00) 0000-0000"`

##### maskChar
- se puede cambiar el símbolo que aparece al capturar con mascaras
- por omisión es "_"

##### format
- formato de presentación para valores numéricos o de fecha.

##### case
- `upper` forza la captura a que sean mayusculas
- `lower` forza la captura a que sean minusculas
- `capitalize` la primera letra de cada palabra la pone en mayusculas con excepción de las preposiciones.

##### mode
- `text` por omisión.
- `email` para capturar una dirección de correo electrónica.
- `search`
- `tel`
- `url`
- `password`

##### min
- valor mínimo (numérico)

##### max
- valor máximo (numérico)

##### showSpinButtons (true, false)
- en el caso de valores numéricos muestra unas flechas para incrementar o decrementar el valor.

##### height
- se puede indicar la altura en pixeles del campo, sobre todo es útil cuando el tipo es: `text-area`.

##### width
- también podemos controlar el ancho en pixeles del campo, por omisión se ajusta automáticamente.

##### items
- se pueden especificar directamente la lista de opciones separadas o comas
- también soporta una [expresión](expr.md) que en este caso debe devolver un arreglo.
- ejemplo 1: `items="Mexico, USA, Canada"`
- ejemplo 2: `items="=[{id: 'mx', name: 'Mexico'}, {id: 'us', name: 'USA'}, {id: 'ca', name: 'Canada'}]"`

##### value
- campo que contiene el valor dentro de la lista de opciones, por omisión es `id`.

##### display
- campo que contiene el nombre a desplegar dentro de la lista de opciones, por omisión es `name`.

##### allowNew
- con esta opción permite agregar valores nuevos al vuelo.
- actualmente funciona en capturas tipo hoja.

##### allowEmpty
- con esta opción permite borrar el campo y dejarlo sin valor.
- actualmente funciona en capturas tipo hoja.

##### accept
- lista de tipos [MIME](http://web.archive.org/web/20140715072214/http://www.utoronto.ca/webdocs/HTMLdocs/Book/Book-3ed/appb/mimetype.html) de archivo que se aceptan
- por ejemplo: `accept="audio/mpeg,audio/wav"`.
- funciona con el tipo `file-uploader`

##### selectButtonText
- se puede indicar el mensaje a desplegar para seleccionar un archivo.
- funciona con el tipo `file-uploader`

##### labelText
- etiqueta a desplegar
- funciona con el tipo `file-uploader`

## Sub objetos

##### [item](editor-item.md)
- lista de opciones a seleccionar.
