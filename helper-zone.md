# Markup: **zone**
- genera una zona de captura dentro de la página

## Contexto
- no tiene

## Parámetros
##### id
- es el identificador de la zona

##### modal
- forma modal que se abre al editar esta zona
- cuando es un arreglo esto abre la forma modal de un detalle.

##### modalGrid
- cuando es un arreglo esto abre una forma modal que abre todo los detalles juntos.

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