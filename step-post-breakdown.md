# Objeto: **breakdown** (post)
- se define el prorrateo a generar

## Parámetros
##### type
- `manual` prorrateo automático entre la cantidad de elementos del arreglo (por omisión)
- `div` prorrateo sobre una cantidad especifica.
- `inc-`[time](time.md) para incrementar una fecha en la unidad de tiempo seleccionada.
- `dec-`[time](time.md) para decrementar una fecha en la unidad de tiempo seleccionada.

##### value
- es el arreglo a recorrer.

## Sub objetos

##### [set](set.md)
- campo a afectar.

## Ejemplo:
Para afectar el IVA de una factura, en base al desglose calculado.
````
{
  "totales": {
    "importe": 10246,
    "descuentos": 939.6,
    "subTotal": 9306.4,
    "impuestos": 1364,
    "total": 10670.4,
    "desgloseImpuestos": [
      {
        "impuesto": "IVA",
        "tasa": 16,
        "base": 8525,
        "importe": 1364
      },
      {
        "impuesto": "IVA",
        "tasa": "0",
        "base": 356.4,
        "importe": 0
      }
    ]
  }
}
````

````
{{#breakdown value="desgloseImpuestos"}}
    {{set account="impuesto"}}
    {{set subAccount="tasa"}}
    {{set inc="importe"}}
{{/breakdown}}
````