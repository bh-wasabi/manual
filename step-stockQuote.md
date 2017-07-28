# Objeto: **stockQuote** (step)
- obtiene un valor externo

## Parámetros
#### source
- `banxico` Banco de México

#### id
- identificador del símbolo, dependido de la fuente del mismo.

###### Símbolos de Banxico
- `dolar-fix` (SF43718)
- `dolar-liquidacion` (SF60653)
- `euro` (SF46410)
- `yen` (SF46406)
- `libra-esterlina` (SF46407)
- `dolar-canadiense` (SF60632)
- `tasa-objetivo` (SF61745)
- `tiie-28d` (SF60648)
- `tiie-91d` (SF60649)
- `cetes-28d` (SF60633)
- `udis` (SP68257)
- `reservas-internacionales` (SF43707)

#### as
- es posible cambiar el nombre del objeto leído.

## Sub objetos
- puede ser cualquiera de los objetos del [step](step.md) del flujo de trabajo.


# Ejemplo:
````
{{#stockQuote source="banxico" id="dolar-fix" as="_quote"}}
  {{log id="banxico" quote="_quote"}}
{{/stockQuote}}
````

regresa:
````
{"id":"dolar-fix", "source":"banxico", "symbol":"SF43718", "value":17.6886, "date":"2017-07-27"}
````