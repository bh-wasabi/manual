# Objeto: **field** (cube)
- esta descripción aplica a todos los campos de un cubo
- column, row, count, sum, avg, min y max.

## Parámetros
#### field
- identificador del campo de la vista

#### label
- etiqueta a desplegar, por omisión toma la del campo

#### width
- ancho de la columna, por omisión toma la del campo

#### format
- formato a usar, por omisión toma el [formato](format.md) del campo

#### value
- es posible modificar el valor a desplegar, pudiendo usar una [expresión](expr.md), por ejemplo: `value="=color.toUpperCase()"`.

#### preset
- es posible indicar el nombre de un `preset` y en lugar de presentar el valor, se va a presentar el nombre.
- unicamente aplica a `column` y `row`.

#### hide (true, false)
- oculta el campo

#### sortOrder
- `desc` orden descendente
- `asc` orden ascendente

### fixedOrder
- es posibile definir el orden en base a lista de nombres, separadas por comas.

#### expanded (true, false)
- abre el cubo con este campo expandido.

#### displayFolder
- sirve para agrupar varios campos y al momento de seleccionar los campos a presentar aparecen como sub campos de esta carpeta virtual.

#### showTotals (true, false)
- podemos controlar si queremos el cubo totalize por esta dimensión.

#### showGrandTotals (true, false)
- podemos controlar el gran total de esa dimensión.

#### groupInterval
- sirve para dividir un campo en partes, por ejemplo en la fecha podemos controlar el año, mes y día, por ejemplo:

`````
{{row field="fecha" type="date" label="Año" groupInterval="year"}}
{{row field="fecha" type="date" label="Mes" groupInterval="month"}}
{{row field="fecha" type="date" label="Día" groupInterval="day"}}
`````