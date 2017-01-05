# Objeto: **validator**
- define la validación de captura en un campo
- pude ser multiple

## Parámetros

##### id
- identificador de la validación
- opcional

##### type
- `required` campo requerido
- `email` valida que el valor corresponda con un correo electrónico
- `numeric` valida que el valor sea numérico
- `stringLength` valida el tamaño del campo en cantidad de caracteres.
- `range` valida que el valor este en el rango (min y max)
- `pattern` debe cumplir con un patrón de captura definido por una expresión regular.
- `duplicates` valida valores duplicados, el mismo campo en otros documentos de la misma colección.
- `expr` valida usando una expresión.

##### message
- el mensaje de error a desplegar si no cumple con las reglas de validación

##### min (#)
- valor mínimo aceptable

##### max (#)
- valor máximo aceptable

##### trim (true, false)
- elimina los espacios iniciales y finales antes de validar.

##### reevaluate (true, false)
- Indica si la regla debe ser siempre controlada por el valor objetivo o sólo cuando el valor objetivo de los cambios.

##### expr 
- expresión a usar para validar.

##### falseIsValid (true, false)
- si se indica el validación es correcta cuando el valor es falso.

##### log
- es posible mandar un mensaje a la consola para buscar errores.
- puede ser una expresión.
- es recomendable usar la propiedad `id` para identificar la validación.

