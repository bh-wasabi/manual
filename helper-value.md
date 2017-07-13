# Markup: **value**
- imprime el valor literal del campo
- si tiene algún formato definido lo usa automáticamente
- si el campo es un id de otro documento o de algún [preset](editor.md) hay que usar [name](helper-name.md).

## Contexto
- campo

## Parámetros

#### align
- `left`
- `right`
- `center`

#### format
- en los campos tipo number, calc y date, se puede especificar un formato especifico
- el sistema va usar [Moment.js](http://momentjs.com) para formatear las fechas y [Numeral.js](http://numeraljs.com) para formatear los números.
- existen algunos valores pre-definidos como: `format="currency"`.
- el si se indica `format="pesos"` convierte un importe a texto.


## Ejemplo:
````
{{value base.nombre}}
````