# Objeto: **browser**
- define una forma de explorar la información.

## Parámetros
#### id
- identificador del explorador.

#### name
- nombre visible del explorador.

#### type
- `list`
- `grid`
- `cube`
- `tileView`

#### list
- identificador de la [lista](list.md), si se quiere usar una lista existente.

#### grid
- identificador de la [cuadrícula](grid.md), si se quiere usar una cuadrícula existente.

#### cube
- identificador del [cubo](cube.md), si se quiere usar un cubo existente.

#### tileView
- identificador del [mosaico](tileView.md) a mostrar.

#### mobile
- identificador del documento móvil a mostrar.

#### source
- con esta opción es posible definir un tipo de documento diferente del actual.

#### view
- [vista](view.md) a utilizar en este explorador.

#### altPlaceholder
- nombre a desplegar.
- por omisión es "Seleccionar..."

#### altViews
- lista de vistas alternativas.

#### altSource
- el filtro completo se genera de la colección indicada.

#### altSourceView
- vista a utilizar en `altSource`.
- también se puede usar `altView`

#### altSourceParam
- nombre del parámetro a enviar a la vista.

#### altSearchEnabled (true, false)
- permite buscar en el filtro.

#### card
- identificador del diseño de la [tarjeta](card.md) a usar.

#### menu
- opcionalmente podemos asignar un [menú](menu.md) especifico a este explorador.

#### showDoc (true, false)
- con esta opción podemos mostrar los detalles del documento anexo.

#### docId
- es posible especificar donde esta el `id` del documento a abrir.
- por omisión es `_id`
- puede ser una expresión.

#### docType
- es posible especificar donde esta el `type` del documento a abrir.
- por omisión es `_type`
- puede ser una expresión.

#### docPosition (%)
- se define el porcentaje de pantalla que va ocupar el documento por omisión.

#### docOrientation (horizontal, vertical)
- se define la orientación que queremos para el documento anexo.

#### pagesTabsPosition
- es posible cambiar este parámetro del documento desde aquí.

## Sub objetos

#### [param](param.md)
- es posible definir parámetros de que se pueden usar en la vista o documento como valores por omisión.
- puede ser una expresión.

#### [list](list.md)
- aquí mismo podemos definir la lista a usar.
- presentación del explorador tipo lista.

#### [grid](grid.md)
- aquí mismo podemos definir la cuadrícula a usar.
- presentación del explorador tipo cuadrícula.

#### [cube](cube.md)
- aquí mismo podemos definir el cubo a usar.
- presentación del explorador tipo cubo.

#### [tileView](tileView.md)
- aquí mismo podemos definir el mosaico a usar.
- presentación del explorador tipo mosaico.
