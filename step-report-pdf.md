# Objeto: **reportToPdf** (step)
- genera un archivo PDF usando el reporte del documento.
- lo almacena en una ruta de s3
- opcionalmente se puede guardar en el Dropbox vinculado.

## Parámetros
#### report
- identificador del reporte a utilizar.

#### s3FilePath
- ruta donde se va almacenar el archivo PDF.
- puede ser una expresión.

#### dropboxFilePath
- ruta de Dropbox donde se va almacenar el archivo PDF.
- puede ser una expresión.

#### context
- es posible cambiar el contexto a usar en el reporte.
- por omisión toma el documento actual.

#### copyToDropbox (true, false)
- con esta opción es posible copiar el reporte en el Dropbox vinculado con el usuario.
- esta opción se puede usar sin la necesidad de definir la ruta en Dropbox, supone que la primera parte de la ruta es el tenant.