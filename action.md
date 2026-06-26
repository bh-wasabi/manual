# Objeto: **action**
- define una acción del documento
- esto funciona cuando el documento es editable.

## Parámetros
#### id
- identificador de la acción

#### type
- `open` abre el documento para editarlo.
- `close` guarda los cambios.
- `affect` guarda y afecta el documento (inicia el flujo de trabajo).
- `affect-direct` afecta y si es correcto guarda el documento, es útil para cuando se quiere validar un documento, funciona únicamente con flujos de 1 paso, esta opción no modifica _isAffected="true".
- `cancel` cancela el documento, inicia un flujo de trabajo.
- `add` agrega un detalle, abre la ventana modal asignada.
- `copy` copia el documento.
- `cancel-edit` cancela la edición.
- `geocomplete` herramienta para buscar una dirección o establecimiento y obtener la dirección. [definición del objeto obtenido por google](google-geocomplete.md).
- `menu` podemos tener una acción que invoque a un menú.
- `attach` con esta opción podemos adjuntar archivos al documento.
- `photo` abre la cámara del browser y toma una foto que se convierte en un adjunto automáticamente.
- `subdoc` con esta opción es posible agregar un sub-documento (es necesario especificar `source` para que funcione y definir el botón sobre la forma modal usando `buttonFloat`).
- `add-subdoc` agrega un nuevo documento desde este documento.
- `refresh` refresca el documento.
- `refresh-widgets` refresca los `widgets` del documento.
- `post` para ejecutar un `request` tipo `post` en el backend.
- `get` genera un get con los datos de la forma y opcionalmente la transforma a la captura.
- `update` obtiene una vista y ejecuta un `update` en el documento, usa `source`, `view`y `update`, si no tiene vista usa el mismo documento como contexto.
- `start-workflow` inicia un flujo de trabajo del documento.
- `zoom-in` aumenta el `zoom` del contenido del documento.
- `zoom-out` disminuye el `zoom` del contenido del documento.
- `form-pdf` genera un archivo PDF de la forma.
- `report-pdf` genera un archivo PDF de un reporte del documento.
- `report-docx` genera un archivo docx (Word) de un reporte del documento.
- `report-all` genera un archivo PDF de un reporte de todas los registros de una vista.
- `image-map` despliega una imágen de fondo.
- `sub-link` genera un sub-vínculo.
- `inbox-reassign` asigna la tarea a otro usuario.
- `save-as` guarda un arreglo en un archivo de texto, usa `items` y `fileName`.
- `save-as-excel` guarda un arreglo en un archivo de excel, usa `items` y `fileName`.
- `flatten` en el caso `save-as` se puede usar este parámetro para que los arreglos sean planos. 
- `quickReport` abre una ventana con un reporte.
- `openFile` abre el contenido de un archivo.
- `attachTemplate` abre el contenido de un archivo y abre el resultado en una url.
- `openFolder` abre el contenido de un "carpeta" de adjuntos en s3, usa `path` para saber la ruta, puede usar `sort` y `limit` adicionalmente, también se le puede pasar un arreglo directo a `items`, con la lista de url's a abrir, otra opción puede tener un `source` y `view` para leer los `items`.
- `openPreview` abre un archivo adjunto, si tiene `else` abre una url.
- `viewScheduler` despliega un calendario, requiere definir `scheduler`.
- `viewData` ejecuta una vista y abre un campo de `items`.
- 'viewCube' despliega un cubo, requiere ´cube´.
- `report-markdown` abre un PDF con el `markdown` de un campo, requiere `value`, `templateSource` y `templateId` para saber que tipo documento contiene la plantilla.
- `suggest` se envía el documento a una rutina interna de sugerencia, se puede usar el `as` para usar el resultado como `scope` de un `update`.
- `speak-items` pregunta una lista.
- `export` en el caso de `report-pdf` se puede cambiar el formato de exportación del reporte a `csv` o `json`.
- `inbox-remove`
- `remove`
- `download`
- `logout`
- `openSubDoc`
- `openUrlDoc`
- `iframe`
- `plugin`
- `bim360`
- `openHtml`
- `dicom`
- `notify`
- `paylink`
- `affect-all`
- `print-template`
- `print-zebra-band`
- `view-json`
- `download-text`
- `download-xlsx`
- `save-fields-as-csv`
- `save-layout-as-text`
- `save-as-json`
- `save-as-excel`
- `viewGrid`
- `viewChart`
- `reload-speak-items`
- `run-eval`
- `report-ai`
- `report-xlsx`
- `report-xlsx-template`
- `print-all`
- `print-all-log`
- `bpmn`
- `copy-to-clipboard`
- `survey`
- `view-scheduler`
- `analysis`
- `copyFromNota`
- `pasteItems`
- `pasteText`
- `browser-action`

