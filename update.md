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

#### unless
- condición negativa

#### transform
- identificador de la transformación.
- es posible hacer transformaciones recursivas, si el `update` viene de una transformación padre.

#### view
- vista a usar

#### source
- documento a usar en la vista
- por omisión toma el tipo de documento actual.

#### dmn 
- identificador de la tabla DMN, se tiene que subir previamente con un `make`.

#### fusionOnce
- con esta opción es posible usar multiples tablas DMN para generar el resultado.
- lista de tablas DMN separadas por comas.
- esta opción lo hace una sola vez con el primer registro que se enviar al DMN.

#### fusionAll
- con esta opción es posible usar multiples tablas DMN para generar el resultado.
- lista de tablas DMN separadas por comas.
- esta opción lo hace para cada registro que se enviar al DMN.

#### input o body
- es una forma de pasar los parámetros usando una sección completa, incluso puede ser un arreglo
- en el caso de dmn, se pueden mandar arreglos de arreglos y se van a considerar todo como un solo arreglo.
- por omisión se manda el documento actual.

#### body1, body2, body3
- en las vistas en posible enviar un body como arreglo.
- por omisión se manda el documento actual en body1.

#### output
- se puede especificar un campo de salida unitario

#### map
- es posible concertar los resultados
- lista de campos separada por comas

#### reduce
- es posible reducir los resultados
- lista de campos separada por comas

#### compact (true, false)
- si se ejecuta map/reduce elimina los registros que no tienen valor.

#### pluck
- es posible extraer un campo del resultado, cuando es tipo arreglo

#### orderBy
- al final es posible ordenar el resultado por algún campo.

#### having
- filtra los resultados si estos campos indicados tienen valor (sin hacer map/reduce)
- lista de campos separada por comas

#### copying
- copia los campos del origen en el resultado
- lista de campos separada por comas

#### forceRecalc (true, false)
- forza el recálculo de la sección en algunos casos.

## Sub objetos

#### [param](param.md)
- parámetros

#### [set](set.md)
- actualiza el valor de uno o varios campos.

#### [get](get.md)
- es posible leer un documento externo para usarlo para actualizar.

#### setRef (ref, value)
- es posible poner un valor en una referencia más profunda.

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

