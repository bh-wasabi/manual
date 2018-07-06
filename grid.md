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

#### applyTo
- campo de aplicación
- para que actualice los totales hay que activar el `refreshApplyStatus` en el `onChange` de este campo.

#### applyMax
- máximo a aplicar

#### inputBox
- define si aparece una captura para agregar renglones 
- puede ser una expresión

#### inputBoxField
- campo a capturar
- puede ser una expresión

#### inputBoxPlaceholder
- etiqueta a mostrar
- puede ser una expresión

## Sub objetos

#### [column](grid-column.md)
- columna a desplegar en la cuadrícula
