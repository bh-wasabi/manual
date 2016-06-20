# Objeto: **pdf** (step)
- genera un archivo PDF a partir de una plantilla
- lo almacena en una ruta de s3

## Parámetros
##### template
- identificador de la plantilla a utilizar.

##### s3FilePath
- ruta donde se va almacenar el archivo PDF.

##### public (true, false)
- genera el archivo publico

##### as
- el nombre del archivo generado en s3 es posible ponerlo en este nombre.


## Sub objetos
##### param
- es posible pasar parámetros adicionales al `template`. 