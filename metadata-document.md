#### document
- id del tipo de documento

#### name
- nombre en sigular del tipo documento

#### name2
- se puede usar para tener alguna traducción

#### group
- agrupador del tipo de documento

#### exportBI (booleano)
- 

#### author
- nombre del autor del tipo documento

#### ignore (booleano)
- es posible comentar los renglones del metadata usando esta columna, tambien se recomienda poner el color de las letras en gris para que sea más visual lo comentado.

#### include
- lista de proyectos (separados por comas) que se desean incluir.

#### exclude
- lista de proyectos (separados por comas) que se desean excluir.

#### tplName
- id del template a usar cuando el documento usa como `embed`
- el template debe existir dentro de `_cfg.hbs` en la carpeta `merge`.

#### fullWidth (booleano)
- si es `VERDADERO` pone las etiquetas de los campos en la parte superior y el valor en la parte inferior
- si es `FALSO` pone las etiquetas a la izquierda de los campos, si se usa un lenguaje tipo RTL como hebreo o arabe se ponen las etiquetas y valores en inverso.

#### modalSize
- existen varios tamaños por omisión para las ventanas que se van a usar en ese documento.
- `small`, `medium`, `long`, `long2`, `long3`, `xlong`, `xlong2`, `xlong3`, `xxlong`, `xxlong2`, `xxxlong`, `xxxlong2`, `xxxlong3`, `full`, `full2`, `full3`,`smallwide`, `semiwide`, `wide`, `wide2`, `wide3`, `xwide`, `xwide2`, `xxwide`.

#### font-size-xxl (booleano)
- si se activa aparecen todos los caractéres de esa forma en una fuente extra grande.

#### labelPct
- es posible determinar un % para las etiquetas en una forma cuando esta en modo consulta, por omisión usa el `20`.

#### color
- es posible cambiar el color de la banda superior cuando abre este tipo de documento.
- colores: `blue`, `blue-grey`, `brown`, `cyan`, `deep-purple`, `green`, `grey`, `indigo`, `light-blue`, `light-green`, `orange`, `pink`, `primary`, `read`, `teal`.

#### viewFilters
- es posible pasar algunos filtros a la vista que se usa en ese momento.
- el formato es: `campo1=valor1,campo2=valor2,etc.`

#### fnName
- es posible usar una función (aqui va el id de la función) para poner el nombre del documento.

#### hideTitle (booleano)
- es posible auto-ocular el titulo de la ventana para aprovechar mejor el espacio visual.

#### autoClose (booleano)
- es posible auto-cerrar la forma y evitar algunos clicks innecesarios.

#### autoOpenEditors (booleano)
- es posible auto-abrir la forma para editar y evitar algunos clicks innecesarios.

#### folioName (booleano)
- es posible auto-foliar el documento y asignar el folio al nombre del documento
- se usan en las notas en general.

#### folioFixed
- por medio de esta opción es posible tener un folio unificado de multiples notas.

#### consecutiveType
- ademas del folio, se puede generar un consecutivo que se incrementa en el último paso de la afectación (despues de todas las validaciones)
- este consecutivo se puede generar usando este tipo aquí definido y puede ser una expresión para que sea más dinámico.

#### dynamicName
- es posible folear la nota usando el tipo y sub tipo de movimiento y generar automaticamente un nombre mas dinámico.

#### subjectName
- si el sistema va mandar un mensaje automatico tipo SES (correo electronico) o SMS (mensaje de texto), aqui se puede definir el asunto del mensaje.

#### setSubType
- por medio de esta expresión es posible establecer el sub tipo de movimiento de forma dinámica usando algún campo o expresión.

#### setSubTypeName
- lo mismo que `setSubType`, pero para establecer el nombre del sub tipo de movimiento.

#### flowAutoCompleteCondition
- 

#### browserView
- id de la vista a usar en el browser por omisión.

