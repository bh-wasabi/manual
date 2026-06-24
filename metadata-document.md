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
- 

#### affectPostgre
- 

#### allowNotify
- 

#### autoNotify
- 

#### notifyPerson
- 

#### notifySubPersons
- 

#### notifyList
- 

#### notifyTopic
- 

#### notifyTpl
- 

#### notifyBody
- 

#### notifyPortal
- 

#### notifyPortalName
- 

#### notifyPriority
- 

#### notifyDisablePdf
- 

#### autoEvalSubPersons
- 

#### hasRules
- 

#### bannerTopTemplate
- 

#### bannerRightTemplate
- 

#### folioServiceName
- 

#### autoPrint
- 

#### autoHeader
- 

#### autoStamp
- 

#### allowDraft
- 

#### disableAttach
- 

#### disableAttachRecord
- 

#### allowMutiply
- 

#### includeInPrintAll
- 

#### isAction
- 

#### viewRequest
- 

#### sidPrefix
- 

#### dateLabel
- 

#### landscape
- 

#### isDisabled
- 

#### forceReadOnly
- 

#### forceDate
- 

#### disableAllZones
- 

#### disableEditButton
- 

#### disableSaveButton
- 

#### autoExportItems
- 

#### disableDelete
- 

#### validateEmptyMov
- 

#### updateParentMultipleNames
- 

#### completeBookItems
- 

#### notReduceBook
- 

#### validateBalanceMN
- 

#### sort
- 

#### sortDirection
- 

#### style
- 

#### isDeliveryReception
- 

#### allowInsertLot
- 

#### insertLotGrid
- 

#### insertLotTitle
- 

#### insertLotSection
- 

#### insertLotKeyField
- 

#### insertLotClearFields
- 

#### isRequested
- 

#### startOnOpen
- 

#### docxTemplate
- 

#### xlsxTemplate
- 

#### saveRecordDetail
- 

#### saveRecordDetailKey
- 

#### saveRecordDetailValue
- 

#### userRole
- 

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
