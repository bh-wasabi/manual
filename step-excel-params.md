# Objeto: **params** (excel)
- define todos los parámetros que vamos a enviar para abrir y/o recalcular una hoja de excel.

## Parámetros
#### page
- nombre de la página a enviar los parámetros.

#### keys
- nombres de las columnas (en el excel) que sirven como llave.
- la lista de nombres van separados por comas.

#### sourcePath
- posición en el documento, por omisión es `sourcePath="/"` (raíz).
- si se posiciona en un arreglo, genera un `set` para cada detalle.
- para evaluar los parámetros.

## Sub objetos

#### set
- asigna el valor a los parámetros.
- la llave es el nombre de la columna en el excel.
- los valores pueden ser [expresiones](expr.md).

## Ejemplo:
````
{{#params page="params" keys="col1" sourcePath="/"}}
    {{set col1="tipoDocumento" col2="movimiento.tipo"}}
    {{set col1="fecha" col2="movimiento.fecha"}}
    {{set col1="usuario" col2="DEMO"}}
{{/params}}
````