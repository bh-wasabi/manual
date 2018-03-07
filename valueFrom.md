# Objeto: **ValueFrom**
- obtiene un valor de una forma mas compleja.
- estos se re-calculan únicamente en el servidor al momento que se guarda el documento.

## Parámetros

#### dmn 
- identificador de la tabla DMN, se tiene que subir previamente con un `make`.
- se genera la sección calculada tipo arreglo automáticamente.
- requiere los parámetros `input`.
- opcionalmente se puede especificar un `map` y/o `reduce`.

#### input
- para el caso de una sección `dmn` se debe especificar el origen de datos a usar en la tabla DMN. 
- puede ser un arreglo.

#### output
- para el caso de `dmn` se puede especificar el campo de salida unitario.

#### map
- es posible concertar los resultados de la tabla DMN.
- lista de campos separada por comas.

#### reduce
- es posible reducir o concentrar los resultados de la tabla DMN.
- lista de campos separada por comas.

#### pluck
- es posible extraer un campo del resultado, cuando es tipo arreglo.
