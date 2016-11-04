# Objeto: **doc**
- define un tipo de documento

## Parámetros

##### type
- tipo de objeto, en este caso debe ser `type="doc"`.

##### id
- identificador del tipo de documento

##### name
- nombre visible del tipo de documento

##### error
- despliega un mensaje de error junto al título del documento.

##### defaultView
- id de la vista por omisión (al usar este tipo de documento desde otros documentos)

##### defaultDisplay
- campo que contiene el nombre o titulo del documento por omisión (al usar este tipo de documento desde otros documentos)
- "seccion.campo"

##### defaultDisplayTemplate
- plantilla a usar para desplegar el documento.
- de esta forma podemos tener un mayor control de la presentación en las ayudas de captura, tipo: `select`, `lookup` y `autocomplete`.

##### preview
- id del reporte por omisión

##### pagesStart (#)
- número de pagina (tab) inicial, por omisión es 1.
- puede ser una expresión.

##### pagesJustified (true, false)
- justifica las páginas (tabs) del documento.

##### pagesTabsPosition
- `top` por omisión.
- `left`

##### pagesTabsWidth (%)
- cuando `pagesTabsPosition="left"` es posible controlar el ancho de la zona donde aparecen los tabuladores.
- por omisión en `10`.

##### pagesTabsHeight
- define la altura de las páginas, para evitar problemas de `scroll`.
- de preferencia especificar en pixeles, por ejemplo: `550px`.

##### allowEdit (true, false)
- permite la edición

##### allowDirectOperations (true, false)
- permite operaciones directas fuera de un proceso

##### allowAdd (true, false)
- permite agregar detalles

##### allowTimeline (true, false)
- presenta la linea del tiempo del documento

##### confirmUnSaved (true, false)
- confirma con el usuario si quiere ignorar los cambios del documento, antes de cambiar de registro.

##### rules
- nombres de las reglas que queremos usar en este tipo de documento.
- por ejemplo el calculo de impuestos, descuentos, etc.

##### promos (true, false)
- si queremos manejar promociones

##### promosSection
- sección del documento donde queremos aplicar las promociones.

##### promosQuantity
- campo que tiene la cantidad, que se necesita para el calculo de las promociones.

##### totalsSection
- nombre de la sección de totalizadores.

##### addModal
- id de la forma modal que se invoca al agregar (un detalle)

##### addLabel
- etiqueta a desplegar en el botón de agregar.

##### attachSection
- sección del documento que va administrar los archivos adjuntos.

##### attachLanguage
Define el nombre de los campos en que se van a guardar los archivos adjuntos.
- `en` Ingles (por omisión).
- `es` Español.

##### attachDisableDragAndDrop (true, false)
- con esta opción es posible desactivar el "arrastrar y soltar" los archivos.

##### optionsSection
- sección del documento que contiene las opciones del artículo.

##### startOnOpen
- al abrir el documento o crear uno nuevo posible indicar la forma [modal](modal.md) al abrir.
- puede ser una [expresión](expr.md).

##### transformOnVCard
- se puede configurar un evento de tipo `transform` al momento de adjuntar un archivo `.vcf` (vCard).
- [estructura del archivo vCard](vcard.md).

##### autoOpenEditors (true, false)
- si se activa aparece la ayuda en captura automáticamente.

##### cfgLinkField 
- `sección.campo` del documento que contiene la configuración externa.
- usa el `preset` del campo para conocer cual es la fuente de su configuración externa.
- esto funciona cuando se quiere hacer una forma dinámica basada en partes externas.
- reemplaza algunos objetos dinámicamente en base a la configuración.
- genera un objeto `_cfg` disponible para hacer expresiones en el documento.

##### getDocFromView
- con esta opción podemos cambiar el origen de donde se obtiene un documento unitario.
- por ejemplo podemos ir a una ruta de s3 a obtener el documento de ahí.

##### postParentSection
- si es un sub documento, con esta opción al guardar el registro se actualiza el `parent` con el contenido del sub documento.
- aquí se indica el nombre de la sección del documento maestro.
- esto únicamente funciona al insertar un sub documento.

##### postCurrentSection
- aquí se define la sección del documento actual a afectar en el documento maestro.

## Sub objetos
##### [param](param.md)
- los parámetros del documento se pueden asignar de forma unitaria también, para que se puedan agregar comentarios a un lado y sea mas claro.

##### [section](section.md)
- aquí se definen las secciones y campos del documento

##### [field](field.md)
- en algunos casos (únicamente de lectura), podemos definir campos directos sin necesidad de que estén contenidos en una sección especifica.
- esto es muy útil cuando son documentos importados de tablas de sql, donde no existen secciones.

##### [view](view.md)
- las vistas son usadas múltiples propósitos, desde tener una consulta simple en ayudas en captura, poder tener vistas con campos específicos o calculados al vuelo, cubos, SQL, cypher, etc.

##### [centralView](centralView.md)
- esto muy útil cuando se quiere re-utilizar una misma vista en varios `widgets` y así evitar consultar innecesarias.

##### [browser](browser.md)
- aquí se define la presentación que necesitamos para que el usuario pueda ver una vista.

##### [grid](grid.md)
- los grid's se pueden usar para configurar una cuadrícula para diferentes usos.

##### [gallery](gallery.md)
- defie una galería de imágenes

##### [map](map.md)
- define un mapa

##### [action](action.md)
- las acciones sirven para poner los botones específicos del documento.

##### [menu](menu.md)
- los documentos pueden contener menús específicos, estos se ligan a una acción tipo menú.

##### [transform](transform.md)
- se pueden definir rutinas de transformación re-utilizables en el mismo documento.

##### [sync](sync.md)
- es posible sincronizar una sección del documento con otra fuente de datos (ej: una tabla de SQL).

##### [graph](graph.md)
- en esta parte se configura como el documento afecta a la base de datos gráfica (GraphDB).
- relaciones con otros documentos.

##### [workflow](workflow.md)
- aquí se definen los flujos de trabajo, ya sean humanos o de maquina.

##### [survey](survey.md)
- es posible definir una encuesta que se aplica sobre el documento.

## Markup
##### [page](page.md)
- aquí se pone todo el diseño de cada una de las páginas (tab) del documento

##### [card](card.md)
- se puede agregar un diseño especifico para cuando tenemos un "browser" tipo "card"

##### [modal](modal.md)
- es el diseño de la ventana modal que aparece al editar una sección del documento.

##### [report](report.md)
- es el diseño de la presentación preliminar de un documento con objeto de impresión.

##### [template](template.md)
- aquí se puede definir una plantilla HTML o XML genérica.