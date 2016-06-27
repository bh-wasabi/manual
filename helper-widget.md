# Markup: **widget**
- presenta un componente para visualizar un indicador

## Contexto
- es opcional
- en el caso de la galería se requiere y debe ser el arreglo que contiene todos los adjuntos, el sistema automáticamente filtra las imágenes.

## Parámetros
##### name
- nombre visible del componente

##### type
- `list` incrusta una [lista](list.md).
- `selectBox` incrusta un [combo](selectBox.md).
- `dateBox` incrusta una [captura de fechas](dateBox.md).
- `cube` incrusta un [cubo](cube.md).
- `grid` incrusta una [cuadrícula](grid.md).
- `chart` incrusta una [gráfica](chart.md).
- `gauge` incrusta una gráfica de tipo [gauge](gauge.md).
- `map` incrusta un [mapa](map.md).
- `scheduler` incrusta una [agenda](scheduler.md).
- `gallery` muestra una galería de imágenes (basado en los archivos adjuntos del documento).
- `tileView` incrusta un [mosaico de imágenes](tileView.md).
- `info` incrusta un [cuadro informativo](info.md).

##### source
- identificador del tipo de documento (opcional).
- cuando se quiere incrustar un objeto de otro tipo de documento.
- sirve para cuando es tipo `list`,  `cube`, `grid` y `chart`.

##### view
- identificador de la vista a utilizar.
- si se usa `source` por omisión toma la vista que esta definida en el tipo de documento.
- sirve para cuando es tipo `list`,  `cube`, `grid` y `chart`.

##### allowOpen (true, false)
- funciona unicamente con listas y con `source`.
- define si es posible abrir el documento que esta ligado al detalle de la lista.

##### label
- nombre a mostrar sobre el menú de contexto.
- cuando se tiene un menú de contexto en las listas.

##### list
- identificador de la lista a incrustar.

##### cube
- identificador del cubo a incrustar.

##### grid
- identificador de la cuadrícula a incrustar.

##### chart
- identificador de la gráfica a incrustar.

##### gauge
- identificador de la gráfica tipo gauge a incrustar.

##### info
- identificador del cuadro informativo a incrustar.

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

## Sub facilitadores
##### [param](helper-param.md)
- podemos pasar parámetros adicionales.
