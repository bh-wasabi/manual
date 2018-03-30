# Objeto: **syncUser** (view)
- sincronización de la vista por usuario.
- Obtiene un resultado de MS-SQL Server y usa un Stored Procedure de MySQL para convertir el resultado en una lista de documentos nuevos a agregar a la colección
- se agrega el ID del usuario a todos los documentos en el campo `_user`.

## Parámetros
#### fromMsSqlQuery
- ejecuta un `query` en la conexión actual de MS-SQL Server
- puede ser una expresión.

#### toMySqlCall 
- ejecuta un `sp` en la conexión actual de MySQL.


Ejemplo:
````
{{#view id="lista"}}
  {{syncUser fromMsSqlQuery="exec spVerDocumentos 'DEMO'" toMySqlCall="spDemoSincro($body)"}}
  {{#find}}
    {{filter field="_user" eq="user.id"}}
  {{/find}}
{{/view}}
 ````