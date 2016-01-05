# Objeto: **validator**
- define la validación de captura en un campo
- pude ser multiple

## Parámetros
##### type
- `required` campo requerido
- `email` valida que el valor corresponda con un correo electrónico
- `numeric` valida que el valor sea numérico
- `stringLength` valida el tamaño del campo en cantidad de caracteres.
- `range` valida que el valor este en el rango (min y max)
- `pattern` debe cumplir con un patrón de captura definido por una expresión regular.

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

