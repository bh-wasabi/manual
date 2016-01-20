# Objeto: **insert** (step)
- con este comando es posible crear documentos nuevos.

## Parámetros
##### source
- tipo de documento a crear.
- parámetro opcional, por omisión crea el documento sobre la misma colección.

##### upsert (true, false)
- busca actualizar el documento usando los filtros.

## Sub objetos
##### [create](step-create.md)
- se usa para cada una de las secciones del documento nuevo.

##### [filter](filter.md)
- en el caso del `upsert="true"` es necesario definir los filtros, para que se busque actualizar primero y en caso de que no se encuentre el documento se inserta.