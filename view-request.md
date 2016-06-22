# Objeto: **request** (view)
- sirve para generar una solicitud a un recurso externo.

## Parámetros
##### type
- `get`
- `put`
- `post`

##### url
- en el caso del tipo `get`, `put`, `post` y `delete` aquí se especifica la `url` de donde va obtener o enviar el documento.

##### sourceType
- `json` se parsea el resultado como JSON (por omisión).
- `xml` se parsea el resultado como XML.

## Sub objetos
##### [param](param.md)


## Ejemplos:
````
{{#request type="get" url="http://api.demo.com/action/id" sourceType="json" as="data"}}
	...
{{/request}}
````