# Objeto: **ValueFrom**
- obtiene un valor de una forma mas compleja (desde el servidor)
- estos se re-calculan únicamente en el servidor al momento que se guarda el documento.

## Parámetros

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

#### [param](param.md)
- parámetros

#### input o body
- es una forma de pasar los parámetros usando una sección completa, incluso puede ser un arreglo
- en el caso de dmn, se pueden mandar arreglos de arreglos y se van a considerar todo como un solo arreglo.

#### body1, body2, body3
- en las vistas en posible enviar un body como arreglo.

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

