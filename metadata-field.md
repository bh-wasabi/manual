#### document
- tipo de documento

#### field
- id del campo

#### order
- orden en la forma

#### section
- sección a la que corresponde el campo
- por omisión es `base`

#### display
- nombre o etiqueta del campo

#### display2
- nombre en el segundo idioma

#### type
- `text` campo tipo texto de un reglón
- `text-area` campo tipo text multi-renglón
- `number` campo numérico
- `date` campo fecha
- `datetime` campo fecha y hora
- `time` campo hora
- `boolean` campo lógico (true/false)
- `calc` campo calculado de valor numérico
- `code` ayuda en captura usando la hoja del code.
- `embed` sub documento 
- `expr` campo calculado de cualquier tipo
- `file-uploader` permite cargar un archivo
- `lookup` campo con ayuda en captura abierta tipo ElasticSearch que no es un id de mongo
- `password` campo enmascadaro en la captura
- `preset` ayuda de captura de los presets internos
- `reference` ayuda en captura usando una colección de la base de datos
- `select` ayuda en captura que se puede definir dinámicamente en el mismo campo al momento de la forma
- `siNo` ayuda en caputura tipo Sí/No
- `table` define una sección tipo arreglo
- `text-id` campo tipo texto para identificadores
- `url` campo tipo URL

#### references
- id del documento a usar como ayuda en captura

#### view
- id de la vista a usar como ayuda en captura
- por omisión usar `lista`

#### format
- format a usar
- es tipo fecha se pone el formato de fecha y/o hora tipo moment.js
- si es numérico el formato tipo numeral.js o `currency`

#### multiple (booleano)
- permite definir el campo soporta multiples valores.

#### readOnly (booleano)
- define si es unicamente de lectura

#### required (booleano)
- define si es requierido

#### requiredOnAffect (booleano)
- valida al afectar que efectivamente este campo tenga valor.

#### parent
-

#### case
- si tipo texto puede ser `upper`, `lower`, `capitalize`

#### value
-

#### defaultValue
- valor por omisión al crear el documento

#### defaultValue2
-

#### status
- estatus de tipo comentario

#### comentaries
- comentarios sobre el campo

#### group
- grupo al que pertence el campo

#### exportBI
-

#### acceptFile
-

#### author
- nombre o iniciales del autor del cambio

#### ignore (booleano)
- es posible comentar los renglones del metadata usando esta columna, tambien se recomienda poner el color de las letras en gris para que sea más visual lo comentado.

#### include
- lista de proyectos (separados por comas) que se desean incluir.

#### exclude
- lista de proyectos (separados por comas) que se desean excluir.

#### height
- altura en pixeles para los campos de altura variable tipo `text-area`

#### title
- 

#### title2
-

#### fieldSetHeader
- es posible poner un encabezado en la captura en el modal

#### fieldSetHeader2
- es el encabezado cuando se compila en en idioma alterno

#### sameLine
- es posible poner 2 campos en la misma línea
- debe ir por parejas de `start` y `end`

#### detach
- dentro de la misma sección es posible separar un bloque de campos si se usa esta leyenda.

#### detach2
- lo mismo para el idioma alterno

#### doubleEnter
- cuando son campos multiples es posible definir que se inserte un `enter` adicional para separar los valores.

#### hasHtml (booleano)
- si el contenido de este campo tiene HTML es necesario indicarlo para que se presente correctamente.

#### refresh (booleano)
- por medio de esta propiedad el sistema refrescar las condiciones de visibilidad de otros campos en el modal.

#### isTrue
- si el campo es tipo siNo, aqui se puede indicar el id del campo calculado automatico que se va asignar si el valor es `si`.

#### isFalse
- si el campo es tipo siNo, aqui se puede indicar el id del campo calculado automatico que se va asignar si el valor es `no`.

#### condition
- condición de visibilidad
- en este caso la condicion no es una expresión sino un campo calculado que tenga o no valor, el motivo de esto es que esta condición se usa en las plantillas de HBS y ahi la unica forma de hacer un {{if campo}}{{/end}} es si el campo tiene un valor que no sea vacio (`''`), `null`, `false`, `0`, `undefined`.

#### forceReadOnly (booleano)
- aqui puede ir una expresión adiciona para checar si el campo es de lectura.

#### column
-

#### modalColumn
-

#### search
-

#### localSearch
-

#### alwaysLoad
-

#### sendSearchValue
-

#### searchFilters
-

#### showControls
-

#### showClearButton
-

#### validator
-

#### validatorRegEx
-

#### validatorMainDoc
-

#### total
-

#### hide
-

#### link
-

#### modalHide
-

#### recordHide
-

#### tableHide
-

#### reportHide
-

#### disable
-

#### saveSelectedItem
-

#### min
-

#### max
-

#### maxLength
-

#### options
-

#### definitionWidth
-

#### definition
-

#### definition2
-

#### fixedColumn
-

#### multipleTileView
-

#### multipleTileViewWidget
-

#### multipleTileViewLabel
-

#### multipleTileViewLabel2
-

#### multipleTileViewTitle
-

#### multipleTileViewTitle2
-

#### multipleTileViewGrid
-

#### unlink
-

#### forceGetScope
-

#### insertLot
-

#### insertLotWidth
-

#### editRole
-

#### showRole
-

#### subParams
-

#### player
-

#### playerSource
-
