# Objeto: **upsertCollection**
- actualiza directamente un documento en una colección especifica.

## Parámetros

#### source
- tipo de documento a modificar
- puede ser una expresión.

#### id
- id del documento a modificar
- puede ser una expresión.
- si el id viene vacío ejecuta `insert`.

## Sub objetos

#### [update](step-update-collection-update.md)
- define la sección del documento a modificar.

#### [create](step-upsert-collection-create.md)
- define la sección del documento a insertar.

## Nota
- cuando se ejecuta `update` no efectúa recálculos, ya que actualiza únicamente los campos que cambian.
- cuando se ejecuta `insert` si genera todos los campos por omisión y recálculos.