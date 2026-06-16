# Objeto: **syncUser** (view)
- sincronización de la vista por usuario.
- Obtiene un resultado de MS-SQL Server y usa un Stored Procedure de MySQL para convertir el resultado en una lista de documentos nuevos a agregar a la colección
- se agrega el ID del usuario a todos los documentos en el campo `_user`.

## Parámetros
#### fromMsSqlQuery
- ejecuta un `query` en la conexión actual de MS-SQL Server
- puede ser una expresión.

#### useMySqlCall 
- ejecuta un `sp` en la conexión actual de MySQL.

#### ttl (#)
- minutos que perdura la sincronización, por ejemplo: `ttl="60"`.

Ejemplo:
````
{{#view id="lista"}}
  {{syncUser fromMsSqlQuery="exec spVerDocumentos 'DEMO'" useMySqlCall="spDemoSincro($body)" ttl="60"}}
  {{#find}}
    {{filter field="_user" eq="user.id"}}
  {{/find}}
{{/view}}
 ````

