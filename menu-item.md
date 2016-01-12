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

##### menú con múltiples opciones y sub opciones.
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