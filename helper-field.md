# Markup: **field**
- define la captura de un campo
- únicamente funciona en las ventanas de tipo [modal](modal.md).

## Contexto
- campo a editar

## Parámetros
##### readOnly (true, false)
- con esta opción es posible controlar esto a nivel forma.
- puede ser una [expresión](expr.md).

## Ejemplo:
````
{{#modal base id="base" name="Datos Básicos"}}
  {{#row}}
    {{#fieldSet}}
      {{field nombre}}
      {{field grupo}}
      {{field estatus}}
    {{/fieldSet}}   
  {{/row}}
{{/modal}}
````