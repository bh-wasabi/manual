# Objeto: **formToPdf** (step)
- genera un archivo PDF usando las formas del documento.
- lo almacena en una ruta de s3

## Parámetros

#### s3FilePath
- ruta donde se va almacenar el archivo PDF.
- puede ser una expresión.

#### context
- es posible cambiar el contexto a usar en el reporte.
- por omisión toma el documento actual.

#### copyToDropbox (true, false)
- con esta opción es posible copiar el reporte en el Dropbox vinculado con el usuario.