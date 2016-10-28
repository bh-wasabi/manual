# Markup: **fieldImage**
- define la captura de un campo tipo imagen.
- únicamente funciona en las ventanas de tipo [modal](modal.md).
- debe ir en conjunto con el campo tipo texto donde se va a guardar la url.

## Contexto
- campo a editar

## Ejemplo:
````
{{#modal base id="foto" name="Foto" prev="base" next="direcciones"}}
  {{field foto hide="true"}}
  {{fieldImage foto}}
{{/modal}}
````