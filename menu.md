# Objeto: **menu**
- define un menú
- puede ser un menú múltiple o un menú de contexto

## Parámetros
##### id
- identificador del menu

##### startHref
- es posible que inicie el menú directamente en una opción.
- opcional

##### startName
- si se usa la opción `startHref` aquí debemos indicar el nombre a mostrar.

## Sub objetos

##### [item](menu-item.md)
- puede ser recursivo, para poder tener "n" niveles de profundidad.

## Ejemplos
Menú con opción de cambiar las vistas del cubo:
````
{{#menu id="menu-cubo"}}
  {{#item text="Ver" icon="bookmark"}}
    {{item text="(vistas)" type="cube-view-names"}}
    {{item text="Guardar vista..." icon="save" beginGroup="true" type="cube-view-save"}}
    {{item text="Ajustes..." icon="preferences" type="cube-view-preferences"}}
  {{/item}}
  {{item text="Refrescar" icon="refresh" type="refresh"}}
{{/menu}}
````
