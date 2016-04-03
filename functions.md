# calc
- funciones predefinidas adicionales

##### expireColor (fecha)
- devuelve el los colores `green`, `yellow`, `red` o `grey`, en base al vencimiento de la fecha.

##### case (id, parámetros...)
- ejecuta una tabla de decisión.
- debe existir el identificador en la configuración (`_cfg`).

##### extract (arreglo, campo)
- extrae un campo de un arreglo y lo convierte a un texto separado por comas.

##### first (arreglo, filtros)
- devuelve el primer elemento del arreglo.
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- si no hay resultados devuelve un objeto vacio `{}`.

##### match (arreglo, filtros) o (arreglo, lista de campos, valores...)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- si no hay resultados devuelve un arreglo vacío `[]`.

##### lookup (arreglo, filtros) o (arreglo, lista de campos, valores...)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- a diferencia de `match` esta comando regresa el primer registro que coincida con el filtro.
- si no hay resultados devuelve un objeto vacío `{}`.

##### lookupInPreset (preset, filtros) o (preset, lista de campos, valores...)
- obtiene el `preset` (con todos sus campos)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- regresa el primer registro que coincida con el filtro.
- si no hay resultados devuelve un objeto vacío `{}`.

Ejemplos: 

Sintaxis 1:
````
calc.lookupInPreset('app.subTipoSujeto', 'tipo='+tipo+'&id='+subTipo).cuenta
````

Sintaxis 2:
````
calc.lookupInPreset('app.subTipoSujeto', 'tipo, id', tipo, subTipo).cuenta
````

#### taxAmount (preset, rateField, keyField, taxTypes, amount)
Esta función regresa el importe de impuestos a nivel línea.
- `preset` tipos de impuestos.
- `rateField` nombre del campo de la tasa dentro del `preset`.
- `keyField` nombre del campo del id dentro del `preset`.
- `taxTypes` campo que contiene la lista (separada por comas) de los impuestos asignados.
- `amount` campo que contiene el importe total (antes de impuestos).

#### taxBreakdown (preset, rateField, keyField, items, taxTypesField, amountField, resultTaxTypeField, resultRateField, resultAmountField)
Esta función regresa el desglose de los impuestos totales de un movimiento.
- `preset` nombre del preset que contiene los tipos de impuestos.
- `rateField` nombre del campo de la tasa dentro del `preset`.
- `keyField` nombre del campo del id dentro del `preset`.
- `items` sección del documento que contiene la lista de artículos.
- `taxTypesField` nombre del campo dentro de los articulos que contiene la lista de impuestos.
- `amountField` nombre del campo que contiene el importe total (antes de impuestos)
- `resultTaxTypeField` nombre del campo del tipo de impuesto (resultado).
- `resultRateField` nombre del campo de la tasa (resultado).
- `resultAmountField` nombre del campo del importe (resultado).
