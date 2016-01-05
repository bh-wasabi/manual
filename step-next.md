# Objeto: **next** (step)
- define el siguiente paso del flujo de trabajo
- este objeto se usa únicamente si para determinar el siguiente paso es necesario evaluar casos.

## Parámetros
##### type
- `case` esta opción sirve para tener múltiples casos

##### value
- valor o [expresión](expr.md) a analizar.

## Sub objetos

##### [case](next-case.md)
- analiza cada caso para determinar el siguiente paso del flujo de trabajo.


## Ejemplo:
````
{{#next type="case" value="movimiento.autorizacion"}}
    {{case when="normal" then="resolver"}}
    {{case when="autorizar" then="autorizar"}}
{{/next}}
````