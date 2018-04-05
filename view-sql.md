# Objeto: **sql**
- podemos ejecutar una consulta directa a la base de datos SQL, ya sea usando un `query` o llamando a un `stored procedure`.
- los parametros se usan con el prefijo $.

## Parámetros
#### query
- puede ser a multiples líneas para tener mayor claridad, hay que incluir los parámetros en la misma sentencia.

#### call
- nombre del stored procedure con sus parametros.
- es posible usar el parámetro $body si se envió en la vista.

#### mssql
- ejecuta una consulta a MS-SQL (si esta configurado), devuelve el `recordset`.
- puede ser una expresión.
- no funcionan los parámetros con `$`.

#### mssqlMultiple
- ejecuta una consulta a MS-SQL (si esta configurado), devuelve el `recordsets` (mútiples arreglos).
- puede ser una expresión.
- no funcionan los parámetros con `$`.
- en este caso los resultados no se pueden hacer cálculos adicionales.

## Ejemplos:
````
{{#view id="articulos"}}
  {{define type="param" id="tenant" value="session.tenant"}}
  {{sql query="
    SELECT * 
      FROM articulo 
     WHERE tenant=$tenant"}}
{{/view}}

{{#view id="resumen"}}
  {{define type="param" id="tenant" value="session.tenant"}}
  {{sql call="sp_ver_resumen($tenant)"}}
{{/view}}
````