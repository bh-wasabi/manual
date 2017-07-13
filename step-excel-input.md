# Objeto: **input** (excel)
- otra forma más rápida de pasar los parámetros de secciones completas.

## Parámetros
#### page
- nombre de la página a enviar los parámetros.

#### section
- sección del documento
- también puede ser una lista de secciones separadas por comas (únicamente si todas las secciones indicadas son tipo objeto), esto es para mejorar el performace y hacer menos recálculos.

#### headers
- se indica la primera celda donde inicia el encabezado, por omisión es `A1`.

#### recalc
- `all` por omisión
- `page` recalcula únicamente la página actual.

#### type
- `update-table` por omisión si la sección es un objeto.
- `insert-table` por omisión si la sección es un arreglo.