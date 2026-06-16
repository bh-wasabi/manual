# Objeto: **cypher**
- podemos ejecutar una consulta directa a la base de datos GraphDB.

## Parámetros
#### query
- puede ser a multiples líneas para tener mayor claridad, hay que incluir los parámetros en la misma sentencia.

## Ejemplo:
````
{{#view id="relaciones"}}
    {{cypher query="MATCH (p:Person{name:{name}})-[r]-() RETURN p,r LIMIT 100"}}
{{/view}}
````

