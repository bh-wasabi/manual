# Objeto: **tileView**
- define un mosaico de imágenes a desplegar en en documento
- para desplegarlas hay que usar un [widget](helper-widget.md) o en un [browser](browser.md).

## Parámetros
#### id
- identificador del mosaico.

#### section
- sección del documento que contiene las imágenes.
- puede ser la misma que se usa para adjuntos.
- para controlar el tamaño individual de cada imagen en el arreglo hay que incluir `widthRatio` y `heightRatio`.

#### allowEdit (true, false)
- permite la edición de documentos.

#### allowSearch (true, false)
- permite buscar.

#### allowAltViews (true, false)
- permite cambiar de vista dinámicamente, requiere que se configure `altViews` en el nodo padre.

#### itemMargin (#)
- separación en pixeles para cada elemento del mosaico.

#### baseItemHeight
- alto por omisión de un elemento del mosaico.

#### baseItemWidth
- ancho por omisión de un elemento del mosaico.

#### itemTemplate
- identificador del [template](template.md) se se usa para dibujar cada elemento del mosaico.

#### direction
- `vertical` por omisión.
- `horizontal`

#### mimeType
- es posible seleccionar el tipo de archivo a mostrar en el carrusel.
- por omisión es `image`.

#### filter
- es posible seleccionar indicar un filtro adicional.
- por ejemplo: `filter="tipo=foto"`.
- es posible tener multiples filtros separados por el símbolo `&`.
- Nota: hay que tomar en cuenta si el campo esta basado en un `preset` el valor a filtrar es el `id`. 

#### showScrollbar (true, false)
- muestra la barra de scroll en el mosaico.
- por omisión es `false`.

## Sub objetos

## Ejemplo
````
{{tileView id="fotos" section="adjuntos" filter="tipo=foto" itemMargin="20" baseItemHeight="130" baseItemWidth="180" itemTemplate="foto" direction="horizontal"}}
````