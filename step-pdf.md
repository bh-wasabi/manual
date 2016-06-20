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

## Ejemplo:
````
{{#pdf template="email" s3FilePath="'correos/'+base.nombre+'.pdf'" public="true" as="_url"}}
  {{email from="<demo.wasabi@gmail.com>" to="demo@gmail.com" subject="base.nombre" s3FilePath="_url"}}
{{/pdf}}
````

