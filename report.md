# Markup: **report**
- reporte PDF de un documento
- en algunos reportes esta disponible `_items` como parte del scope.

## Parámetros
#### id
- identificador del reporte

#### header
- identificador del encabezado del reporte
- es otro reporte

#### showStandarFooter (true, false)
- muestra el pie de página estandar

#### pageOrientation
- `portrait`
- `landscape`

#### pageSize
- `letter`
- `executive`
- `legal`
- `tabloid`
- `folio`
- `A0, A1, A2, A3, A4...`
- `B0, B1, B2, B3, B4...`
- `C0, C1, C2, C3, C4...`

#### font
- `Comic`
- `OpenSans`
- `Lato`
- `Roboto`

#### fontSize (#)

#### bold (true, false)

#### italics (true, false)

#### alignment

#### color

#### columnGap

#### fillColor

#### decoration

#### decorationStyle

#### decorationColor

#### background

#### lineHeight

## Sub objetos

#### [image](report-image.md)
- define una imagen en el reporte

#### [row](report-row.md)
- imprime un renglón del reporte

#### [columns](report-columns.md)
- define una zona de columnas

#### [column](report-column.md)
- imprime una columna

#### [record](report-record.md)
- imprime en forma de objeto.

#### [table](report-table.md)
- imprime en forma de tabla.