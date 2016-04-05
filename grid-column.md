# Objeto: **column** (grid)
- configura una columna de la cuadrícula

## Parámetros
##### field
- se indica campo de la vista a desplegar

##### width
- ancho en pixeles de la columna

##### type (text, number, date)
- el tipo de datos lo obtiene del campo, aquí también lo podemos establecer directamente.

##### label
- la etiqueta la obtiene del campo, aquí también se puede establecer directamente.

##### format
- el formato lo obtiene del campo, aquí también se puede establecer directamente el [formato](format.md).

##### hide (true, false)
- oculta la columna.
- puede ser una [expresión](expr.md).

##### show (true, false)
- muestra la columna. 
- puede ser una [expresión](expr.md).
- por omisión es `true`.

##### alignment (left, center, right)
- alienación de la columna

##### allowEditing (true, false)
- permitir la edición en esta columna

##### allowFiltering (true, false)
- permitir el filtrado sobre esta columna

##### allowFixing (true, false)
- permite fijar la columna 

##### allowGrouping (true, false)
- permite agrupar la columna

##### allowHiding (true, false)
- permite esconder la columna

##### allowResizing (true, false)
- permite ajustar el ancho de la columna

##### allowSearch (true, false)
- con esta opción es posible limitar la búsqueda de algunas columnas

##### allowSorting (true, false)
- con esta opción podemos permitir o no ordenar directamente sobre una columna

