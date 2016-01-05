# Objeto: **filter**
- a una consulta se le pueden agregar filtros

## Parámetros
##### field
- ruta del campo dentro del documento, normalmente es "campo.valor"

##### eq
- busca que el valor o la expresión indicada sea "igual" al campo indicado.

##### neq
- busca que el valor o la expresión indicada sea "diferente" al campo indicado.

##### in
- busca que el valor o la expresión indicada este en la lista (separada por comas) definida.

##### nin
- busca que el valor o la expresión indicada no este en la lista (separada por comas) definida.

##### gt
- busca que el valor o la expresión indicada sea "mayor que" al campo indicado.

##### gte
- busca que el valor o la expresión indicada sea "mayor o igual" al campo indicado.

##### lt
- busca que el valor o la expresión indicada sea "menor que" al campo indicado.

##### lte
- busca que el valor o la expresión indicada sea "menor o igual" al campo indicado.

##### exists (true, false)
- busca que el campo "exista" o "no exista" con valor en la colección.