# Objeto: **update**
- actualiza una sección del documento

## Parámetros
#### section
- sección a modificar 

#### sourcePath
- ruta base del documento, por omisión `"/"`, por ejemplo: `sourcePath="seccion1/seccion2"`.
- las expresiones toman en cuenta esta ruta.
- también es posible usar `[ ]` para dividir las rutas, sobre todo si hay caracteres especiales en las ruta, por ejemplo: `sourcePath="[seccion1][seccion2][seccion3]"`
- Nota: Si se usan los corchetes no hay que poner `/`.

#### type
- `object` 
- `array`

#### value
- es posible establecer el valor de toda la sección directamente.

#### sortBy
- podemos ordenar el resultado, lista de campos separados por comas.

#### groupBy
- agrupa el resultado por la lista de campos (separados por comas) indicados.
- por ejemplo: `groupBy="alias, descripción, unidad, precio"`

#### sum
- cuando se usan los agrupadores podemos indicar que campos hay que centrar.
- por ejemplo: `sum="cantidad,importe"`

#### where
- podemos tener filtros adicionales, separados por comas y en forma de llave=valor.
- por ejemplo: `where="unidad=KG"`

#### indexBy
- podemos indexar el resultado por alguno de los campos, esto genera nuevos sub objetos con la llave por el campo indicado.

#### render
- podemos usar un [template](template.md) especial.

#### condition
- es posible condicionar el `update`.

## Sub objetos

#### [set](set.md)
- actualiza el valor de uno o varios campos.

#### [get](get.md)
- es posible leer un documento externo para usarlo para actualizar.

## Ejemplos
En este ejemplo se actualiza directamente el campo `nombre` de la sección `sujeto`.
````
{{#update section="sujeto"}}
 {{set nombre="Nombre del Sujeto"}}
{{/update}}
````
En este ejemplo se actualiza el nombre de cada artículo, buscando el artículo que le corresponde.
````
{{#update section="articulos"}}
  {{#get id="articulo"}}
    {{set nombre="base.nombre"}}
  {{/get}}
{{/update}}
`````
