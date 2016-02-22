# Objeto: **item** (menu)
- puede ser recursivo, para poder tener "n" niveles de profundidad.

## Parámetros
##### text
- texto a desplegar en el menú

##### type
- `href` se mueve a una url interna o externa.
- `post` ejecuta un ajax post en la url indicada.
- `refresh` refresca la forma actual.
- `popup` abre una ventana tipo popup.
- `doc-add` agrega un detalle al documento en la sección que esta definida.
- `doc-refresh` refresca unicamente el documento.
- `cube-view-names` inserta en esa posición del menú la lista de vistas de ese cubo.
- `cube-view-preferences` abre la ventana para configurar las vistas del cubo.
- `cube-view-save` permite guardar la vista actual del cubro.

##### icon
- nombre del icono a desplegar.
- [lista de iconos](icons.md)

##### href (url)
- interna (ej: `/browser/empresa/lista`)
- externa (ej: `http://google.com`)

##### post (url)
- ejecuta un ajax post a la url que se indique

##### beginGroup (true, false)
- si se activa separa el menú con una linea previa.


## Sub objetos

##### [popup](popup.md)
- para abrir una ventana tipo popup al hacer click.

##### item
- recursivamente

## Ejemplos:
Menú con múltiples opciones y sub opciones:
````
{{#menu id="menu-ver"}}
  {{item text="Opción 1"}}
  {{item text="Opción 2"}}
  {{#item text="Opción 3"}}
    {{item text="Sub opción 3.1"}}
    {{item text="Sub opción 3.2"}}
  {{/item}}
{{/menu}}
````
Menú con vistas del cubo:
`````
{{#menu id="menu-cubo"}}
  {{#item text="Ver" icon="bookmark"}}
    {{item text="(vistas)" type="cube-view-names"}}
    {{item text="Guardar vista..." icon="save" beginGroup="true" type="cube-view-save"}}
    {{item text="Ajustes..." icon="preferences" type="cube-view-preferences"}}
  {{/item}}
  {{item text="Refrescar" icon="refresh" type="refresh"}}
{{/menu}}
`````