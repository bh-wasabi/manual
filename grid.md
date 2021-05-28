# Objeto: **grid**
- despliega una cuadrícula en el explorador

## Parámetros
#### id
- identificador del grid

#### section
- sección del documento

#### allowRemove (true, false)
- permite eliminar renglones

#### allowInsert (true, false)
- permite insertar renglones

#### allowSort (true, false)
- permite ordenar (al usuario final) 

#### disableEnter (true, false)
- al oprimir `Enter` se queda en la misma posición.

#### sortingMode
- single (por omisión)
- multiple
- none

#### execOnChangeAlways (true, false)
- al aceptar la forma siempre ejecuta la acción `onChange`.

#### sortBy
- es el orden por omisión que se ejecuta al abrir la cuadrícula.
- lista de columnas separadas por comas

#### filter
- es posible seleccionar indicar un filtro adicional.
- por ejemplo: `filter="tipo=foto"`.
- es posible tener multiples filtros separados por el símbolo `&`.

#### rowReadOnly
- es posible condicionar la edición a nivel renglón.
- es una expresión, el `scope` es el renglón del arreglo.

#### applyBase
- importe base a aplicar

#### applyBaseColumn
- columna que contiene el saldo

#### applyTo
- campo de aplicación
- para que actualice los totales hay que activar el `refreshApplyStatus` en el `onChange` de este campo.

#### applyMax
- máximo a aplicar

#### applySuggest
- sugerencia a copiar

#### applyContinue (true, false)
- pone `si` en el campo.

#### applySplit
- permite dividir una linea, copia el renglón y divide la columna de applySuggest y applyTo.

#### applySplitKey
- se puede copiar algún campo que no este visible, como una llave interna.
- puede ser una lista separada por comas.

#### applyValidate (true, false)
- valida que no se exceda al monto sugerido

#### applyValidateAllOrNothing (true, false)
- valida que sea todo o nada

#### applyFilter
- campo a filtar
- elimina todo lo que no es de esa selección.

#### inputBox
- define si aparece una captura para agregar renglones 
- puede ser una expresión

#### inputBoxField
- campo a capturar
- puede ser una expresión

#### inputBoxPlaceholder
- etiqueta a mostrar
- puede ser una expresión

#### columnAutoWidth (true, false, wordWrapEnabled)
- permite controlar el tamaño automático de las columnas.

#### wordWrapEnabled (true, false)
- esto hace que todos los datos salgan a mas renglones si no caben en una línea.

#### pdfFontSize (#)
- cuando se tienen los `quickReports` se puede definir el tamaño de la letra por omisión

#### showDates
- lista de filtros en `quickReports`, separada por comas.
- `next7, next3, tomorrow, today, yesterday, last3, last7, last15, last30`

#### keyField 
- sirve para definir cuál es el campo importante para validar otros campos requeridos, deberia ser el mismo que se define en el parámetro: ´removeIfEmptyField´.


#### fixedRowsTop (#)
- fija renglones superiores

#### fixedColumnsLeft
- fija columnas a la izquierda

## Sub objetos

#### [column](grid-column.md)
- columna a desplegar en la cuadrícula
