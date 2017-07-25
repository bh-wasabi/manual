# Objeto: **csv** (step)
- genera un archivo csv

## Parámetros
#### items
- para indicar explícitamente cual es el arreglo a convertir en csv.
- por omisión toma el contexto de la acción anterior, por ejemplo: [sql](step-sql.md), [request](step-request.md), [find](step-find.md), etc.
- puede ser una expresión.


#### fields
- campos a seleccionar del arreglo.
- lista separada por comas.

#### fieldNames
- nombres a mostrar en lugar de los campos.
- lista separada por comas.

#### s3FilePath
- ruta donde se almacena el resultado en s3.
- puede ser una expresión.

#### dropboxFilePath
- ruta donde se almacena el resultado en Dropbox.
- puede ser una expresión.

