# Objeto: **onCreate**
- sirve para controlar las acciones cuando un se crea un sub documento.

## Sub objetos

#### [update](on-change-update.md)
- es posible actualizar una sección completa del documento.
- se tiene el documento remoto dentro del contexto.

## Ejemplos:
````
{{#field id="laboratorio"}}
  {{#onCreate}}
    {{#update section="base"}}
      {{set seleccionarDiagnostico="=seleccionarDiagnostico"}}
    {{/update}}
  {{/onCreate}}
{{/field}}
````
