# Objeto: **convert** (step)
- convierte un archivo de un formato a otro formato
- funciona sobre s3

## Parámetros
#### inputFilePath
- ruta del archivo a convertir
- puede ser una expresión.

#### [inputFormat](convert.md)
- formato del archivo a convertir

#### outputFilePath
- ruta del archivo nuevo
- por omisión lo pone en el mismo lugar donde esta el archivo a convertir y le pone la nueva extensión.
- puede ser una expresión.

#### [outputFormat](convert.md)
- formato del archivo nuevo

#### outputPublic (true, false)
- define si el archivo nuevo queda como publico en s3.

#### quality (%)
- porcentaje de calidad
- por omisión `75`

#### removeOnFinish (true, false)
- elimina el archivo a convertir cuando termina el proceso.
- por omisión es `false`.


## Ejemplo
````
{{convert inputFilePath="'docs/'+base.nombre+'.docx'" inputFormat="docx" outputFormat="pdf"}}
````