# Objeto: **find** (step)
- obtiene un arreglo de documentos de una colección interna.

## Parámetros
#### source
- tipo de documento

#### as
- opcionalmente lo podemos accesar usando este nombre

#### limit (#)
- máximo de documentos a obtener

#### skip (#)
- podemos saltar algunos documentos

#### one (true, false)
- si el resultado es un objeto, extrae el primer elemento.

## Sub objetos
- puede ser cualquiera de los objetos del [step](step.md) del flujo de trabajo.

#### [include](view-include.md)
- se define el campo a incluir en la vista

#### [exclude](view-exclude.md)
- se define el campo a excluir en la vista

#### [sort](sort.md)
- se puede definir el orden del resultado de la consulta

#### [filter](filter.md)
- se puede definir filtros sobre la consulta


