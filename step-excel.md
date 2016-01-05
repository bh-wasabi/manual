# Objeto: **excel** (step)
- sirve para actualizar y/o leer un archivo de excel.
- debe ser un libro de excel 97-2004, con terminación `xls`.
- regresa un objeto donde cada una de las páginas del libro quedan como un sub objeto de tipo arreglo.

por ejemplo:
````
{
  "Hoja1": [
    {
      "_row": 2,
      "campo": "Celda A2",
      "valor": 20
    },
    {
      "_row": 3,
      "campo": "Celda A3",
      "valor": 30
    },
    {
      "_row": 4,
      "campo": "Celda A4",
      "valor": 40
    },
    {
      "_row": 5,
      "campo": "Celda A5",
      "valor": 50
    }
  ]
}
````

## Parámetros
##### type
- `url`
- `local`
- `s3`

##### url
- en el caso del tipo `url` aquí se especifica la `url` donde se encuentra el archivo `.xls`.

##### fileName
- ruta y nombre del archivo `.xls`.
- en el caso de s3, es sobre un bucket de uso interno.

##### headers
- se indica la primera celda donde inicia el encabezado, por omisión es `A1`.

##### pages
- se indica los nombres de las páginas que deseamos obtener (separados por comas).

## Sub objetos
- puede ser cualquiera de los objetos del [step](step.md) del flujo de trabajo.

##### [params](step-excel-params.md)
- la forma como se mandan los parámetros es un poco especial por eso tiene un objeto diferente.