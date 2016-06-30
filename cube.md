# Objeto: **cube**
- despliega un cubo en el explorador

## Parámetros
##### allowSorting (true, false)
- le permite al usuario cambiar el orden sobre las dimensiones.

##### allowSortingBySummary (true, false)
- le permite al usuario cambiar el orden sobre las medidas.

##### allowFiltering (true, false)
- le permite al usuario establecer filtros

##### allowExpandAll (true, false)
- le permite al usuario expandir y colapsar todo el cubo

##### autoSaveView (true, false)
- guarda automáticamente el ultimo acomodo (vista) del cubo.
- Nota: para poder configurar las vistas manualmente es necesario apagar esta opción porque se pueden generar conflictos.

##### exportToExcel (true, false)
- permite exportar los datos a Excel.
- unicamente funciona en `Chrome`.

## Sub objetos

##### [column](cube-field.md)
- define una columna del cubo por omisión.

##### [row](cube-field.md)
- define un renglón del cubo por omisión.

##### [data](cube-field.md)
- agrega la dimensión del cubo para un uso posterior.

##### [count](cube-field.md)
- define una medida de tipo conteo

##### [sum](cube-field.md)
- define una medida de tipo suma
- el campo debe ser tipo numérico

##### [avg](cube-field.md)
- define una medida de tipo promedio
- el campo debe ser tipo numérico

##### [min](cube-field.md)
- define una medida de tipo valor mínimo
- el campo debe ser tipo numérico

##### [max](cube-field.md)
- define una medida de tipo valor máximo
- el campo debe ser tipo numérico

## Ejemplo
````
{{#cube allowSortingBySummary="true" allowSorting="true" allowFiltering="true" allowExpandAll="true"}}
  {{column field="category" label="Categoría" width="120"}}
  {{row field="country" label="País" width="150"}}
  {{row field="color" label="Color" width="150" value="=color.toUpperCase()"}}
  {{avg field="price" label="Precio" format="currency"}}
  {{sum field="amount" label="Importe" format="currency"}}
  {{sum field="quantity" label="Cantidad" format="#"}}
  {{count field="quantity" label="Conteo" format="#"}}
{{/cube}}
````