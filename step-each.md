# Objeto: **each**
- genera un cursor para ejecutar multiples acciones para cada uno de los detalles de un arreglo.
- Nota: Si se ejecuta este comando dentro de un `request`, `find`, `query`, etc. que genera un arreglo de documentos, no es necesario indicar el parámetro `items`.

## Parámetros
##### items
- para indicar explícitamente cual es el arreglo a recorrer en el cursor.
- por omisión toma el contexto de la acción anterior, por ejemplo: [sql](step-sql.md), [request](step-request.md), [find](step-find.md), etc.

##### as
- para cada uno de los detalles del arreglo, lo podemos accesar usando este nombre.

##### index
- nombre de la variable donde vamos a almacenar el indice actual del arreglo.

## Sub objetos
- puede ser cualquiera de los objetos del [step](step.md) del flujo de trabajo.

## Ejemplo:
Recorre la lista de empresas que están con estatus Alta y las muestra en la consola del servidor.
````
{{#step}}
  {{#find source="empresa"}}
    {{filter field="base.estatus" eq="on"}}
    {{#each}}
      {{log id="'empresa'" nombre="base.nombre"}}
    {{/each}}
  {{/find}}
{{/step}}
````