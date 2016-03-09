# Objeto: **grid**
- despliega una cuadrícula en el explorador

## Parámetros
##### allowGrouping (true, false)
- le permite al usuario hacer agrupaciones al vuelo.

##### columnChooser (true, false)
- le permite al usuario quitar o poner columnas.

##### allowSearch (true, false)
- permite la búsqueda integrada a la cuadrícula

##### pageSize (#)
- determina el tamaño de la página visible.

##### allowedPageSizes
- le permite al usuario cambiar el tamaño de la página al vuelo, por ejemplo: `allowedPageSizes="10,20,30"`.

##### filters
- `true` o `header` le permite al usuario filtrar dinámicamente sobre todas las columnas visibles
- `row` agrega una línea al encabezado de la cuadrícula donde el usuario puede establecer un filtro avanzado.

##### allowEdit (true, false)
- permite editar

##### editMode
- `row` por omisión
- `batch`
- `cell`
- Nota: esto funciona cuando el `grid` opera dentro de un `browser` directamente.

## Sub objetos

##### [column](grid-column.md)
- columna a desplegar en la cuadrícula