#### modal
- identificador de la forma modal a invocar

#### label
- etiqueta a mostrar en el botón

#### source
- en el caso de sub-documentos aqui se especifica el tipo de documento a agregar.
- también funciona en el caso de `inbox-reassign`.

#### subType
- puede generar un folio con otro tipo diferente a `source`, tambien se puede controlar la afectación de diferente forma.

#### subTypeName
- nombre del `subType`.

#### view 
- en el caso de `inbox-reassign`, es posible definir la vista.

#### cube
- en el caso de ´viewCube´ se define el cubo a abrir.

#### color
- es posible establecer el color del botón en la acción.
- [lista de colores](colors.md).

#### menu
- identificador del menú a invocar sobre esta acción

#### copyTo
- cuando la acción es `type="copy"` aquí se especifica el tipo de documento donde se va a copiar.
- por omisión es al mismo.

#### exclude o excludeSections
- cuando la acción es `type="copy"` aquí se especifica la lista de secciones o la lista de `seccion.campo` a excluir en la copia.
- es una lista separada por comas.

#### visibleMode
- `open` la acción será visible únicamente al abrir el documento.
- `close` la acción será visible únicamente con el documento cerrado.
- `always` la acción será visible siempre.
- `none` la acción no se muestra.

#### hide (true, false)
- oculta la acción

#### btnSolid (true, false)
- con esta opción es posible forzar a que el botón tenga un fondo solido y no sea transparente.

#### btnFlat (true, false)
- con esta opción es posible forzar a que el botón sea transparente.

#### country
- identificador del país
- esto sirve únicamente en la acción `geocomplete`

#### center
- latitud y longitud para centrar en el mapa
- esto sirve únicamente en la acción `geocomplete`

#### findReference
- busca una referencia al abrir la ayuda
- esto sirve únicamente en la acción `geocomplete`
- puede ser una expresión.

#### condition
- es una [expresión](expr.md).
- es posible condicionar la acción usando el contexto del documento.

#### notCondition
- es una condición falsa

#### pageIndex
- es posible condicionar la acción a una página en particular.
- esto funciona cuando se tienen varios `tabs` en el mismo documento.

#### workflow
- flujo de trabajo a afectar.
- puede ser una [expresión](expr.md).

#### message
- mensaje a desplegar al iniciar el flujo de trabajo o cuando se termina de afectar.

#### url o postPath
- la ruta donde se va hacer el `request`
- debe ser una ruta interna.
- esto funcionan únicamente cuando es `type="post"` o `type="get"`.

#### postSplash
- mensaje a desplegar cuando se esta ejecutando el `post`.
- por ejemplo: `postSplash="Recalculando..."`.

#### postMessage
- mensaje a desplegar cuando termina el `post`.

#### postRefreshList (true, false)
- es posible refrescar por completo la lista del `browser` después del post.

#### confirm (true, false)
- es posible confirmar la acción previo a su ejecución.
- puede ser una [expresión](expr.md).

#### confirmMessage
- es posible desplegar un mensaje distinto al confirmar.
- puede ser una [expresión](expr.md).

#### confirmTitle
- titulo de la confirmación.
- puede ser una [expresión](expr.md).

#### confirmHeight
- alto de la ventana

#### confirmWidth
- ancho de la ventana

#### validateSections (true, false)
- valida las secciones antes de ejecutar la acción.

#### error
- mensaje de Error a desplegar (y parar la ejecución de la acción)
- puede ser una [expresión](expr.md).

#### warning
- mensaje de Advertencia a desplegar (sin frenan la ejecución de la acción)
- puede ser una [expresión](expr.md).

