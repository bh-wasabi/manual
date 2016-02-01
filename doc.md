# Objeto: **doc**
- define un tipo de documento

## Parámetros

##### type
- tipo de objeto, en este caso debe ser `doc`

##### id
- identificador del tipo de documento

##### name
- nombre visible del tipo de documento

##### defaultView
- id de la vista por omisión (al usar este tipo de documento desde otros documentos)

##### defaultDisplay
- campo que contiene el nombre o titulo del documento por omisión (al usar este tipo de documento desde otros documentos)
- "seccion.campo"

##### preview
- id del reporte por omisión

##### startPage (#)
- número de pagina (tab) inicial, por omisión es 1.

##### pagesJustified (true, false)
- justifica las páginas (tabs) del documento.

##### allowEdit (true, false)
- permite la edición

##### allowDirectOperations (true, false)
- permite operaciones directas fuera de un proceso

##### allowAdd (true, false)
- permite agregar detalles

##### allowTimeline (true, false)
- presenta la linea del tiempo del documento

##### rules
- nombres de las reglas que queremos usar en este tipo de documento.
- por ejemplo el calculo de impuestos, descuentos, etc.

##### promos (true, false)
- si queremos manejar promociones

##### promosSection
- sección del documento donde queremos aplicar las promociones.

##### promosQuantity
- campo que tiene la cantidad, que se necesita para el calculo de las promociones.

##### totals (true, false)
- si queremos calcular una sección de totalizadores del documento

##### totalsSection
- nombre de la sección de totalizadores.

##### addModal
- id de la forma modal que se invoca al agregar (un detalle)

##### addLabel
- etiqueta a desplegar en el botón de agregar.

##### attachSection
- sección del documento que va administrar los archivos adjuntos.


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