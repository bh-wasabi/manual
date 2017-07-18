# Objeto: **when**
- analiza la condiciones de la función.


## Parámetros

#### parametros
- es posible analizar uno o varios parámetros directamente, para tener una sintaxis mas simple.
- si hay varios parámetros juntos todos se consideran `and`.
- los valores pueden contener operadores `=`, `<`, `>`, `<=`, `>=`, `<>`.
- también es posible separar valores por comas y checar en una lista o un arreglo directamente.
- puede ser una expresión.

#### return
- valor a regresar
- puede ser una expresión.

#### push
- valor a regresar, como parte de un arreglo
- la función se sigue ejecutando para buscar si hay mas casos que agregar al arreglo del resultado.
- puede ser una expresión.
- el resultado también puede ser un objeto `push="{campo1: 'valor1', campo2: 'valor2'}"`

#### condition
- es posible considerar un criterio.
- puede ser una expresión


## Ejemplos
````
{{#function id="paisTelefono"}}
  {{define type="param" id="telefono"}}
  {{when condition="calc.in(Number(telefono.substr(0,3)), [480, 505, 520, 575, 602, 928])" return="us"}}
  {{default return="mx"}}
{{/function}}

{{#function id="iconoEstadoAnimo"}}
  {{define type="param" id="estadoAnimo"}}
  {{when estadoAnimo="feliz" return="happy"}}
  {{when estadoAnimo="triste" return="sad"}}
  {{when estadoAnimo="deprimido" return="sad-outline"}}
{{/function}}

{{#function id="regla1"}}
  {{define type="param" id="edad"}}
  {{when edad="<=16" return="'es menor de edad'"}}
{{/function}}

{{#function id="regla2"}}
  {{define type="param" id="edad"}}
  {{when edad="[3,5,10,11]" return="'Edades especiales'"}}
{{/function}}
````

