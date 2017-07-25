# Objeto: **docx** (step)
- renderea un documento (plantilla) de MS-Word usando que este en s3.
- usa el documento actual como `scope`
- en el documento de word hay que usar una sintaxis mas simple, simplemente poniendo entre llaves simples los campos, por ejemplo: `{base.nombre}`.
- es posible recorrer arreglos de esta forma: `{#articulos}{nombre}{/articulos}`

## Parámetros
#### inputFilePath
- ruta de la plantilla en s3.
- puede ser una expresión.

#### outputFilePath
- ruta donde se almacena el resultado en s3.
- puede ser una expresión.

## Ejemplo:
````
{{docx inputFilePath="plantillas/contrato.docx" outputFilePath="'docs/'+base.nombre+'.docx'"}}
````

