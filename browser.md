# Objeto: **browser**
- define una forma de explorar la información.

## Parámetros
##### id
- identificador del explorador.

##### name
- nombre visible del explorador.

##### type
- `list`
- `grid`
- `cube`
- `tileView`

##### list
- identificador de la [lista](list.md), si se quiere usar una lista existente.

##### grid
- identificador de la [cuadrícula](grid.md), si se quiere usar una cuadrícula existente.

##### cube
- identificador del [cubo](cube.md), si se quiere usar un cubo existente.

##### tileView
- identificador del [mosaico](tileView.md) a mostrar.

##### view
- [vista](view.md) a utilizar en este explorador.

##### altViews
- lista de vistas alternativas.

##### card
- identificador del diseño de la [tarjeta](card.md) a usar.

##### menu
- opcionalmente podemos asignar un [menú](menu.md) especifico a este explorador.

##### showDoc (true, false)
- con esta opción podemos mostrar los detalles del documento anexo.

##### docPosition (%)
- se define el porcentaje de pantalla que va ocupar el documento por omisión.

##### docOrientation (horizontal, vertical)
- se define la orientación que queremos para el documento anexo.

## Sub objetos

##### [list](list.md)
- aquí mismo podemos definir la lista a usar.
- presentación del explorador tipo lista.

##### [grid](grid.md)
- aquí mismo podemos definir la cuadrícula a usar.
- presentación del explorador tipo cuadrícula.

##### [cube](cube.md)
- aquí mismo podemos definir el cubo a usar.
- presentación del explorador tipo cubo.

##### [tileView](tileView.md)
- aquí mismo podemos definir el mosaico a usar.
- presentación del explorador tipo mosaico.
