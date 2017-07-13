# Objeto: **normalize**
- sirve para normalizar los resultados antes de hacer un set.

## Parámetros
#### set
- nuevo valor a poner, puede ser una [expresión](expr.md).

#### in
- lista de posibles valores a reemplazar
- separados por comas

## Ejemplo:
````
{{#set moneda="Moneda"}}
    {{normalize set="MXN" in="mxn,mxp,peso,pesos"}}
    {{normalize set="USD" in="usd,dolar,dolares"}}
    {{normalize set="EUR" in="eur,euro,euros"}}
{{/set}}
````

