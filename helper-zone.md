# Markup: **zone**
- genera una zona de captura dentro de la página

## Contexto
- no tiene

## Parámetros
#### id
- es el identificador de la zona

#### modal
- forma modal que se abre al editar esta zona
- cuando es un arreglo esto abre la forma modal de un detalle.
- puede ser una [expresión](expr.md).
- Nota: a diferencia del `modalGrid` que la expresión puede ser usando datos del documento que pueden cambiar, en este caso la expresión se calcula al inicializar la forma.

#### modalGrid
- cuando es un arreglo esto abre una forma modal que abre todo los detalles juntos.
- puede ser una [expresión](expr.md).

#### modalTable
- otra forma forma de capturar un arreglo.
- requiere del `modal` para la edición de cada registro de la tabla.
- puede ser una [expresión](expr.md).

#### section
- sección del documento a editar.
- por omisión toma la sección que esta definida en `modal` o  `modalGrid`, en caso de usar expresiones es necesario indicar la sección explícitamente.

#### readOnly
- es posible bloquear una zona
- puede ser una expresión

#### condition
- es posible establecer una condición para abrir una zona
- puede ser una expresión

## Ejemplos:
````
{{#zone id="base" modal="base"}}
  {{#h5}}Datos básicos{{/h5}}
  {{#with base}}
    {{#row}}
      {{#col small="30%" dock="start"}}
        {{#div bold="true" noWrap="true"}}
          {{label nombre}}
          {{br}}{{label estatus}}
        {{/div}}
      {{/col}}
      {{#col small="70%" dock="end"}}
        {{#div noWrap="true"}}
          {{value nombre}}
          {{br}}{{name estatus}}
        {{/div}}
      {{/col}}
    {{/row}}
  {{/with}}
{{/zone}}

{{#zone id="grupos" modalGrid="grupos"}}
  {{table grupos cols="grupo"}}
{{/zone}}
````

