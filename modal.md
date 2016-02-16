# Markup: **modal**
- diseño HTML de ventana modal dentro del documento.
- para poder editar los contenidos de una sección especifica.

## Contexto
- sección del documento a editar

## Parámetros
##### id
- identificador del modal

##### name
- nombre visible del modal

##### grid
- identificador de la cuadrícula a utilizar en el modal.

##### next
- es posible indicar la forma modal siguiente.
- puede ser una [expresión](expr.md).

##### prev
- es posible indicar la forma modal anterior.
- puede ser una [expresión](expr.md).

##### cancel (true, false)
- para que aparezca o no el botón de cancelar.
- por omisión es `true`.

##### ok (true, false)
- para que aparezca o no el botón de aceptar.
- por omisión es `true`.

##### size
- `small`
- `medium`
- `large`
- `xlarge`
- `long`
- `xlong`
- `xxlong`
- `xxxlong`
- `wide`
- `xwide`
- `xxwide`
- `full`

##### effects
- `fade`
- `scale`

## Facilitadores
- los objetos de tipo Markup pueden contener HTML abiertamente y sin ninguna restricción.
- [lista de facilitadores](helpers.md).
