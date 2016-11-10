# Objeto: **editor**
- define el editor de un campo

## Parámetros
##### type
- `text` texto simple sin ayuda.
- `text-area` area de texto multi-renglón.
- `select` seleccionar de una lista de opciones, necesita `preset` o `source`.
- `lookup` búsqueda avanzada sobre el campo, necesita `preset` o `source`.
- `autocomplete` sugiere el texto en base a la lista de opciones, necesita `preset` o `source`.
- `tags` multiples etiquetas, necesita `preset` o `source`.
- `number`
- `date` para capturar una fecha.
- `datetime` para capturar fecha con hora.
- `time` para capturar una hora.
- `calendar`
- `checkbox`
- `color`
- `progress-bar`
- `range-slider`
- `slider`
- `switch`
- `file-uploader` cargar archivos.
- `options` para capturar las opciones de un artículo, necesita `parent` (campo que tiene el artículo) y `source` (colección del artículo, debe estar definido `optionsSection` en esa colección).

##### preset
- ayuda en captura para tablas pequeñas (key/value) es están en memoria).

##### presetCondition
- en el caso de un `grid` es posible condicionar la ayuda en captura en general.
- en necesario activar `alwaysLoad="true"`.
- puede ser una expresión.
- muy útil cuando se necesita que algunas columnas "funcionen" en ciertos casos.

##### presetElse
- en el caso de una condición `presetCondition` es posible establecer un resultado para cuando no se cumple la condición.
- en necesario activar `alwaysLoad="true"`.
- puede ser una expresión.
- puede ser una lista separada por comas.

ayudas predefinidas:
- `status`, Activo, Bloqueado, Inactivo.
- `boolean`, Si, No.
- `priority`, Urgente, Alta, Normal, Baja, Muy baja.
- `months` Enero, Febrero, Marzo, Abril, etc.
- `countries` lista de países del mundo.

basados en el mismo documento:
- `doc.[section]` va a buscar específicamente en el documento actual que exista esa sección (tipo arreglo y los campos `id` y `name`).

basados en las configuración:
- `user.[section]` va a buscar específicamente en el usuario que exista esa sección (tipo arreglo y los campos `id` y `name`).
- `company.[section]` va a buscar específicamente en la empresa que exista esa sección (tipo arreglo y los campos `id` y `name`).
- `tenant.[section]` va a buscar específicamente en el tenant que exista esa sección (tipo arreglo y los campos `id` y `name`).
- `app.[section]` va a buscar específicamente en la configuración general que exista esa sección (tipo arreglo y los campos `id` y `name`).

##### source
- cuando la ayuda en captura la queremos basar de otro tipo de documento.
- por omisión usa lo que esta definido en [field](field.md).

##### sourceFindOne
- cuando se usa `getSourceSection` aquí podemos especificar el campo que contiene el identificador del documento.
- puede ser una [expresión](expr.md), el contexto es la sección actual y el documento.

##### sourceFindOneDisableCache (true, false)
- el sistema genera un cache por omisión para este tipo de ayudas en captura.
- con esta opción es posible des-habilitar el cache.
- por omisión es `false`.

##### getSourceSection
- es posible usar una sección especifica de un documento como ayuda en captura.
- es necesario usar `sourceFindOne` para filtrar el documento.
- la sección debe tener los campos `id` y `nombre`.

##### view
- se puede indicar la vista especifica del `source`.
- por omisión toma la vista definida en el tipo de documento en `defaultView`.

##### parent
- campo padre 
- en `select-current` se especifica el campo a usar como base del filtro.
- en `options` se define el campo que tiene el artículo.

##### alwaysLoad (true, false)
- con esta opción forzamos que vuelva a leer la ayuda en captura.
- es muy útil cuando se quiere hacer una ayuda en captura basada en otros campos capturados (en la misma sección) y sobre todo cuando se quiere evitar hacer el `refresh`.
- Nota: para que funcione correctamente esta opción es necesario usar antes `clearFields` del evento `onChange` del campo padre.

##### visible (true, false)
- podemos ocultar un campo con esta opción.

##### readOnly (true, false)
- bloquea la edición

##### spellcheck (true, false)
- activa el corrector ortográfico sobre el campo.

##### placeholder
- etiqueta a desplegar sobre el campo cuando esta vacío.

##### searchEnabled (true, false)
- en algunos editores se puede habilitar la búsqueda con esta opción.

##### showClearButton (true, false)
- muestra un botón que permite borrar el contenido del campo.

##### showSelectionControls (true, false)
- en el caso `type="tags"` con esta opción podemos agregar la selección por `checks` adicional.

##### applyValueMode
- `instantly` valor por omisión.
- `useButtons` aparecen los botones de aceptar y cancelar, cuando es un editor tipo: `tags, date, color, lookup`.

##### hideSelectedItems (true, false)
- escode los elementos previamente seleccionados.

##### multiline (true, false)
- si se pone `false` el campo no crece de tamaño en la forma y genera un scroll a los lados.
- por omisión es `true`.

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
- funciona únicamente con los tipos `file-uploader` y `checkbox`.

##### hint
- es posible agregar una ayuda adicional al campo
- aparece si se para el cursor encima del campo después de un momento.

##### sendSearchValue (true, false)
- cuando se captura en un `grid`, con esta opción podemos mandar el parámetro `searchValue` a la consulta del servidor.

## Sub objetos

##### [item](editor-item.md)
- lista de opciones a seleccionar.

##### [filter](filter.md)
- es posible indicar filtros que se van a aplicar al abrir la ayuda en captura.
- funciona cuando el tipo es `select`, `lookup` o `autocomplete`.

>##### Nota: En los filtros hay 2 contextos disponibles
1. Todos los campos misma sección (invocando al campo directo, `this.campo` o `@campo`)
2. El documento completo.

- los campos de la sección se modifican directamente (y pueden usarse como base de los filtros sin necesidad de refrescar la forma) y los campos del documento cuando se acepta la forma modal.

##### [param](param.md)
- es otra forma de definir los filtros, en algunas ocaciones es más fácil definirlo así.

##### [grid](editor-gird.md)
- en el caso de captura tipo `grid` es posible tener una ayuda de captura con otro `grid`.
- por el momento únicamente funciona con preset's.

