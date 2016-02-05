# Markup: **widget**
- presenta un componente para visualizar un indicador

## Contexto
- es opcional
- en el caso de la galería se requiere y debe ser el arreglo que contiene todos los adjuntos, el sistema automáticamente filtra las imágenes.

## Parámetros
##### name
- nombre visible del componente

##### type
- `cube` incrusta un [cubo](cube.md).
- `grid` incrusta una [cuadrícula](grid.md).
- `chart` incrusta una [gráfica](chart.md).
- `gauge` incrusta una gráfica de tipo [gauge](gauge.md).
- `map` incrusta un [mapa](map.md).
- `scheduler` incrusta una [agenda](scheduler.md).
- `gallery` muestra una galería de imágenes (basado en los archivos adjuntos del documento).
- `tileView` incrusta un [mosaico de imágenes](tileView.md).
- `dashboard-info`

##### source
- identificador del tipo de documento (opcional).
- cuando se quiere incrustar un objeto de otro tipo de documento.
- sirve para cuando es tipo `cube`, `grid` y `chart`.

##### view
- identificador de la vista a utilizar.
- sirve para cuando es tipo `cube`, `grid` y `chart`.

##### cube
- identificador del cubo a incrustar.

##### grid
- identificador de la cuadrícula a incrustar.

##### chart
- identificador de la gráfica a incrustar.

##### gauge
- identificador de la gráfica tipo gauge a incrustar.

##### map
- identificador del mapa a incrustar.

##### scheduler
- identificador de la agenda a incrustar.

##### gallery
- identificador de la galeria a incrustar.

##### tileView
- identificador del mosaico de imágenes a incrustar.

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