#### sendDeviceDataId
- envia deviceDataId al servidor, si la acción el tipo es `affect`, `affect-direct` y `post`.
- esto sirve para poder hacer los cargos automáticos a las tarjetas de crédito.

#### icon
- es posible agregar un icono a la acción.
- [iconos](ion-icons.md)

#### fileName
- en el caso de algunas acciones como `form-pdf` o `report-pdf`, 'report-markdown' es posible indicar el nombre del archivo a generar.
- puede ser una [expresión](expr.md).

#### report
- en el caso de `report-pdf` es necesario indicar el identificador del reporte.

#### reportToUrl (true, false)
- en el caso de `report-pdf` se puede configurar si el reporte se abre en una URL pública.
- por omisión abre internamente el reporte.

#### reportDocx
- un reporte puede estar basado en una plantilla de MS-Word
- aqui se indica la ruta de s3 donde esta la plantilla.

#### fullScreen (true, false)
- cuando es un sub documento es posible abrirlo en pantalla completa.

#### backgroundImage
- imagen a desplegar
- es una ruta del bucket actual de s3.

#### roundedCorners (true, false)
- en el caso de mapear, es posible redondear las esquinas.

#### reload (true, false)
- al afectar es posible volver a cargar el documento completamente.

#### keepTempSections (true, false)
- al momento de afectar un `workflow` es posible indicar que no borre la secciones temporales.

#### transform
- al hacer algún tipo de `get` podemos hacer una transformación con el resultado del `get` para afectar el documento actual.
- en el caso de `add-subdoc` el `transform` sirve para generar el documento por omisión.

#### items
- arreglo de elementos
- en el caso de `save-as` debe ser un arreglo simple.
- puede ser una [expresión](expr.md).

#### validateBefore (true, false)
- en algunos casos es posible validar en SQL (spValidate) antes de ejecutar la acción.

#### path
- ruta de `s3` a mostrar en la acción `openFolder`.

#### as 
- en algunas ocaciones se puede cambiar el scope.

#### refreshList (true, false)
- refresca la lista de documentos
- esto funciona únicamente en la acción tipo `affect-direct`.

#### fromSource
- tipo documento
- es posible leer una vista (con parámetros) previo a ejecutar la acción

#### fromView
- vista 

#### toSection
- modificar la sección indicada con la vista

#### fromSource2
- tipo documento
- es posible leer una segunda vista

#### fromView2
- vista 

#### toSection2
- modificar la sección indicada con la vista

#### redirect
- después de afectar es posible, re direccionar el browser a la siguiente dirección.

#### voice
- cuando va a ejecutar una acción `speak-items` se puede cambiar la voz, por omisión en Carlos (es-CO)

## Sub objetos
#### [update](update.md)
- en algunas acciones es posible cambiar los campos del documento.

#### [ask](ask.md)
- si la acción es `type="post"` o `type="get"` es posible preguntar algunos parámetros manualmente.
- en caso de `update` es posible usar estos parámetros como `_params`

#### [param](param.md)
- si la acción es `type="post"` o `type="get"` es posible pasar parámetros.

#### [attachType](attachType.md)
- si la acción es `type="attach"` es posible definir el tipo de documento.

#### [map](action-map.md)
- si la acción es `type="image-map"` definir las posibilidades.

#### [link](action-link.md)
- si la acción es `type="sub-link"`, es necesario definir algunos parámetros.

#### [openFile](action-openFile.md)
- funciona cuando es `type="openFile"`.

#### [scheduler](action-scheduler.md)
- configuración del visor del calendario.

## Ejemplo geocomplete
````
{{#action id="cliente-direccion" hide="true" type="geocomplete" county="mx" center="23.634501,-102.552784"}}
    {{#update section="enviar" sourcePath="/"}}
        {{set nombre="@name"}}
        {{set calle="address.street"}}
        {{set colonia="address.substreet"}}
        {{set codigoPostal="address.postal_code"}}
        {{set delegacion="address.sublocality"}}
        {{set estado="address.locality"}}
        {{set pais="address.country"}}
    {{/update}}
{{/action}}
````


#### subProcess
- en caso de bpmn se pueden pasar la lista de sub procesos (activos o generales)

#### subProcessLabel
- etiqueta a mostrar en la ventana del diagrama

#### subProcessAction
- acción a ejecutar en caso de sub procesos activos

