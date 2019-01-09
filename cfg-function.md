# Objeto: **function**
- define una función


## Parámetros
#### id
- identificador de la función

#### paramType
- `text` no evalúa el parámetro
- `expr` por omisión

#### returnType
- `text` no evalúa el parámetro
- `json` hace un parseo para obtener los datos
- `expr` por omisión


## Sub Objetos
#### [define](cfg-function-define.md)
- sirve para definir una parámetro de la función

#### [when](cfg-function-when.md)
- condición a evaluar

#### [default](cfg-function-default.md)
- valor por omisión a retornar
- se ejecuta si no encontró ninguna condición previa.

