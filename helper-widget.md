# Markup: **widget**
- presenta un componente para visualizar un indicador

## Contexto
- es opcional
- en el caso de la galería se requiere y debe ser el arreglo que contiene todos los adjuntos, el sistema automáticamente filtra las imágenes.

## Parámetros
##### name
- nombre visible del componente

##### type
- `browser` con esta opción es posible incrustar un [browser](browser.md), tiene algunas restricciones.
- `gallery` muestra una galería de imágenes (adjuntas al documento).
- `dashboard-info`

##### source
- identificador del tipo de documento.
- sirve para cuando es tipo `browser`.

##### browser
- identificador del `browser`.

##### gallery
- identificador de la [galería](gallery.md).

##### height
- opcionalmente se puede definir el alto en pixeles que queremos que ocupe el widget.
- funciona únicamente con `gallery`.

##### width
- opcionalmente se puede definir el ancho en pixeles que queremos que ocupe el widget.
- funciona únicamente con `gallery`.

##### color
- [lista de colores](colors.md)
- funciona únicamente con `dashboard-info`.

##### icon
- [lista de iconos](ion-icons.md)
- funciona únicamente con `dashboard-info`.

##### footer
- leyenda visible en el pie del componente
- funciona únicamente con `dashboard-info`.

## Sub facilitadores
##### [param](helper-param.md)
- podemos pasar parámetros adicionales.

##### [indicator](helper-indicator.md)
- funciona únicamente con `dashboard-info`.
