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

##### readOnly (true, false)
- abre el modal en modo consulta.
- puede ser una expresión.

##### disableFirstFocus (true, false)
- con esta opción se usa para que no haga el auto-focus sobre el primer campo de la forma.

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

##### ignoreSectionValidators (true, false)
- con esta opción es posible indicarle al sistema que no ejecute la validación de la sección del documento.
- se usa cuando en el modal no están involucrados los campos que se usan en la validación de la sección.

## Facilitadores
- los objetos de tipo Markup pueden contener HTML abiertamente y sin ninguna restricción.
- [lista de facilitadores](helpers.md).
