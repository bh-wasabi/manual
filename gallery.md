# Objeto: **gallery**
- define una galería de imágenes a desplegar en en documento
- para desplegarlas hay que usar un [widget](helper-widget.md).

## Parámetros
##### id
- identificador de la galería

##### mimeType
- es posible seleccionar el tipo de archivo a mostrar en el carrusel.
- por omisión es `image`.

##### filter
- es posible seleccionar indicar un filtro adicional.
- por ejemplo: `filter="tipo=foto"`.
- es posible tener multiples filtros separados por el símbolo `&`.
- Nota: hay que tomar en cuenta si el campo esta basado en un `preset` el valor a filtrar es el `id`. 

##### loop  (true, false)
- activa un carrusel automáticamente

##### slideshowDelay (#)
- tiempo de espera (en mili-segundos) para cambiar de imagen
- esto funciona cuando es tipo carrusel `loop="true"`.

##### animationEnabled (true, false)
- hace un efecto al cambiar de imágen

##### animationDuration (#)
- duración del efecto (en mili-segundos)

##### showIndicator (true, false)
- muestra unos puntos por cada imagen que esta visible en la galería.

##### showNavButtons (true, false)
- muestra unos botones en los lados para poder cambiar de imagen manualmente.

##### initialItemWidth (#)
- opcionalmente se puede especificar el ancho que va ocupar cada imagen individual.

##### stretchImages (true, false)
- con esta opción podemos estirar las imágenes para que ocupen todo el tamaño posible.

##### wrapAround (true, false)
- con esta opción podemos ver en los lados las imagen previa y siguiente.

