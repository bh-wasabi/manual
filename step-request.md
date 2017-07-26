# Objeto: **request** (step)
- sirve para generar una solicitud a un recurso externo.

## Parámetros
#### type
- `get`
- `put`
- `post`
- `delete`
- `s3`

#### url
- en el caso del tipo `get`, `put`, `post` y `delete` aquí se especifica la `url` de donde va obtener o enviar el documento.

#### as
- el resultado del `request` se pone en este nombre.

#### filePath
- en el caso del tipo `s3` aquí se especifica la ruta dentro del bucket de s3.
- el bucket es de uso interno.

#### sourceType
- `json` se parsea el resultado como JSON (por omisión).
- `xml` se parsea el resultado como XML.
- `raw` no se parsea.

#### body
- es posible indicar directamente el `body` del `request`.

#### transformBody
- se puede generar una [transformación](transform.md) previa del documento actual y así poder mandar el `body` del `request` con otra estructura.
- puede ser una expresión.

#### transformResponse
- se puede generar una [transformación](transform.md) del body obtenido en el request.
- puede ser una expresión.

#### ignorePrefixes
- con esta opción es posible eliminar prefijos de los nodos, del documento recibido.

## Sub objetos
- puede ser cualquiera de los objetos del [step](step.md) del flujo de trabajo.


## Ejemplos:
````
{{#request type="get" url="http://api.demo.com/action/id" sourceType="json" as="data"}}
	...
{{/request}}
````