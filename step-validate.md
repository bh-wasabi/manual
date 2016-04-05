# Objeto: **validate** (step)
- ejecuta una validación sobre el paso ya sean validaciones del usuario o de otro tipo.

## Parámetros
##### type
- `user` ejecuta una validación para el usuario. (por omisión)
- `xsd` ejecuta una validación de tipo XSD.
- parámetro opcional.

##### condition (true, false)
- espera un resultado verdadero para mandar el error.
- condición a evaluar
- el contexto es el documento y/o el detalle de la sección especifica.
- puede ser una [expresión](expr.md).

##### error
- el texto del error a desplegar
- puede ser una [expresión](expr.md).

##### section
- cuando la sección es de tipo arreglo se valida detalle por detalle.

##### reference
- se puede incluir algún dato del documento que sirva como referencia adicional al usuario.
- puede ser una [expresión](expr.md).

##### xsd
- nombre del archivo de validación XSD.
- actualmente unicamente esta disponible `cfd-3-2`