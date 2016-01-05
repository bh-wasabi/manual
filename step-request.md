# Objeto: **request** (step)
- sirve para generar una solicitud a un recurso externo.

## Parámetros
##### type
- `get`
- `put`
- `post`
- `delete`
- `s3`

##### url
- en el caso del tipo `get`, `put`, `post` y `delete` aquí se especifica la `url` de donde va obtener o enviar el documento.

##### filePath
- en el caso del tipo `s3` aquí se especifica la ruta dentro del bucket de s3.
- el bucket es de uso interno.

##### sourceType
- `json` se parsea el resultado como JSON.
- `xml` se parsea el resultado como XML.
- `raw` no se parsea.

##### transformBody
- se puede generar una [transformación](transform.md) previa del documento actual y así poder mandar el `body` del `request` con otra estructura.

##### ignorePrefixes
- con esta opción es posible eliminar prefijos de los nodos, del documento recibido.

## Sub objetos
- puede ser cualquiera de los objetos del [step](step.md) del flujo de trabajo.
