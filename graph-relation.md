# Objeto: **relation** (graph)
- define la relación que tiene el documento con otros documentos

## Parámetros
#### name
- es el nombre que se le quiere dar a la relación
- normalmente se usa en mayusculas

#### from
- se indica el tipo de documento con el cual se establece la relación padre.

#### to
- se indica el tipo de documento con el cual se establece la relación hijos.

#### section
- sección del documento que tiene la relación.
- si la sección es tipo arreglo, hace una relación por cada detalle del arreglo.

#### field
- campo de la sección que tiene la relación.

## Sub objetos

#### [set](set.md)
- se pueden asignar propiedades adicionales a la relación usando el comando set.
