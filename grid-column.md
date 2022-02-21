# Objeto: **column** (grid)
- configura una columna de la cuadrícula

## Parámetros
#### field
- se indica campo de la vista a desplegar

#### width
- ancho en pixeles de la columna

#### type (text, number, date, button, flag, image)
- el tipo de datos lo obtiene del campo, aquí también lo podemos establecer directamente.

#### boldIf 
- se puede definir una expresión para condicionar el Bold

#### image
- se puede desplegar una imagen en esa celda usando una URL.
- puede ser una expresión.

#### label
- la etiqueta la obtiene del campo, aquí también se puede establecer directamente.

#### format
- el formato lo obtiene del campo, aquí también se puede establecer directamente el [formato](format.md).

#### showZeros (true, false)
- muestra el valor aunque sea cero.

#### hide (true, false)
- oculta la columna.
- puede ser una [expresión](expr.md).

#### show (true, false)
- muestra la columna. 
- puede ser una [expresión](expr.md).
- por omisión es `true`.

#### buttonCaption
- en caso de tipo `button` aquí podemos establecer título.
- por omisión es `Ver...`
- puede ser una [expresión](expr.md).

#### buttonCondition (true, false)
- en caso de tipo `button` aquí podemos condicionar si aparece.
- por omisión es `true`
- puede ser una [expresión](expr.md).

#### alignment (left, center, right)
- alienación de la columna

#### allowEditing (true, false)
- permitir la edición en esta columna

#### allowFiltering (true, false)
- permitir el filtrado sobre esta columna

#### allowFixing (true, false)
- permite fijar la columna 

#### allowGrouping (true, false)
- permite agrupar la columna

#### allowHiding (true, false)
- permite esconder la columna

#### allowResizing (true, false)
- permite ajustar el ancho de la columna

#### allowSearch (true, false)
- con esta opción es posible limitar la búsqueda de algunas columnas

#### allowSorting (true, false)
- con esta opción podemos permitir o no ordenar directamente sobre una columna

#### summaryType
- `sum`
- `count`
- `avg`
- `min`
- `max`

#### summaryFormat
- `fixedPoint`

#### summaryPrecision (#)
- precisión del formato

#### validateNumber (true, false)
- valida que el texto capturado sea una número válido

#### validatePositiveNumber (true, false)
- valida que el texto capturado sea una número válido y mayor de cero

#### validateDate (true, false)
- valida que el texto capturado sea una fecha válida en formato YYYY-MM-DD o YYYY/MM/DD

#### validateHour (true, false)
- valida que el texto capturado sea una hora válida en formato HH:mm

#### validateDuplicate (true, false)
- valida que no se duplique el valor

#### validateExcess
- valida que el valor no exceda al valor de otro campo.

#### required (true, false)
- define el campo como requerido
- puede tomar en cuenta el `keyField` definido en el `grid`.

#### items
- se puede definir la ayuda en captura directamente sobre esa columna

#### image
- se puede definir una URL que contenga una imagen para esa columna.

## Sub objetos

#### [onClick](field-on-click.md)
- es posible disparar algun evento al hacer click en la columna.
