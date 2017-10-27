# Objeto: **insert** (step)
- con este comando es posible crear documentos nuevos.

## Parámetros
#### source
- tipo de documento a crear.
- parámetro opcional, por omisión crea el documento sobre la misma colección.

#### upsert (true, false)
- busca actualizar el documento usando los filtros.

#### condition
- con esta opción es posible condicionar la acción.
- puede ser una [expresión](expr.md).

#### startWorkflow
- con esta opción es posible iniciar un flujo de trabajo después de insertar el documento.
- puede ser una [expresión](expr.md).

#### startWorkflowCondition
- es posible condicionar el inicio del flujo de trabajo.
- puede ser una [expresión](expr.md).

## Sub objetos
#### [create](step-create.md)
- se usa para cada una de las secciones del documento nuevo.

#### [update](step-update.md)
- también se puede hacer un update, en el caso del posible upsert.
- esta opción sirve para cambiar parcialmente una sección.

#### [filter](filter.md)
- en el caso del `upsert="true"` es necesario definir los filtros, para que se busque actualizar primero y en caso de que no se encuentre el documento se inserta.