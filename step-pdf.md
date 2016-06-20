# Objeto: **pdf** (step)
- genera un archivo PDF a partir de una plantilla
- lo almacena en una ruta de s3

## Parámetros
##### template
- identificador de la plantilla a utilizar.

##### s3FilePath
- ruta donde se va almacenar el archivo PDF.

##### as
- el nombre del archivo generado en s3 es posible ponerlo en este nombre.

##### public (true, false)
- genera el archivo publico

##### expires (#)
- si no es publico, es posible indicar los segundos que se vuelve publico el archivo.

##### header
- `html` a usar como encabezado del reporte.

##### headerHeight (#)
- altura del encabezado en pixeles.

##### footer
- `html` a usar como pie del reporte.

##### footerHeight (#)
- altura del pie en pixeles.

##### width (#)
- ancho en pixeles del reporte.

##### height (#)
- alto en pixeles del reporte.

##### pageFormat
- `Letter` por omisión.
- `A3`
- `A4`
- `A5`
- `Legal`
- `Tabloid`

##### pageTop (#)
- margen superior de la página en pixeles.

##### pageBottom (#)
- margen inferior de la página en pixeles.

##### pageLeft (#)
- margen izquierdo de la página en pixeles.

##### pageRight (#)
- margen derecho de la página en pixeles.

##### pageOrientation
- `portrait` por omisión.
- `landscape`

## Sub objetos
##### param
- es posible pasar parámetros adicionales al `template`. 

## Ejemplo:
````
{{#pdf template="email" s3FilePath="'correos/'+base.nombre+'.pdf'" public="true" as="_url"}}
  {{email from="<demo.wasabi@gmail.com>" to="demo@gmail.com" subject="base.nombre" s3FilePath="_url"}}
{{/pdf}}
````