#### itemTemplate
- template del detalle a usar por omisión.
- el template puede existir en el mismo documento en la zona de `markup` o en `_app`.

#### isNote (booleano)
- es importante marcar los tipos de documentos que son notas.

#### noteReference
- en la colección de notas se puede guardar una referencia indexada para búsquedas o para mostrar en los listados.

#### noteReferences
- en la colección de notas se puede guardar una lista referencias indexada para búsquedas.

#### noteTokensFields
- lista de campos que se van a tokenizar para generar una lista de referencias indexada para las búsquedas-

#### noteDate
- en la colección de notas se puede guardar una fecha indexada para búsquedas o para mostrar en los listados.

#### noteReason
- en la colección de notas se puede guardar un motivo para búsquedas o para mostrar en los listados.

#### noteAmount
- en la colección de notas se puede guardar un importe indexado para búsquedas o para mostrar en los listados.

#### noteAmountRate
- en la colección de notas se puede guardar un tipo de cambio para mostrar en los listados.

#### addResponsable (booleano)
- 

#### allowInsert (booleano)
- permite agregar documentos si se abre el browser con el listado
- en el caso de las notas es muy recomendable que se que sea `FALSO` en todos los casos.

#### allowEdit (booleano)
- permite editar documentos si se abre el browser con el listado
- en el caso de las notas es muy recomendable que se que sea `FALSO` en todos los casos.

#### displayExpr
- es una forma más dinámica de generar el nombre del documento

#### showChangeHistory (booleano)
- si se activa en la forma nos permite ver la historia de quien y cuando fueron modificando el documento a nivel campo.

#### tempSections
- lista de secciones separadas por coma que son temporales y antes de guardar el documento se eliminan.

#### autoAffect
- es posible auto afectar un documento, en las notas debe ser tipo `node` y en los catálogos que generan personas `node-direct`

#### affectPostgre
- 

#### allowNotify (booleano)
- permite la notificación al momento de afectar, con esta opción sale una ventana para seleccionar las personas a notificar.

#### autoNotify (booleano)
- con esta opción se puede generar una notificación automática.
- puede ser una expresión.

#### notifyPerson (booleano)
- se define si la notificación se dirige a la misma persona a la que se hace el documento o nota.

#### notifySubPersons
- es posible notificar a un grupo de personas relacionadas con el documento.

#### notifyList
- es posible configurar una lista de personas o usuarios a notificar y si se activa esta opción al afectar un documento que contenga esto envia multiples notificaciones.

#### notifyTopic
- aqui se define el asunto del mensaje a enviar.
- puede ser una expresión.

#### notifyTpl
- es posible usar un template de HBS para generar un mensaje, se va mandar el documento afectar como scope de la plantilla.

#### notifyBody
- aqui se define el detalle del mensaje si no se unso una plantilla.
- puede ser una expresión.

#### notifyPortal
- es posible poner la URL opcional para complementar el mensaje
- puede ser una expresión.

#### notifyPortalName
- si se usa una URL aqui se puede poner el nombre amigable.

#### notifyPriority
- es posible manejar diferentes prioridades y dependiendo de la severidad del asunto usar diferentes formas de notificación a las personas.
- prioridades: `baja`, `mediana`, `alta`.

#### notifyDisablePdf (booleano)
- en algunas ocaciones el sistema envia el PDF de la nota en forma automática, es posible desactivar esa opción.

#### autoEvalSubPersons
- 

#### hasRules
- 

#### bannerTopTemplate
- id del banner a usar en la parte superior del documento.
- los banners se configuran en `_app.hbs` dentro del `markup`.

#### bannerSideTemplate
- id del banner a usar en la parte lateral del documento.
- los banners se configuran en `_app.hbs` dentro del `markup`.

#### folioServiceName (booleano)
- por medio de esta opción es posible folear el documento usando el nombre del servicio.

#### autoPrint
- id del reporte que se va usar por omisión para generar el PDF del documento unitario.
- por omisión se genera `preliminar` con todos los campos y siguiendo todas las condiciones de visibilidad.

