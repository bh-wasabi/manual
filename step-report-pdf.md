# Objeto: **reportToPdf** (step)
- genera un archivo PDF usando el reporte del documento.
- lo almacena en una ruta de s3

## Parámetros
#### report
- identificador del reporte a utilizar.

#### s3FilePath
- ruta donde se va almacenar el archivo PDF.
- puede ser una expresión.

#### context
- es posible cambiar el contexto a usar en el reporte.
- por omisión toma el documento actual.

#### copyToDropbox (true, false)
- con esta opción es posible copiar el reporte en el Dropbox vinculado con el usuario.