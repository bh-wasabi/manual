# Markup: **field**
- define la captura de un campo
- únicamente funciona en las ventanas de tipo [modal](modal.md).

## Contexto
- campo a editar

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