# Objeto: **pipeline**
- consultas avanzadas sobre una colección de documentos.

#### default 
- es posible definir una lista de valores por omisión

## Sub objetos

#### [filter](filter.md)
- se puede definir filtros sobre la consulta

#### [group](view-group.md)
- agrupa por un campo

#### [unwind](view-unwind.md)
- puede explosionar un campo tipo arreglo

#### [sort](sort.md)
- se puede definir el orden del resultado de la consulta

#### [match](filter.md)
- se puede definir filtros adicionales sobre el resultado de la consulta

#### [calc]
- se pueden hacer campos calculados al final del pipeline

#### [mapRedude]
- se pueden hacer un Map Reduce al final de todo


## Ejemplo:
````
{{#pipeline}}
  {{filter field="country" eq="'Canada'"}}
  {{group field="category" as="categoria"}}
  {{group field="color"}}
  {{group field="country" as="pais"}}
  {{group field="quantity" type="sum" as="cantidad"}}
  {{group type="count" as="conteo"}}
  {{unwind field="tags"}}
  {{group field="tags" as="etiqueta"}}
{{/pipeline}}
{{#pipeline}}
  {{sort field="cantidad" direction="desc"}}
{{/pipeline}}    
````