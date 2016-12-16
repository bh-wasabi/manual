# Objeto: **item** (zone)
- define un elemento en la forma dentro de una zona.

## Parámetros
##### field
- identificador del campo de la sección de la zona.

##### x (#)
- posición inicial horizontal.
- en pixeles.

##### y (#)
- posición inicial vertical.
- en pixeles.

##### maxWidth (#)
- ancho máximo del elemento.
- en pixeles.

##### interSpace (true, false)
- pone un espacio entre las letras.

##### letterSpacing (#)
- espacio entre letras.
- usa el CSS para generar esto, si se quiere que funcione en HTML y PDF usar interSpace.
- en pixeles.

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
- es posible determinar una condición de despliegue de ese campo.
- puede ser una expresión.

## Sub objetos

##### [map](form-map.md)
- es posible establecer las coordenadas (x, y) a nivel valor del campo (opción).
