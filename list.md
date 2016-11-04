# Objeto: **list**
- las listas son muy practicas, ya que podemos tener en un espacio pequeño una descripción compleja del documento.
- es parecido al inbox del correo electrónico.

## Parámetros
##### itemTemplate
- identificador del [template](template.md) se se usa para dibujar cada elemento de la lista.

##### allowSearch (true, false)
- permite la búsqueda en la lista
- busca sobre todo los campos de la vista

##### allowAltViews (true, false)
- permite cambiar de vista dinámicamente, requiere que se configure `altViews` en el nodo padre.

##### allowInsert (true, false)
- permite agregar nuevos documento a la colección

##### allowInsertLot (true, false)
- permite agregar nuevos documento a la colección en [lote](insert-lot.md).

##### allowRefresh (true, false)
- permite refrescar la lista.

##### allowEdit (true, false)
- permite la edición del documento.

##### allowItemClick (true, false)
- permite hacer click en la lista para visualizar el documento.
- por omisión es `true`.

##### items
- si la lista se va usar dentro de un documento como widget, es necesario especificar la sección del documento que contiene la lista (debe ser tipo arreglo).

##### selectItem (#)
- es posible presentar la lista (como widget), indicando en que posición queremos que se posiciona.

## Sub objetos

##### [insertLot](insert-lot.md)
- con esta opción es posible insertar documentos en lote.