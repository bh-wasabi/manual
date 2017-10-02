# Objeto: **findOne** (step)
- obtiene el primer documento de una colección y filtros específicos.

## Parámetros
#### source
- tipo de documento

#### as
- es posible cambiar el nombre del objeto leído.

#### startWorkflow
- con esta opción es posible iniciar un flujo de trabajo después de obtener el documento.
- puede ser una [expresión](expr.md).

## Sub objetos
- puede ser cualquiera de los objetos del [step](step.md) del flujo de trabajo.

#### [filter](filter.md)
- se deben definir filtros sobre la consulta
