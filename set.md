# Objeto: **set**
- actualiza uno o varios campos de una sección del documento

## Parámetros
#### campo
- uno o varios campos de la sección

#### condition
- con esta opción es posible condicionar la acción.

#### forceMapValue (campo)
- aquí va una expresión con el nombre del campo
- en caso de estar en un grid, es posible leer el nombre del campo y actualizar correctamente el grid.

## Sub objetos

#### [from](set-from.md)
- podemos leer el valor a actualizar desde otro lugar.

#### [normalize](normalize.md)
- podemos normalizar algunos valores facilmente.

## Ejemplos:
`````
{{set total="totales.total"}}
{{set nombre="movimiento.nombre" fecha="movimiento.fecha" moneda="movimiento.moneda"}}
`````

