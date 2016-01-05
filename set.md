# Objeto: **set**
- actualiza uno o varios campos de una sección del documento

## Parámetros
##### campo
- uno o varios campos de la sección

## Sub objetos

##### [from](set-from.md)
- podemos leer el valor a actualizar desde otro lugar.

##### [normalize](normalize.md)
- podemos normalizar algunos valores facilmente.

## Ejemplos:
`````
{{set total="totales.total"}}
{{set nombre="movimiento.nombre" fecha="movimiento.fecha" moneda="movimiento.moneda"}}
`````