#### autoHeader (booleano)
- se usa en las notas

#### autoStamp (booleano)
- genera automáticamente una firma electronica del documento

#### allowDraft (booleano)
- permite el guardar el documento para despues editarlo y/o procesarlo desde la bandeja de entrada del usuario.

#### disableAttach (booleano)
- deshabilita la opción de adjuntar documentos.

#### disableAttachRecord (booleano)
- 

#### allowMutiply (booleano)
- en algunos documentos tipo `embed` es posible generar una explosión usando algunos criterios.

#### includeInPrintAll (booleano)
- es una opción extra para cuando se quiera saber si esta nota se incluye en la impresión total del expediente de la persona.

#### isAction (booleano)
- 

#### viewRequest (booleano)
- 

#### sidPrefix
- es posible agregar un prefijo al SID que es un id corto adicional que se genera en el documento.

#### dateLabel
- es posible cambiar la etiqueta de fecha que se usa en los reportes preliminares.

#### landscape (booleano)
- para el reporte por omisión es posible imprimirlo en forma horizontal por omisión.

#### isDisabled (booleano)
- 

#### forceReadOnly (booleano)
- condición adicional para forzar modo lectura y no permitir la edición
- puede ser una expresión.

#### forceDate
- se puede establecer otro campo para definir la fecha del documento.
- por omision la fecha se genera de forma automática cuando se guarda el documento.

#### disableAllZones (booleano)
- 

#### disableEditButton (booleano)
- 

#### disableSaveButton (booleano)
- 

#### autoExportItems
- 

#### disableDelete (booleano)
- 

#### validateEmptyMov (booleano)
- esta opción valida que no se pueda afectar una nota si no genera algo en mov, movPoliza o movControl.
- puede ser una expresión.

#### updateParentMultipleNames
- 

#### notReduceBook
- evita la reducción automática de la póliza y deja todos los renglones tal cual como se hayan producido.

#### sort
- es posible especificar el campo por el cual se hace el orden de la vista `lista` que se genera por omisión.
- por omisión el sistema ordena por `_id`

#### sortDirection
- es posible cambiar la dirección del ordenamiento
- `asc` o `desc`

#### style
- es posible agregar un CSS a la plantilla que se genera por omisión en `lista`

#### isDeliveryReception (booleano)
- 

#### allowInsertLot (booleano)
- permite la opción de agregar en lote usando un `grid` donde se puede copiar un tabla de `Excel`.

#### insertLotGrid
- id del `grid` a usar para agregar en lote.

#### insertLotTitle
- título del `grid`.

#### insertLotSection
- sección del documento a modificar.

#### insertLotKeyField
- llave primaria.

#### insertLotClearFields
- lista de campos a borrar cuando se inserta en lote.

#### isRequested (booleano)
- 

#### startOnOpen
- es posible definir cual es la sección que abre por omisión
- si se indica `n/a` no abre nada.

#### docxTemplate
- nombre del archivo `docx` que debe estar en un Bucket especial de `s3` para usar como plantilla.
- https://github.com/open-xml-templating/docxtemplater#readme

#### xlsxTemplate
- nombre del archivo `xlsx` que debe estar en un Bucket especial de `s3` para usar como plantilla.
- https://github.com/optilude/xlsx-template#readme

#### saveRecordDetail (booleano)
- si se activa esta opción, la nota en cuestión queda registrada en la persona.
- se se hacen mas notas similares se van planchando.

#### saveRecordDetailKey
- es posible guardar en la persona en una llave en particular

#### saveRecordDetailValue
- es posible guardar en la persona en un valor en particular del documento

#### userRole
- es posible definir que roles tienen acceso a este documento

#### mapReduceMovControl
- 

#### validateMovControl
- 

#### uniqueMovControl
- 

#### changePersonId
- 

#### changePersonName
- 

#### changePersonType
- 
