# Objeto: **zone** (form)
- define una zona en la forma.

## Parámetros
##### id
- identificador de la zona.

##### section
- sección del documento.

##### readOnly (true, false)
- define si la zona es editable.
- puede ser una expresión.

##### modal
- identificador de la ventana modal a abrir.

##### modalGrid
- identificador de la ventana modal (tipo cuadricula) a abrir.

##### modalTable
- identificador de la ventana modal (tipo tabla) a abrir.

##### width (#)
- ancho de la imagen de la zona.
- en pixeles.

##### height (#)
- alto de la imagen de la zona.
- en pixeles.

##### x (#)
- posición inicial horizontal.
- en pixeles.

##### y (#)
- posición inicial vertical.
- en pixeles.

##### lineSpacing (#)
- espacio entre lineas.
- en pixeles.

##### maxLines (#)
- lineas máximas en caso de arreglos.

##### color
- nombre del color.
- por omision es: `color="black"`.

##### backgroundColor
- color de fondo.

##### fontSize (#)
- define el tamaño de la letra.
- en pixeles.
- por omisión es: `fontSize="25"`

##### fontWeight (normal, bold, bolder, lighter, etc.)
- equivale a `font-weight` del `css`.
- por omisión es: `fontWeight="normal"`

##### fontFamily
- equivale a `font-family` del `css`.
- por omisión es: `fontFamily="'Comic Sans MS', 'Comic Sans', cursive"`

##### condition
- es posible determinar una condición de despliegue de la zona.
- puede ser una expresión.

## Sub objetos

##### [item](form-item.md)
- define un elemento de la forma.
