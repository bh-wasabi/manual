# Objeto: **s3**
- busca un archivo especifico en una ruta de s3.


## Parámetros
#### filePath
- ruta donde esta el archivo
- use pueden usar los parametros con prefijo `$` directamente, es posible usar `$tenant`, `$tenantHash` y `$user` sin tener que definirlos.
- puede ser una [expresión](expr.md).

#### sourceType
- `json` convierte el resultado a un json.
- `xml`
- `pdf`	devuelve el binario del PDF en base64.
