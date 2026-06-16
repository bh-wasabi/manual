# Objeto: **union**
- es posible unir los resultados con otros documentos y crear un resultado de múltiples fuentes.
- esto une los resultados.

## Parámetros
#### source
- tipo de documento a unir.

#### view
- nombre de la vista a unir.

#### leftOuterJoin
- lista separada por comas.
- hace el `LEFT OUTER JOIN` con los campos señalados.
- tienen que tener el mismo nombre del campo de los 2 lados para que se pueda hacer la unión.

#### merge
- lista separada por comas.
- se pueden definir la lista de campos a unir.
