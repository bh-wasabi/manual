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

##### moveX (#)
- es posible mover toda la zona horizontalmente.
- en pixeles.

##### moveY (#)
- es posible mover toda la zona verticalmente.
- en pixeles.

##### cols (#)
- cantidad de columnas cuando es un arreglo.
- por omisión es `1`

##### colSpacing (#)
- espacio entre columnas cuando es un arreglo.
- también puede ser una lista separada por comas.
- por omisión es `200`
- en pixeles.

##### lineSpacing (#)
- espacio entre lineas cuando es un arreglo.
- también puede ser una lista separada por comas.
- por omisión es `50`
- en pixeles.

##### maxLines (#)
- lineas máximas en caso de arreglos.
- por omisión es `10`

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
