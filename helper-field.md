# Markup: **field**
- define la captura de un campo
- únicamente funciona en las ventanas de tipo [modal](modal.md).

## Contexto
- campo a editar

## Parámetros
#### readOnly (true, false)
- con esta opción es posible controlar la edición a nivel forma.
- puede ser una [expresión](expr.md).

#### hide (true, false)
- con esta opción es posible controlar el despliegue a nivel forma.
- en algunos casos es necesario poner el campo invisible para que se guarden los datos en la sección.
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

