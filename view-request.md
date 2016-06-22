# Objeto: **request** (view)
- sirve para generar una solicitud a un recurso externo.

## Parámetros
##### type
- `get` (por omisión)
- `put`
- `post`

##### url
- en el caso del tipo `get`, `put`, `post` aquí se especifica la `url` de donde va obtener o enviar el documento.
- es posible agregar los parámetros de la vista directamente usando `$`.
- puede ser una [expresión](expr.md).

##### sourceType
- `json` se parsea el resultado como JSON (por omisión).
- `xml` se parsea el resultado como XML.

## Ejemplos:
````
{{#request type="get" url="http://api.demo.com/action/id" sourceType="json" as="data"}}
	...
{{/request}}
````