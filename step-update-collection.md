# Objeto: **updateCollection**
- actualiza directamente un documento en una colección especifica.

## Parámetros

#### source
- tipo de documento a modificar
- puede ser una expresión.

#### id
- id del documento a modificar
- puede ser una expresión.
- tambien es posible usar `filter` para buscar el documento a actualizar.

## Sub objetos

#### [update](step-update-collection-update.md)
- define la sección del documento a modificar.

#### [filter](filter.md)
- define un filtro del documento a actualizar.

## Nota
- cuando se ejecuta `update` no efectúa recálculos, ya que actualiza únicamente los campos que cambian.
- si no existe el documento, no hace nada.