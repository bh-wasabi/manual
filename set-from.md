# Objeto: **from** (set)
- sirve para leer el dato desde otra fuente.

## Parámetros

#### consecutive
- para obtener el siguiente consecutivo.
- aqui se asigna la llave del consecutivo
- puede ser una [expresión](expr.md).
- el contexto que genera es `_value`.

#### source
- `balance` para obtener el saldo de algún indicador.
- `currency-rate` para obtener el tipo de cambio actualizado.

#### from
- en el caso `currency-rate`, aquí se indica la moneda origen.

#### to
- en el caso `currency-rate`, aquí se indica la moneda destino.

#### otros parámetros
- es posible pasar otros parámetros que sirvan como filtro al momento de hacer la consulta a la fuente externa.
- por ejemplo si la fuente es `balance` podemos enviar cualquiera de los campos que usa la tabla (`indicator`, `item`, `location`, etc.)

## Ejemplos:
````
{{from source="balance" indicator="inventario" item="alias" location="movimiento.almacen"}}

{{from source="currency-rate" from="USD" to="MXN"}}
````
````
{{#set folio="_value"}}
  {{from consecutive="=base.tipo"}}
{{/set}}
````
