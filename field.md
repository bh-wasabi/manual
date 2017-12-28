# Objeto: **field**
- define un campo del documento
- normalmente van dentro de una sección

## Parámetros
#### id
- identificador de la sección

#### type
- `text` campos tipo texto (por omisión)
- `number` campos numéricos
- `date` fechas (con o sin hora)
- `boolean` lógicos (true, false)
- `calc` campo calculado que regresa un valor numérico
- `expr` campo calculado que regresa cualquier tipo de valor
- `doc` es posible definir un sub documento que va en el campo.
- `multiple-doc` es posible definir un arreglo de sub documentos que va en el campo.
- `count` calcula el conteo de una sección especifica del documento
- `sum` calcula la suma el campo que esta definido en `value` de una sección especifica del documento.
- `avg` calcula el promedio del campo que esta definido en `value` de una sección especifica del documento.
- `max` calcula el valor máximo del campo que esta definido en `value` de una sección especifica del documento.
- `min` calcula el valor máximo del campo que esta definido en `value` de una sección especifica del documento.

#### label
- es la etiqueta a desplegar por omisión.

#### labelModalClass
- es posible agregar una clase a la etiqueta cuando se hace el modal.

#### align
- `left`
- `right`
- `center`

#### format
- en los campos tipo number, calc y date, se puede especificar un formato especifico
- el sistema va usar [Moment.js](http://momentjs.com) para formatear las fechas y [Numeral.js](http://numeraljs.com) para formatear los números.
- existen algunos valores pre-definidos como: `format="currency"`.
- la opción `format="currency2"` tiene la ventaja de que si el valor es cero no lo pinta.
- el si se indica `format="pesos"` convierte un importe a texto.
- el si se indica `format="phone334"` formatea un teléfono de 10 dígitos.

#### saveFormat
- en el caso de las fechas es posible definir el formato al guardar.

#### value
- en el caso de campos calculados `calc` y expresiones `expr`, aquí se asigna la [expresión](expr.md) que se usa para calcular el valor.
- en el caso de agregaciones `sum`, `avg`, `min` y `max` aquí se define el campo a utilizar, es necesario indicar también la sección `section` donde esta el campo.

#### section
- se usa para `count`, `sum`, `avg`, `min` y `max`.

Ejemplo:
````
{{#section id="totales"}}
  {{field id="conteo" type="count" section="articulos"}}
  {{field id="importe" type="sum" section="articulos" value="importe"}}
{{/section}}
````

#### defaultValue
- asigna el valor por omisión a un campo.
- puede ser una expresión
- si el campo es de una sección tipo arreglo, es posible asignar una lista de valores separados por comas.

#### if
- con esta opción es posible condicionar la visibilidad el campo.
- genera un [facilitador if](helper-if.md) automáticamente, que se evalúa el contexto al momento de ejecución de la página.
- Nota: no se pueden poner expresiones aquí, lo que se puede es tener un campo calculado con la expresión necesario y aquí evaluar el campo.

#### isRules (true, false)
- se le indica al campo donde vienen las reglas que vamos a usar en el calculo.

#### source
- tipo de documento que se va usar como fuente en las capturas.

#### sourceExpr
- es posible basar el tipo de documento usando una expresión.
- para que funcione correctamente es necesario hacer un [refresh](on-change.md) de la forma para que se actualice la fuente.

#### view
- se puede indicar la vista especifica del `source`.
- por omisión toma la vista definida en el tipo de documento en `defaultView`.

#### sourceFilter
- se puede especificar el campo remoto donde se va aplicar el filtro
- este tipo de filtros pueden funcionar en tiempo real sobre la misma forma, evita hacer un "refresh".

#### sourceFilterValue
- aquí se pasa el valor que se va a mandar al filtro.
- puede ser una [expresion](expr.md)

#### helpText
- una forma rápida de armar la ayuda en captura del campo.

#### helpType
- `popover` aparece una ventana de ayuda volátil sobre la etiqueta.
- `popup` aparece una ventana de ayuda que el quita al hacer click afuera de la ventana o el botón de cerrar si tiene título.

#### helpTemplate
- en caso de querer usar el `helpType`
- con esta opción es posible asignar un [template](template.md) a la ventana de ayuda.

#### helpTitle
- es posible establecer un título sobre la ventana de ayuda.
- funciona en `helpType="popup"`.

#### helpWidth
- es posible definir el ancho de la ventana de ayuda.
- funciona en `helpType="popup"`.

#### helpHeight
- es posible definir el alto de la ventana de ayuda.
- funciona en `helpType="popup"`.

#### map
- en algunos casos es posible indicar otro nombre del campo, para hacer ciertos mapeos específicos.

#### isImage (true, false)
- un campo tipo texto, puede contener la url de una imagen.
- es otra forma de anexar mas directa y con la posibilidad de editar en la misma forma de captura donde van los demás campos.

#### isImageFace (true, false)
- tratar de obtener la cara de la persona.
- esto funciona actualmente para la parte `mobile`.

#### imageHeight 
- alto de la imagen

#### imageWidth 
- ancho de la imagen

#### imageFit 
- ajusta la imagen a los tamaños especificados.

#### boldIf
- es posible agregar una condición para que se despliega el campo en negritas.
- funciona únicamente en secciones tipo arreglo
- debe ser una expresión.

#### isFlag (true, false)
- define si el campo va a desplegar una bandera en las tablas.
- requiere un preset con los `id's` de las banderas

#### changeOnClick (true, false)
- es posible hacer un cambio sin la necesidad de abrir el documento.
- esto funciona únicamente con la opción `isFlag="true"`.
- hace un carrusel del preset.

#### placeholder
- cuando es `type="doc"` o `type="multiple-doc"`, es posible definir el valor a mostrar en el botón.

## Sub objetos

#### [editor](editor.md)
- el sistema soporta diferentes ayudas en captura, que se definen a travez de la configuración del editor.

#### [validator](validator.md)
- se pueden agregar una o varias validaciones de captura.

#### [onChange](on-change.md)
- se pueden configurar un evento cuando el campo cambia de valor.

#### [style](style.md)
- es posible cambiar algunas cosas adicionales de diseño.
- esta opción actualmente funciona únicamente en formas PDF.