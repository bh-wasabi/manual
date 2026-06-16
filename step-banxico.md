# Objeto: **banxico** (step)
- obtiene un valor externo

## Parámetros
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
{{#banxico id="dolar-fix" as="_quote"}}
  {{log id="banxico" quote="_quote"}}
{{/banxico}}
````

regresa:
````
{"id":"dolar-fix", "code":"SF43718", "value":17.6886, "date":"2017-07-27"}
````

