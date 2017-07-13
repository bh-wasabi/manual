# Objeto: **pipeline**
- consultas avanzadas sobre una colección de documentos.

## Sub objetos

#### [group](view-group.md)
- agrupa por un campo

#### [unwind](view-unwind.md)
- puede explosionar un campo tipo arreglo

#### [sort](sort.md)
- se puede definir el orden del resultado de la consulta

#### [filter](filter.md)
- se puede definir filtros sobre la consulta

## Ejemplo:
````
{{#pipeline}}
  {{group field="category" as="categoria"}}
  {{group field="color"}}
  {{group field="country" as="pais"}}
  {{group field="quantity" type="sum" as="cantidad"}}
  {{group type="count" as="conteo"}}
  {{unwind field="tags"}}
  {{group field="tags" as="etiqueta"}}
  {{filter field="country" eq="'Canada'"}}
{{/pipeline}}
{{#pipeline}}
  {{sort field="cantidad" direction="desc"}}
{{/pipeline}}    
````