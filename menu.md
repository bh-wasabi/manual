# Objeto: **menu**
- define un menú
- puede ser un menú múltiple o un menú de contexto

## Parámetros
#### id
- identificador del menú

#### name
- nombre del menú

#### shortName
- nombre corto del menú

#### startHref
- es posible que inicie el menú directamente en una opción.
- opcional

#### startName
- si se usa la opción `startHref` aquí debemos indicar el nombre a mostrar.

#### text
- texto a desplegar

#### action
- en algunos menús es posible invocar a una acción del documento.

#### showUserName (true, false)
- con esta opción es posible desplegar el nombre del usuario en el menú principal
- en lugar del nombre de la acción.

#### showProyectName (true, false)
- con esta opción es posible desplegar el nombre del proyecto del usuario en el menú principal

## Sub objetos

#### [item](menu-item.md)
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
